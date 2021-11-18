# Intellij, PHPStorm, PyCharm, Webstorm, etc. - Prefill Commit Messages with Ticket Number from Branch

If you use Intellij, PHPStorm, Webstorm, etc. + a ticket system, this solution might be helpful for you, to spice up your commit messages 🔥🌶️

You will install a custom Intellij plugin and use a regex. When you commit your changes, the commit message will be automatically prefilled with the ticket number you provided in your branch.

The solution supports the following branches. On the right you can see the result.

<pre>
feature/#3444_test                          => #3444
#3444_test                                  => #3444
feature/#123-ABC_test                       => #123-ABC
feature/#123ABC-ABC123_test                 => #123ABC-ABC123
feature/#ABC-123_test                       => #ABC-123
bug/#ABC123-123_test                        => #ABC123-123
bug/#ABC123ABC-123_test                     => #ABC123ABC-123
</pre>


## Install plugin

https://plugins.jetbrains.com/plugin/14762-git-commit-message-template

## IDE Settings

- Open your Intellij Settings
- Go to `Other Settings | Git Commit Message Template`
- Go to `Regex to extract info from branch`
- Select `Custom` and add the regex from below the image ⬇️

<img width="1003" alt="ticket-nr-commit-message" src="https://user-images.githubusercontent.com/25182140/142412294-6d6e62e8-f726-4822-bafb-9860c8f6c5bc.png">



## Regex

````
(\#[a-zA-Z0-9\-]+[a-zA-Z0-9]+)|(\#[0-9]+)
````

To complete your setup hit `Apply`, now you are ready to commit 🚀
