1. Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.
PROTIP: use the inspector to learn the dimensions of the current profile image and use a placeholder image service such as Place Bear to get an image of the same size.

ANSWER:
profileImage = document.querySelector('img.profile-image')
profileImage.src = 'https://cdn.shopify.com/s/files/1/0715/2011/products/1_040510c9-1cf4-4201-9b26-6010a5b3bee3_large.jpeg?v=1442898778'

*********---------*********
2. Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

ANSWER:
cloudImage = document.querySelector('.portfolio-image > img')
cloudImage.src = 'https://i.pinimg.com/736x/06/34/43/063443a1daf229d5326c61b4c9ec1ad5--good-morning-america-goats.jpg'

*********---------*********
3. Select the heading that says "Panda the Bear" and change it to your own name.

ANSWER:
nameHead = document.querySelector('h1.highlight')
nameHead.innerText = "Sarah The Costa"

*********---------*********
4. Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

ANSWER:
titleInfo = document.querySelector('#employment > h3')
titleInfo.innerText = "Experience"

*********---------*********
5. Change the colour of the body.

ANSWER:
pageBackground = document.querySelector('body')
pageBackground.style.backgroundColor = '#1B4F72'

*********---------*********
6. Change the colour of each element using the highlight class. Use a for loop to do this.

ANSWER:
highLight = document.querySelectorAll('.highlight')
highLight.forEach(function(element){element.style.backgroundColor = '#979A9A'})

*********---------*********
7. Change the font family of the h1 to 'monospace'.

ANSWER:
nameHead.style.fontFamily = 'monospace'

*********---------*********
8. Find a way to select the round icons in the sidebar and then change their colour.

ANSWER:
iconBackground = document.querySelectorAll('a.action-icon-bg')
iconBackground.forEach(function(element){element.style.backgroundColor = '#1B4F72'})

*********---------*********
9. Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

ANSWER:
contactName = document.querySelector('#name')
contactName.placeholder = "Identify Yourself"

*********---------*********
10. Change the placeholder attribute of the message field to "state your business".

ANSWER:
contactMsg = document.querySelector('#message')
contactMsg.placeholder = "State Your Business"

*********---------*********
11. Give the name field a "value" attribute of "your nemesis".

ANSWER:
contactName.value = "Your Nemesis"

*********---------*********
12. Change the value attribute of the email field to "koalathebear@gmail.com".

ANSWER:
contactEmail = document.querySelector('#email')
contactEmail.value = 'koalathebear@gmail.com'

*********---------*********
13. Change the value of the submit button on the contact form to "En garde!".

ANSWER:
submitButton = document.querySelector('#submit')
submitButton.value = 'En garde!'

*********---------*********
14. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).

ANSWER:
submitButton.disabled = true

*********---------*********
15. We should help Panda protect their privacy by erasing their personal details from the sidebar.

ANSWER:
bioInfo = document.querySelector('.bio-info')
bioInfoList = document.querySelectorAll('.bio-info-item')
bioInfoList.forEach(function(element){bioInfo.removeChild(element)})



PART 2 ***********************
1. That drawing of Pikachu is really cute. Let’s duplicate it using cloneNode() and insert it at the bottom of the .portfolio-container using insertAdjacentHTML() or appendChild().

ANSWER:
var pikachu = document.querySelector('#right-image > img')
pikachu.cloneNode(true);
var portfolioContainer = document.querySelector('.portfolio-container')
portfolioContainer.append(pikaClone)

*********---------*********
2. Wow, that was so satisfying I think we should do it 10 more times. Use a for loop to help you do this.

ANSWER:
for(var i = 0; i < 10; i++){ var pikaClone = pikachu.cloneNode(true); portfolioContainer.append(pikaClone) };

*********---------*********
3. Let’s add a message about when the page was last updated. We'll do this by appending a new <li> element to the <ul> in the sidebar (you might need to refresh the page to bring back the list items that we emptied out earlier).

ANSWER:
var newItem = document.createElement('li')
var lastUpdated = document.lastModified
var spanOne = document.createElement('span')
var spanTwo = document.createElement('span')
spanOne.className = 'bio-info-title'
spanTwo.className = 'bio-info-value'
newItem.append(spanOne)
newItem.append(spanTwo)
spanOne.innerText = "Last Updated"
spanTwo.innerText = lastUpdated
bioInfo.append(newItem)
