desc 'host the site locally'
task :host do
  sh "budo -d docs"
end

desc 'download MapLibre GL JS'
task :download do
  sh <<-EOS
curl -L -o docs/maplibre-gl.js \
https://unpkg.com/maplibre-gl@latest/dist/maplibre-gl.js
curl -L -o docs/maplibre-gl.js.map \
https://unpkg.com/maplibre-gl@latest/dist/maplibre-gl.js.map
curl -L -o docs/maplibre-gl.css \
https://unpkg.com/maplibre-gl@latest/dist/maplibre-gl.css
  EOS
end

desc 'build style.json'
task :build do
  sh <<-EOS
charites --provider maplibre build style.yml \
docs/optbv-intl-dev.json
  EOS
end

desc 'serve the style with unvt/charites'
task :serve do
  sh "charites serve style.yml"
end

desc 'count the lines of yml files'
task :lines do
  sh "wc -l style.yml layers/*.yml"
end

