#HTML Chapter 1: “Structure” (pp.12-39)#
###In all kinds of documents, structure is very important in helping readers to understand the messages you are trying to convey and to navigate around the document.
So, in order to learn how to write web pages, it is very important to understand how to structure documents.
For example, newspapers show the same stories in print as they do on websites; you can apply for insurance over the web; and stores have online catalogs and e-commerce facilities.###

###Insurance forms often have headings for different sections, and each section contains a list of questions with areas for you to fill in details or checkboxes to tick.
The structure is very similar when a news story is viewed online (although it may also feature audio or video).
If the article is a long piece, there may be subheadings that split the story into separate sections or quotes from those involved.###

##Structuring Word 
Documents##

###For example, a document might start with a large heading, followed by an introduction or the most important information.
The different styles for the document, such as different levels of heading, are shown in the drop down box.###

##TML Describes
the Structure 
of Pages##

To describe the structure of a web page, we add code to the words we want to appear on the page.
In the browser window you can see a web page that features exactly the same content as the Word document you met on the page 18.
You can see the HTML code for this page below.





##Body, Head & Title##
##body##
###Everything inside this element is shown inside the main browser window.
You met the element in the first example we created.###
##head##
##This contains information about the page (rather than information that is shown within the main part of the browser window that is highlighted in blue on the opposite page).##

###The HyperText part refers to the fact that HTML allows you to create links that allow visitors to move from one page to another quickly and easily. (17)
A markup language allows you to annotate text, and these annotations provide additional meaning to the contents of a document. (16)
If you think of a web page, we add code around the original text we want to display and the browser then uses the code to display the page correctly. (13)### 

##HTML Chapter 8: “Extra Markup” (p.176-199)##

##Extra 
Markup##
####At this point, we have covered the main tags that fit nicely into groups and sections. (7)
In this chapter, we will focus on some helpful topics that are not easily grouped together. (5)####

The Evolution of HTML

####Since the web was first created, there have 
been several different versions of HTML.####

####With the exception of a few elements added in HTML5 (which have been highlighted), the elements you have seen in this book were all available in HTML 4. (24)
Where you should be particularly aware of browsers not supporting certain features, I have made a note of this (as you have seen with some of the HTML5 elements introduced in the Forms chapter — and as you will see in the CSS chapters). (24)
Each new version was designed to be an improvement on the last (with new elements and attributes added and older code removed). (20)
Although HTML 4 had some presentational elements to control the appearance of pages, authors are not recommended to use them any more. (20)
(Examples include the element for centering content on a page, for controlling the appearance of text, and to put a line through the text — all of these can be achieved with CSS instead.) In 1998, a language called XML was published. (19)
Since HTML was the most widely used markup language around, it was decided that HTML 4 should be reformulated to follow the rules of XML and it was renamed XHTML. (18)
Not all web users, however, have the latest browsers installed on their computers, which means that not everyone will be able to view all of the latest features and markup. (17)####

HTML5
Released 2000

####The transitional version of XHTML was created because it allowed authors to continue to follow older practices (with a less strict syntax) and use some of the elements and attributes that were going to be removed from future versions of HTML. (44)
In order to help web page authors move to this new syntax, two main flavors of XHTML 1.0 were created: ● Strict XHTML 1.0, where authors had to follow the rules to the letter ● Transitional XHTML 1.0, where authors could still use presentational elements (such as and ). 
There was also a third version of XHTML 1.0 called XHTML 1.0 Frameset, which allowed web page authors to partition a browser window into several "frames," each of which would hold a different HTML page. 
At the time of writing, the HTML5 specification had not been completed, but the major browser makers had started to implement many of the new features, and web page authors were rapidly adopting the new markup. ####

##DOCTYPEs##
####Because there have been several versions of HTML, each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using (although browsers usually display the page even if it is not included).#### 

##comment in html##

####If you want to add a comment to your code that will not be visible in the user's browser, you can add the text between these characters: It is a good idea to add comments to your code because, no matter how familiar you are with the page at the time of writing it, when you come back to it later (or if someone else needs to look at the code), comments will make it much easier to understand. (35)
Although comments are not visible to users in the main browser window, they can be viewed by anyone who looks at the source code behind the page. (26)####

##ID Attribute##

####For example, you might want to assign one paragraph within the page (perhaps a paragraph containing a pull quote) a different style than all of the other paragraphs. 
As you will see when you come to look at CSS in the next section, giving an element a unique identity allows you to style it differently than any other instance of the same element on the page. 
If you go on to learn about JavaScript (a language that allows you to add interactivity to your pages), id attributes can be used to allow the script to work with that particular element. 
It is used to uniquely identify that element from other elements on the page. (17)####

In this example, CSS has been applied to make elements with a class attribute whose value is important uppercase, and elements with a class attribute whose value is admittance red.
For example, you might have some paragraphs of text that contain information that is more important than others and want to distinguish these elements, or you might want to differentiate between links that point to other pages on your own site and links that point to external sites. 
In the example on the left, key paragraphs have a class attribute whose value is important. 
HTML chapter-08/class-attribute.html Class Attribute By default, using these attributes does not affect the presentation of an element.

##inline element##

####Some elements will always 
appear to continue on the 
same line as their neighbouring 
elements. These are known as 
inline elements.
Examples of inline elements are 
<a>, <b>, <em>, and <img>####

##Grouping Text & 
Elements In a Block## <div>


###element should occupy on the screen and change the appearance of all the elements contained within it. 
element allows you to group a set of elements together in one block-level box. 
element will start on a new line, but other than this it will make no difference to the presentation of the page.### 

##Grouping Text & 
Elements Inline## <span>

###Contain a number of inline elements The most common reason why people use elements is so that they can control the appearance of the content of these elements using CSS. (14)
Contain a section of text where there is no other suitable element to differentiate it from its surrounding text 2.### (11)

###Frames### <iframe>
The content of the iframe can be any html page (either located on the same server or anywhere else on the web). (14)
One common use of iframes (that you may have seen on various websites) is to embed a Google Map into a page. (12)
An iframe is like a little window that has been cut into your page — and in that window you can see another page. (11)

src
###The src attribute specifies the 
URL of the page to show in the 
frame.
height
The height attribute specifies 
the height of the iframe in pixels.
width
The width attribute specifies 
the width of the iframe in pixels###

##scrolling##

###This is important if the page inside the iframe is larger than the space you have allowed for it (using the height and width attributes).###

##frameborder##
###In HTML 4 and XHTML, it indicates whether the frame should have a border or not. 
A value of 0 indicates that no border should be shown###

##seamless##

###The seamless attribute (like some other new HTML5 attributes) does not need a value, but you will often see authors give it a value of seamless. (17)
In HTML5, a new attribute called seamless can be applied to an iframe where scrollbars are not desired.###

##Information About your pages##

<meta>
###In the first line of the example on the opposite page, you can see a element where the name attribute indicates an intention to specify a description for the page. (25)
(If the page is time sensitive, it can be set to expire.) The element is an empty element so it does not have a closing tag. (19)
It is not visible to users but fulfills a number of purposes such as telling search engines about your page, who created it, and whether or not it is time sensitive,
The value of the name attribute 
can be anything you want it to 
be. Some defined values for this 
attribute that are commonly### 
used are
description:
###keywords This contains a list of comma separated words that a user might search on to find the page. (21)
This description is commonly used by search engines to understand what the page is about and should be a maximum of 155 characters. (19)
robots This indicates whether search engines should add this page to their search results or not###

Escape Characters

There are some characters that are used in 
and reserved by HTML code. (For example, the 
left and right angled brackets.)

###Therefore, if you want these characters to appear on your page you need to use what are termed "escape" characters (also known as escape codes or entity references). (24)
When using escape characters, it is important to check the page in your browser to ensure that the correct symbol shows up. (21)
There are also special codes that can be used to show symbols such as copyright and trademark, currency symbols, mathematical characters, and some punctuation marks###

Online Extra
You can find a more complete 
list of escape codes in the 
tools section of the website 
accompanying this book.

DOCTYPES tell browsers which version of HTML you 
are using.
X You can add comments to your code between the 
<!-- and --> markers.
X The id and class attributes allow you to identify 
particular elements.
X The <div> and <span> elements allow you to group 
block-level and inline elements together.
X <iframes> cut windows into your web pages through 
which other pages can be displayed.
X The <meta> tag allows you to supply all kinds of 
information about your web page.
X Escape characters are used to include special 
characters in your pages such as <, >, and ©

##HTML Chapter 17: “HTML5 Layout” (pp.428-451)##

###HTML5 is introducing a new set of 
elements that help define the structure of 
a page.###

###element ● How to ensure older browsers recognize these elements As with all HTML5 and CSS3 content, its usage is still subject to change but it is already widely being used by web developers and it is likely that you will want to use them. (18)
They are covered here (rather than with the other HTML elements you met earlier in the book) because you'll find it easier to understand how they can be used now that you have seen how CSS can control the layout a page.###

##Traditional HTML layouts##

###For a long time, web page authors used <div> elements to group 
together related elements on the page (such as the elements that form a 
header, an article, footer or sidebar). Authors used class or id attributes 
to indicate the role of the <div> element in the structure of the page.##3

There is a side bar on the right hand side (perhaps featuring a search option, links to other recent articles, other sections of the site, or even ads).

New Html5 Layout elemnent 5

###HTML5 introduces a new set of elements that allow you to divide up the parts of a page. (9)
They are still subject to change, but that has not stopped many web page authors using them already. (7)
The names of these elements indicate the kind of content you will find in them###

###For example, the header sits inside a new element, the navigation in a element, and the articles are in individual elements. (16)
Similarly, search engines might place more weight on the content in an element than that in the or elements. (16)
For example, screen reader software might allow users to ignore headers and footers and get straight to the content. (15)
The point of creating these new elements is so that web page authors can use them to help describe the structure of the page###

Headers & Footers
<header> <footer>
###Each individual and element can also have its own and elements to hold the header or footer information for that section within the page. (25)
The element can therefore be used to contain the title and date of each individual post, and the might contain links to share the article on social networking sites. (23)
The and elements can be used for: ● The main header or footer that appears at the top or bottom of every page on the site. (19)
For example, on a page with several blog posts, each individual post can be thought of as a separate section###

Navigation 
<nav>

##At the time of writing, some of the developers that were already using HTML5 decided to use the element for the links that appear at the bottom of every page (links to things like privacy policy, terms and conditions and accessibility information). (22)
Going back to our blog example, if you wanted to finish an article with links to related blog posts, these would not be counted as major navigational blocks and therefore should not sit inside a element.##

Articles <Article>


##For example, a blog post might live inside one element and each comment on the article could live inside its own child element. (19)
If a page contains several articles (or even summaries of several articles), then each individual article would live inside its own element. (18)
This could be an individual article or blog entry, a comment or forum post, or any other independent piece of content##

Aside 

##When the element is used inside an element, it should contain information that is related to the article but not essential to its overall meaning. (14)
When the element is used outside of an element, it acts as a container for content that is related to the entire page.##

Sections
<section>


##For example, on a homepage there may be several elements to contain different sections of the page, such as latest news, top products, and newsletter signup. (18)
Because the element groups related items together, it may contain several distinct elements that have a common theme or purpose. (18)
The element should not be used as a wrapper for the entire page (unless the page only contains one distinct piece of content). (16)
Alternatively, if you have a page with a long article, the element can be used to split the article up into separate sections##

Heading Groups
<hgroup>

###The purpose of the element is to group together a set of one or more through elements so that they are treated as one single heading. (12)
element (using an attribute to indicate that it is a subheading). (10)
When it was first proposed by the people developing HTML5, there were some complaints and it was withdrawn from the HTML5 proposals. (10)
For example, the element could be used to contain both a title inside an element and a subtitle within an element.### 

##Figures
<figure> <figcaption>##

###It is important to note that the article should still make sense if the content of the element were moved (to another part of the page, or even to a different page altogether)The element should also contain a element which provides a text decription for the content of the element###

Sectioning Elements
<div>

###element will remain an important way to group together related elements, because you should not be using these new elements that you have just met for purposes other than those explicitly stated. (15)
Some people have asked why there is no element to contain the main part of a page.###

##Linking Around 
Block-Level Elements##

###HTML5 allows web page authors to place an element around a block level element that contains child elements###

##Helping Older 
Browsers Understand##

###In order to style these elements using earlier versions of IE, you need to use a simple JavaScript known as the HTML5 shiv or HTML5 shim. (25)
Also, IE9 was the first version of Internet Explorer to allow CSS rules to be associated with these new HTML5 layout elements.###

##Example
HTML5 LAYOUT##

###The courses are grouped together inside a element that has a class attribute whose value is courses (to distinguish it from other elements on the page). (22)
Each of the courses lives inside an element, and use the and elements to contain an image.###

summary 


The new HTML5 elements indicate the purpose of different parts of a web page and help to describe its structure. 
X Older browsers that do not understand HTML5 elements need to be told which elements are block-level elements

HTML Chapter 18: “Process & Design” (pp.452-475)

This section discusses a process that 
you can use when you are creating a new 
website.

It looks at who might be visiting your site and how to ensure the pages feature the information those visitors need. (10)
It also covers some key aspects of design theory to help you create professional looking sites.

Who is the Site For?

####Every website should be designed for the 
target audience—not just for yourself or the 
site owner. It is therefore very important to 
understand who your target audience is.
If your site sells light bulbs, even though most people using a computer probably use light bulbs, they are not likely to order them from someone in a different country###

Why People Visit
YOUR Website

###Now that you know who your visitors are, you need to consider why they are coming
To help determine why people are coming to your website, there are two basic categories of questions you can ask: 1: The first attempts to discover the underlying motivations for why visitors come to the site###

What Your Visitors are 
Trying to Achieve

###It is unlikely that you will be able to list every reason why someone visits your site but you are looking for key tasks and motivations###
Ivy is a picture editor and wants to look at a photographer's site to see examples of his work before deciding whether to commission him. 
Gordon bought a tennis racquet several years ago; now he wants to purchase one from your site for his girlfriend. 
Jasper had a bad experience staying in a hotel when visiting Sydney, Australia, and wants to make a complaint. 
Molly has read about your new doggy daycare service in the press and wants to find out whether it would be suitable for her to use. 
Ayo hopes to study architecture and wants to learn more about a new course that is being offered###

###What Information 
Your Visitors Need###

###You know who is coming to your site and why 
they are coming, so now you need to work out 
what information they need in order to achieve 
their goals quickly and effectively.###

###By ensuring that you provide the information that your visitors are looking for, they will consider your site more relevant to them. (12)
You may want to offer additional supporting information that you think they might find helpful. (11)
Look at each of the reasons why people will be visiting your site and determine what they need to achieve their goals. (9)
You can prioritize levels of information from key points down to non-essential or background information###

###Therefore, you will have more opportunity to tell them any extra information that you think would be helpful to them (or to expose them to other products and services you want to promote)###

How Often People Will 
Visit Your Site

###Some sites benefit from being updated more frequently than others
A website about fashion trends will need to change a lot more frequently than one that is promoting a service that people do not buy regularly (such as domestic plumbing or double glazing)You will often find that some parts of a site will benefit from being updated more frequently than others.
It can often be helpful to set a schedule for when a site will be updated (rather than doing it on an ad hoc basis)###

##Site Maps##

###Now that you know what needs to appear 
on your site, you can start to organize the 
information into sections or pages
This involves placing each piece of information that a visitor might need to know on a separate piece of paper and then organizing the related information into groups
Additionally, if the site is large and is compartmentalized into sections, each section might require its own section homepage to link to all of the information within it.###

###It is worth noting that the site owner might organize information in a way that is different to what the public expects.
It is important to reflect the public's understanding of the subject (rather than just the site owner's understanding of it).###

WireFrames
###A wireframe is a simple sketch of the key information that needs to go on each page of a site.###

###The wireframes make design easier because you know what information needs to appear on which page before considering how the the page should look.
This involves sketching or shading areas where each element of the page will go (such as the logo, primary navigation, headings and main bodies of text, user logins etc).
It should focus on what information needs to be on each page and create a visual hierarchy to indicate the most important parts of each page.
By creating a wireframe you can ensure that all of the information that needs to be on a page is included.
A lot of designers will take the elements that need to appear on each page and start by creating wireframes.
It enables the client to ensure the site has all the functions and information it needs to offer###

##Getting your message 
across using design##

###Organizing and prioritizing information on a page helps users understand its importance and what order to read it in.###

content
Web pages often have a lot of information to communicate.

###(Key messages would not stand out.) By making parts of the page look distinct from surrounding content, designers draw attention to (or away from) those items.
Designers create something known as a visual hierarchy to help users focus on the key messages that will draw people's attention, and then guide them to subsequent messages.###

###By presenting certain types of information in a similar visual style (such as using the same style for all buttons or all links), users will learn to associate that style with a particular type of content.###


##visual hierarchy Attention is immediately drawn to a picture that shows the service this company offers and a headline to explain it.##

###Further down are three distinct groups showing you what the services do, the costs involved and some of the services' users.
Under this is the information that introduces the company's services.
The four points (at the bottom left of the screenshot) are all presented in a similar manner with consistent headings and icons###

##Visual hierarchy##

SIZE Larger elements will grab users' attention first.
color Brighter sections tend to draw users' attention first.
Foreground and background color can draw attention to key messages.
##Style An element may be the same size and color as surrounding content but have a different style applied to it to make it stand out##
##It is created by adding visual contrast between the items being displayed.
Visual hierarchy refers to the order in which your eyes perceive what they see##

grouping and
Similarity
It is created by adding visual contrast between the items being displayed.
Visual hierarchy refers to the order in which your eyes perceive what they see.

###Consistency In this example each book review has a consistent style for the book titles, author names, and purchasing links.
Headings Giving a chunk of information a heading clearly tells the user whether or not the content of the grouping is relevant to them.
Having read just one of the blocks it is possible to infer the meaning of the other items in this box that follow the same style.
It also helps users of screen readers, as users often have the option to hear the headings on the page.###

It's important to understand who your target audience 
is, why they would come to your site, what information 
they want to find and when they are likely to return.
X Site maps allow you to plan the structure of a site.
X Wireframes allow you to organize the information that 
will need to go on each page.
X Design is about communication. Visual hierarchy helps 
visitors understand what you are trying to tell them.
X You can differentiate between pieces of information 
using size, color, and style. 
X You can use grouping and similarity to help simplify 
the information you present

ABc of programing

For example, hotel handbooks may contain steps to follow in different scenarios such as when a guest checks in, when a room needs to be tidied, when a fire alarm goes off, and so forth.
G THE ABC OF PROGRAMMING HANDBOOKS Large companies often provide handbooks for new employees that contain procedures to follow in certain situations.
(You would not want someone going through every single step in the entire handbook while you were waiting to check in.) Similarly, in a complex script, the browser might use only a subset of the code available at any given time.
If the brakes now pass the test, the mechanic knows they are fixed and can move onto the next test.
You could compare scripts to any of the following: RECIPES By following the instructions in a recipe, one-by-one in the order set out, cooks can create a dish they have never made before.

A script is a series of instructions that the computer 
can follow in order to achieve a goal. 
Each time the script runs, it might only use a subset of 
all the instructions. 
Computers approach tasks in a different way than 
humans, so your instructions must let the computer 
solve the task prggrammatically. 
To approach writing a script, break down your goal into 
a series of tasks and then work out each step needed 
to complete that task (a flowchart can help).

##css files The CSS enhances the HTML page with rules that state how the HTML content is presented (backgrounds, borders, box dimensions, colors, fonts, etc.). Programmers often refer to this as a separation of concerns.
Where possible, aim to keep the three languages in separate files, with the HTML page linking to CSS and JavaScript files.##
















































