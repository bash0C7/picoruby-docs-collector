# picoruby-docs

Collector for PicoRuby gem documentation. Parses RBS type signatures and README files from picoruby/picoruby mrbgems directory.

## Usage

```ruby
require 'picoruby_docs'

collector = PicorubyDocs::Collector.new(
  { 'repo_path' => '/path/to/picoruby' }
)
records = collector.collect
# => [{ content: "GPIO class...", source: "picoruby/picoruby:docs/picoruby-gpio" }, ...]
```

## Development

```bash
bundle config set --local path vendor/bundle
bundle install
bundle exec rake test
```
