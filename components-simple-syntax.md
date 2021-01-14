# Components Simple Syntax

## Image

To display an image in Leopard using simple output parameters, you need to add an output parameter named `image` and assign the image's URL to the output parameter's value. You can also add an optional alternative text after the URL, with a pipe symbol \('\|'\) as the separator.

![output parameter named image with an url to an image](https://developers.artificial-solutions.com/user/pages/03.engine/02.teneo-web-chat/02.easy-message-type-creation-in-studio/twc_simple_output_param_image.png)

## Image Carousels

## Map

## Tables

## Video

To display a video using simple output parameters, you need to add an output parameter named `video` and assign the video's URL to the output parameter's value.



## Text Alert



## Audio

To display an audio player using simple output parameters, you need to add an output parameter named `audio` and assign the audio's URL to the output parameter's value.



## System message

To display a system message using simple output parameters, you need to add an output parameter named `system` and assign the text message to the output parameter's value.

![output parameter named system with the value containing a system text message](https://developers.artificial-solutions.com/user/pages/03.engine/02.teneo-web-chat/02.easy-message-type-creation-in-studio/twc_simple_output_param_system.png)

## Quick reply

To display quick reply options using simple output parameters, you need to add an output parameter named `quickreply` and assign the options to the output parameter's value. Use the pipe symbol \('\|'\) to separate the options.

![](https://developers.artificial-solutions.com/user/pages/03.engine/02.teneo-web-chat/02.easy-message-type-creation-in-studio/twc_simple_output_param_quickreply.png)

## Buttons

To display buttons using simple output parameters, you need to add an output parameter named `buttons` and assign the button texts to the output parameter's value. Use the pipe symbol \('\|'\) to separate the button texts. If you want to add a title to your buttons, create another output parameter named `buttons_title` and assign the title text to the output parameter's value.

![two output parameters. One named buttons containing the buttons text, the other is named buttons\_title containing the title text](https://developers.artificial-solutions.com/user/pages/03.engine/02.teneo-web-chat/02.easy-message-type-creation-in-studio/twc_simple_output_param_buttons.png)

The JSON for each button option consists of three elements:

## Clickable list

To display a clickable list using simple output parameters, you need to add an output parameter named `clickablelist` and assign the options to the output parameter's value. Use the pipe symbol \('\|'\) to separate the options. If you want to add a title to your clickable list, create another output parameter named `clickablelist_title` and assign the title text to the output parameter's value.

![](https://developers.artificial-solutions.com/user/pages/03.engine/02.teneo-web-chat/02.easy-message-type-creation-in-studio/twc_simple_output_param_clickablelist.png)

## Link buttons

To display link buttons using simple output parameters, you need to add an output parameter named `linkbuttons` and assign the link button details \(text, url and optional target\) to the output parameter's value. Use the pipe symbol \('\|'\) to separate the button details. If you want to add a title to your link buttons, create another output parameter named `linkbuttons_title` and assign the title text to the output parameter's value.

![Output parameters for linkbuttons](https://developers.artificial-solutions.com/user/pages/03.engine/02.teneo-web-chat/02.easy-message-type-creation-in-studio/linkbuttons.png)

## Card

A card refers to a box that contains at least one of the following components:

* An image
* A title, subtitle or a body text
* Buttons, links or a clickable list

To display a card using simple output parameters, you need to use the prefix `card_` when naming the output parameters. For example, to display an image, you would name the output parameter `card_image`. Then assign the corresponding content to the output parameter's value. Note that all the card components are optional, however, you need to include at least one component to display the card properly.

![multiple output parameters named with the card prefix &apos;card&apos; containing corresponding content](https://developers.artificial-solutions.com/user/pages/03.engine/02.teneo-web-chat/02.easy-message-type-creation-in-studio/twc_simple_output_param_card.png)

The table below shows the different card components that are supported:

| Output parameter name | Example value | Comments |
| :--- | :--- | :--- |
| card\_title | This is the title | Plain text as value |
| card\_subtitle | This is the subtitle | Plain text as value |
| card\_bodytext | This is the body text | Plain text as value |
| card\_image | https://address/image.png\|alt text | Url of image, use the pipe symbol \('\|'\) as separator for alternative text |
| card\_buttons | Button 1\|Button 2\|Button 3 | Use the pipe symbol \('\|'\) as the separator |
| card\_clickablelist | Option 1\|Option 2\|Option 3 | Use the pipe symbol \('\|'\) as the separator |
| card\_linkbuttons | Link 1,https://link1.html,\_blank\|Link 2,https://link2.html | Use comma as separator between text, URL and \(optional\) target; Use the pipe symbol \('\|'\) the as separator between hyperlinks |
| card\_links | Link 1,https://link1.html\|Link 2,https://link2.html | Use comma as separator between text and URL; Use the pipe symbol \('\|'\) the as separator between hyperlinks. |

Note that the order in which you create the output parameters doesn't affect how the card is displayed in Leopard.

## Modal

A 'modal' refers to a modal window that disables the main chat window. Users will not able to use the text input field nor the corner buttons to minimize or close the chatbot until they've clicked one of the buttons in the modal window.

To display a modal window using simple output parameters, you need to add multiple output parameters with the prefix `modal_`, for example, `modal_image` and `modal_title`. Then assign the corresponding content to the output parameter's value. Note that all the modal components are optional, however, you need to include at least one button, or else the users will not be able to close the modal window.

![multiple output parameters with the modal prefix &apos;modal\_&apos; containing corresponding content](https://developers.artificial-solutions.com/user/pages/03.engine/02.teneo-web-chat/02.easy-message-type-creation-in-studio/twc_simple_output_param_modal.png)

The table below shows the different modal components that are supported:

| Output parameter name | Example value | Comments |
| :--- | :--- | :--- |
| modal\_title | This is the title | Plain text as value |
| modal\_subtitle | This is the subtitle | Plain text as value |
| modal\_bodytext | This is the body text | Plain text as value |
| modal\_image | https://address/image.png\|alt text | Url of image, use the pipe symbol \('\|'\) as separator for alternative text |
| modal\_buttons | Button 1\|Button 2\|Button 3 | Use the pipe symbol \('\|'\) as the separator |
| modal\_clickablelist | Option 1\|Option 2\|Option 3 | Use the pipe symbol \('\|'\) as the separator |
| modal\_linkbuttons | Link 1,https://link1.html,\_blank\|Link 2,https://link2.html | Use comma as separator between text, URL and \(optional\) target; Use the pipe symbol \('\|'\) the as separator between hyperlinks |

Note that the order in which you create the output parameters doesn't affect how the modal elements are displayed.

#### Combo <a id="combo"></a>

In Leopard, a 'combo' refers to an output that contains more than one message type.

To display a combo using the simple syntax, you need to have at least two different message types added to the same output node.

## **Combo order**

If you want to order the message types in your combo in a specific way, you can add a special output parameter called `combo_order` to specify the order of the components. If not specified, the order will be random. The value of the 'combo\_order' parameter should contain the type names separated by the pipe symbol \('\|'\) in the order that you want them.

![](https://developers.artificial-solutions.com/user/pages/03.engine/02.teneo-web-chat/02.easy-message-type-creation-in-studio/twc_simple_output_param_combo.png)

