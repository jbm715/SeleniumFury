SeleniumFury
=========
 Selenium Fury helps you quickly build page objects when using either Selenium RC API or Selenium Web Driver API.
 
Demo Setup
=========
If you are running the demo from the source.

```ruby
bundle console
require 'spec/spec_helper'
```

If you are running the demo from the installed gem

```ruby
irb
require 'selenium_fury'
include SeleniumFury::SeleniumWebDriver::CreateSeleniumWebDriver
```

Quick Test Demo
=========
```ruby
launch_web_driver("http://www.homeaway.com/")
home_page=get_page_object(driver,'HomePage')
home_page.search_keywords.send_keys 'Destin'
home_page.keyword_submit.click
driver.quit
```

Generate Demo
=========
```ruby
launch_web_driver("http://www.homeaway.com/")
generate(driver)
driver.quit
```
Validate Demo
=========
```ruby
launch_web_driver("http://www.homeaway.com/")
get_page_object(driver,'HomePage')
validate(HomePage)
driver.quit
```

#Element Types
=======
 * GenericElement - any type of element
 * CheckboxElement - a checkbox
 * DropDownElement - a dropdown
 * ImageElement - an image element
 * LinkElement - an anchor element
 * RadioButtonElement - a radio button
 * SubmitElement - buttons
 * TextElement - an static element that holds text
 * TextInputElement - a user interactable element
 * SelectableElement - a generic radio type button


Notes on #set and #value
========
 * set should only work on elements that can be interacted with
 * value should only work on elements that can be interacted with



========

 * [Scott Sims](http://scottcsims.com/): Current maintainer.

Copyright
=========
* Copyright (c) 2012 HomeAway, Inc.
* All rights reserved.  http://www.homeaway.com
  See LICENSE for details.
