# Lokalise Theme for ZenDesk

[Lokalise Theme used on Zendesk](https://lokalisesupport.zendesk.com/hc/en-us), based on the [default Copenhagen theme for Zendesk Guide](https://github.com/zendesk/copenhagen_theme) (licensed under [Apache 2.0](https://github.com/zendesk/copenhagen_theme/blob/master/LICENSE)).

## Previewing Locally

[Documentation on Zendesk help](https://support.zendesk.com/hc/en-us/articles/115014810447)

Perform the following step to preview and edit the theme locally:

1. Clone the repo
2. Enable API access in your Zendesk Support account by going to *Admin > Channels > API* and copy your API token
3. Install [Zendesk apps tools](https://develop.zendesk.com/hc/en-us/articles/360001075048) (ZAT):
  + Install [Ruby](https://www.ruby-lang.org/en/downloads/) (if you are on Windows, make sure to use [RubyInstaller](https://rubyinstaller.org/downloads/) with MSYS2). ZAT does not seem to work with Ruby 2.6 and above, so pick Ruby 2.5
  + Do not forget to restart your terminal after installing Ruby
  + Install ZAT by running `gem install zendesk_apps_tools`. This command may take some minutes to complete
4. `cd` into the theme folder
5. Run `zat theme preview`
  + Enter `lokalisesupport` for subdomain
  + Enter `YOUR_EMAIL/token` for login. The `/token` part is required and means you are going to authenticate with an API token obtained at step 2
  + Enter your API token for password
  + You should get a link to theme preview. Preview mode supports live reloading so whenever you edit template files the changes should be reflected nearly instantly
6. If running `zat theme preview` on Windows returns an error related to EventMachine (`Unable to load the EventMachine C extension`), follow these steps:
  + Run `gem uninstall eventmachine` and uninstall all versions
  + `gem install eventmachine --platform ruby`
  + Run `zat theme preview` again
  + [Find more information about this issue on GitHub](https://github.com/oneclick/rubyinstaller2/issues/96)

## Templates
The theme includes all the templates that are used for a Help Center that has *all* the features available.
List of templates in the theme:

* Article page
* Category page
* Community post list page
* Community post page
* Community topic list page
* Community topic page
* Contributions page
* Document head
* Error page
* Footer
* Header
* Home page
* New community post page
* New request page
* Requests page
* Search results page
* Section page
* Subscriptions page
* User profile page

You can add up to 10 optional templates for:

 * Article page
 * Category page
 * Section page

You do this by creating files under the folders `templates/article_pages`, `templates/category_pages` or `templates/section_pages`.
Learn more [here](https://support.zendesk.com/hc/en-us/articles/360001948367).
