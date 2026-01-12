# rspec-teamcity-formatter

RSpec formatter that outputs test results in [TeamCity service message format](https://www.jetbrains.com/help/teamcity/service-messages.html), enabling 
integration with TeamCity CI and JetBrains IDEs (RubyMine, IntelliJ IDEA).

## Background

This formatter was extracted from [JetBrains RubyMine](https://www.jetbrains.com/ruby/) to allow standalone use in 
custom tooling, Docker containers, and CI environments without requiring the full IDE.

## Installation

Add to your Gemfile:

```ruby
gem 'rspec-teamcity-formatter'
```

Or install directly:

```bash
gem install rspec-teamcity-formatter
```

## Usage

```bash
rspec --require teamcity/spec/runner/formatter/teamcity/formatter --format Spec::Runner::Formatter::TeamcityFormatter
```


## Output Format

Produces TeamCity service messages like:

```
##teamcity[testStarted name='my test']
##teamcity[testFinished name='my test' duration='42']
```

These messages are automatically parsed by TeamCity and JetBrains IDEs to display real-time test results.

## Attribution

Original code © JetBrains s.r.o. Extracted from RubyMine IDE source code.

## License

Apache License 2.0 - see [LICENSE](LICENSE.txt) file
