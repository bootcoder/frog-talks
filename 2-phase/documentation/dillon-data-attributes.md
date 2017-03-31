# Data Attributes
### Dillon Arevalo

### Overview

HTML tags often (read nearly always) contain attributes. A few examples of attributes you are likely familiar with are the `class` attribute, the `method` or `action` attributes, or the `href` attribute. Attributes are useful for a great many things, including styling, DOM navigation, and modifying the basic functionality of your code.

A subclass of attributes are the `data-*` attributes (where `*` is a placeholder for any number of characters). These attributes are used to store and manipulate data that is relevant to the tag but won't have any immediate functional impact on the HTML object. Instead, this data stored can be read, modified, or used as another useful identifier for a selection of tags.

For example, I could create a whole class of images with similar uses across my website, but they might be different sizes and want to accomplish the same task. I could give them the attributes `data-height="xxx" data-width="yyy"` and be able to reference these values in my javascript or styling.

### Syntax Overview

The `*` in `data-*` is a placeholder meant to be filled with a specific and meaningful word or phrase but there are some limits in the characters you can use. Namely, no uppercase characters are allowed.

The characters are input as any other attribute would be: `<img src="picture.png" alt="my picture" class="profile_picture" id="specific_user_id" data-update-count="4" />`. In this case I'm holding how many times this profile picture has been updated in my `data-update-count` attribute.

When referenced in javascript you can pull up the data attribute and read or write it with `element_name.updateCount`. Note that the name is turned into camel case

### Some Use Cases

a great example from MDN discusses a space ship image sprite in a web game having the following data elements: ```data-ship-id="324"   data-weapons="laserI laserII"   data-shields="72%" data-x="414354" data-y="85160" data-z="31940"```. These data attributes can then be read and modified as the game continues.

Another example from MDN in the Use Data Attributes Guide discusses having an article section with a tag showing how many columns it will be displayed in. This is something that can be done with the css but knowing which articles want to have which characteristics can be very useful.

### Links

- [MDN Use Data Attributes Guide](https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes)
- [MDN `data-*` Info Page](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/data-*)
- [Sitepoint Introductory Guide](https://www.sitepoint.com/use-html5-data-attributes/)
