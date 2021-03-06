# OmniAuth Intuit

This gem contains the Intuit strategy for OmniAuth 1.0

Intuit uses the OAuth 1.0a flow, you can read about it here: https://ipp.developer.intuit.com/0010_Intuit_Partner_Platform/0030_Intuit_Anywhere/0036_Coding_Your_App/0050_OAuth_for_Intuit_Anywhere

## How To Use It

Usage is as per any other OmniAuth 1.0 strategy. So let's say you're using Rails, you need to add the strategy to your `Gemfile` along side omniauth:

    gem 'omniauth'
    gem 'omniauth-intuit'

Next, you need to add the following to your `config/initializers/omniauth.rb`:

    Rails.application.config.middleware.use OmniAuth::Builder do
      provider :intuit, "consumer_key", "consumer_secret" 
    end

You will get your consumer key and secret when you register your app with Intuit Anywhere.  (See
https://ipp.developer.intuit.com/0010_Intuit_Partner_Platform/0030_Intuit_Anywhere/0040_Hello_World_IA for an example)

You can now follow the OmniAuth README at: https://github.com/intridea/omniauth

## Running example code

`shotgun -s thin -d -p 3000 config.ru`     

## Note on Patches/Pull Requests

- Fork the project.
- Make your feature addition or bug fix.
- Add tests for it. This is important so I don’t break it in a future version unintentionally.
- Commit, do not mess with rakefile, version, or history. (if you want to have your own version, that is fine but bump version in a commit by itself I can ignore when I pull)
- Send me a pull request. Bonus points for topic branches.

## License

Copyright (c) 2011 by Jaigouk Kim, Profitably

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
