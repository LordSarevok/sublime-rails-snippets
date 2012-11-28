# Sublime Text 2 Rails snippets

I don't know who the original author is, but this repo is an improved version of https://github.com/bradrobertson/sublime-packages/tree/master/Rails

# Installation

Backup the old Rails snippets before instalation

    $ cd /Library/Application Support/Sublime Text 2/Packages
    $ mv Rails ~/SublimeRailsBackup

## From Git

    $ cd /Library/Application Support/Sublime Text 2/Packages
    $ git clone https://github.com/tadast/sublime-rails-snippets.git Rails

## From Package control

Look for "Ruby on Rails snippets". [Here's how to install packages](http://wbond.net/sublime_packages/package_control/usage)

### Troubleshooting

If Sublime complains it can't `find Ruby on Rails.tmLanguage`, chances are you are using [this hack](https://gist.github.com/925008).
You'll need to change the path where it looks for that file. Here's the [forked version which works with this plugin](https://gist.github.com/4161901).

You may also need to change `Packages/(DetectSyntax|User)/DetectSyntax.sublime-settings` to replace/include this rule

    {
      "name": "Ruby on Rails snippets/Ruby Haml",
      "rules": [
        {"file_name": ".*\\.haml$"}
      ]
    },
    {
      "name": "Ruby on Rails snippets/Ruby on Rails",
      "rules": [
        {"function": {"name": "is_rails_file"}}
      ]
    }



# Changes in this "fork"

* Use ruby 1.9 hash syntax (`foo: :bar`, not ` :foo => :bar`)
* Prefer `=` over `-` for haml snippets (Rails 3 way)
* Prefer `respond to format.html` over `respond to wants.html`
* All rjs snippets removed
* `class<tab>` autocompletes a ruby class
* `arc<tab>` autocompletes an ActiveRecord model class
* `con<tab>` autocompletes a controller class
* `crud<tab>` autocompleted controller actions
