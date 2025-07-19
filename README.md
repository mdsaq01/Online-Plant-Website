# Online-Plant-Website

Introduction:
Plant Paradise is an ecommerce website built to sell specialist houseplants and accessories to plant enthusiasts online. The project is a full stack web application built using the Django Framework. The key purpose of the project is to provide additional revenue and online awareness for the business and to allow site administrators to easily update and manage key site areas through the front end site and admin panel. This project was built as my submission for my milestone 4 project during the code institute Diploma in Software Development.

UX Design
This site has been built to cater to two key user groups:

Site Users - These are regular individuals, potential customers and collaborators visiting the site to view and buy products and discover information about the business.
Site Administrators - These are site owners, and stakeholders, who's primary focus is to manage content on the site, view, edit, create, and delete products, product categories, orders and other data types. While a dedicated admin site exists to enable full administration behaviour for the site, some key business procedures have been made accessible for site admins through the regular consumer facing site, to improve the user experience for site administrators.

Strategy
Site Owner Goals
As a site owner/stakeholder I want to:

Increase our online awareness and attract new users to our business.
Increase revenues via direct ecommerce sales.
Encourage existing customers to revisit the site to make additional purchases.
Manage products displayed on the site easily.
Improve my social media engagement.
Ideal User
The ideal user:

Is someone who owns a smartphone, tablet, computer or similar device.
Will have an interest in plants and other related products.
Is located in the same country as the business.
Is comfortable shopping online.
Has payment details saved on their device.
Is english speaking.
Likes to receive email updates from business's they are interested in.
Is active on social media.
User Stories As a new user:

I wish to immediately know the site's intention.
I need to be able to navigate between site pages and sections easily.
I wish to browse the sites product range.
I need to view detailed information on particular products of interest.
I want to purchase products directly through the site.
I want to be able to create an account to improve my experience for future sessions.
I want to access the business's social media profiles.
I need to be able to contact the business easily.
I want to register for an account. As an existing user:+
I need to be able to login to my account.
I need to view my past orders.
I need to be able to logout of my account. As a site admin:
I want to be able to manage site products.
I want to sort products into relevant groups.
I need to view, create, edit and delete products.
I need to view, create, edit and delete categories.
I need to view, create, edit and delete users.
I need to view, create, edit and delete orders.
I need to be able to assign additional site administrators.


Structure
The structure of the current project is as follows.

The project is cnmposed of the following applications. Each application is designed to sepparate concerns of specific functionality.

Apps:

Index - Handles rendering of homepage.
Products - Handles products and associated models.
Cart - Handles aggregation of products prior to order completion.
Checkout - Handles taking payment and creation of order models.
Contact - Handles user email contact to store owner.
Profile - Handles storage of individual user's order history and site preferences.
Social - Handles add, edit, read and delete of store's social media accounts.
In addition: Django-allauth is used to provide standard user account functionality such as login, logout, register, confirm email, forgot password etc....
Pages

Index Page - This is the primary landing page

Products Page - View of all products with search options to narrow donw search.

Single Product Page - A detailed view of a single product with an add to cart form and Edit and delete links for super users.

Add Product page - This is an admin only page which contains a form where a new product can be added. There are two outcomes for this page:

If the product has no variants, the product is created and the creator is directed to the detailed product page on completion.
If the wproduct has variants, the user is taken to the add variants page on completion.
Add Variant page - On this page a site admin can create, edit or delete product variants. On completion of this page, the user is brought to the single product view of the base product.

Add collection page - This allows site admins to create a product collection. This is so products can be grouped together for promotions or other reasons. (eg. Staff favourites, Sale etc...) Unfortunately due to time limit it was not within the scope of this project to display product collections once created.

Cart Page - This page displays the items that a user has added to their cart. There are two options:

A user can proceed to checkout using the checkout button.
A user can return back to products page using the alternate button.
Checkout page - This page has two sections, a order summary section and a checkout area which enables the user to enter their details, pay and complete their order.

Checkout success page - On successful checkout a user is brought to a success page which displays a concise summary of their order.

Contact Page - The contact form is a generic contact form which enables users to send a message to the business. On successful completion a success message is displayed and the email is sent to the site admin's elected email address.

Social page - This allows site admins to edit all social media ccounts displayed in the footer.

Social/add - This allows a site admin to add a new social profile from the options that have been stored in the database.

Social/add_icon - This allows a user to add a new icon and name to the available dropdowns.

Account page - This allows users to store their account details and to view their previous orders.

Sign In Page - This allows users with existing accounts to login and access their account.

Sign Out Page - This allows logged in users to logout of their account.

Signup Page - This allows new users to create an account.

Skeleton
Navigation Main Navigation: The primary navigation menu for this site is located in the header of the site on all pages. Hover and touch effects are used to indicate that navigation links are clickable and bright colors are chosen to ensure navigation links stand out from the surrounding background. Links to each important site page are included in the main navigation menu. On smaller devices the main navigation menu collapses and is denoted using the standard 'burger stack' toggler icon.

Login Section: The login section appears in the top right hand corner of the site header. The login area provides quick access to sign in, sign up and sign out site areas. When logged in a link to the user account can be found in this submenu. This is intended to encourage users to sign in to unlock additional site content and functionality and provides immediate feedback that the site is dynamic and can be interacted with by the user.

Footer Navigation: Links to imortant site pages and sections are mirrored in the site footer. This consistent footer navigation menu is displayed on all site pages to encourage users to explore additional pages once they have scrolled ot the bottom and read all content on the current page.

The footer also includes links to the businesses social media accounts to encourage further off-site interactions by users and to improve the business' credibility. As this is a fake business imagined for demonstration purposes, the social media links currently direct to the relevant social media home pages. To encourage user retention all links to external sites will open in a new tab/window.

Images as links: Images are used as links to improve navigation primarily on touch devices. This is utilised on the product category tiles on the homepage as well as the image cards on the products page.

Buttons as Links: Buttons and pseudo buttons are used throughout the site to boldly demonstrate a clickable site element. Clear labels and icons are used to indicate a buttons purpose or intended destination to improve first time learning and site useability. On the homepage buttons are used to bring users to the all products page. When used on forms, buttons are used for submission of information but redirects are also utilised upon form submission to transport the user to the page where the result of their input is displayed. This is to provide clear feedback to a user with the result of their input and to encourage ongoing interaction from users once one interaction has been completed.

Surface
Fonts
--hygge: 'Karla', sans-serif -> This is the Logo font.
--main: 'Source Sans Pro', sans-serif -> This font is used for the body text, larger passages of text and with heavier font weight it is also used for form labels and lesser headings.
--head: 'Staatliches', cursive; - This is used as the main Headin font. It's uppercase font style and bold font-weight is bold and striking and draws attention to key section headinds, alerts and other sections of informations that site users need to be made aware of.
Colors
A predominently green color palette was chosen for this project to allude to the site's main content (Plants). Three shades of green (light, mid, dark) are the basis of the color palette. These are offset with bright orange accent color used for buttons, links and other interactive elements. Bootstraps default green (success) and red (danger) color's are utilised in "yes"/"no", "do"/"don't" scenarios, where users are given multiple decisions or when feedback to a user input with a positive or negative connotation is provided. In such instances the traffic light (green means go, red means stop) metaphor is chosen rather than adhering to the color scheme in order to provide a better user experience and improved first-time-learning.

--grn: #33775d;
--grn-dark: #004b33;
--grn-light: #62a68a;

--orange: #ee9b00;
--sand: #cebfa8;
Throughout the site different shades of grey as well as white and black are used to outline form and container backgrounds and to provide appropriate contrast for sections of text in order to ensure ease of readability.

Images

Images have been used throughout the project to provide site context and to be visually appealing. As product images are not required to be dimensioned before upload care has been taken to ensure that images are scaled evenly across the site to provide a consistent and proffesional look and feel. Ideally in a real commercial application all product images would be studio shots with a plain white background. Unfortunately due to image useasge rights this was not possible for this project.

Icons

Icons have been used throughout this project as metaphors to reinforce heading and button meaning.


Technologies Used:
Languages
Html5
CSS3
Javascript
jQuery
Python
Libraries & Frameworks
Bootstrap - Used for quick protoyping of front end styles.
Django - Used for authentication, routing, serving dynamic html templates and interacting with the database.
Other
Fontawesome - Used to add icons throughout the project.
Google Fonts - Used to enable the use of additional fonts for the project.
Heroku - For app hosting and deployment.
Stripe - To enable customer payments for the project.
Amazon AWS S3 - Used to host images, files and other documents.
Postgress - Used to store site data.

Snapshots
![2](https://github.com/user-attachments/assets/8e08dfb3-d3b7-4f08-a6d2-0c795f279650)
![1](https://github.com/user-attachments/assets/c6e953a3-4c20-49cb-b478-87a6b3d8d09b)
![6](https://github.com/user-attachments/assets/96d68cc3-aef7-40dd-bf23-d26e400d5047)
![5](https://github.com/user-attachments/assets/d73b7bc3-9006-46aa-aae8-e3db97c74e60)
![4](https://github.com/user-attachments/assets/6edd2450-1f25-4e7a-a7bb-3620bf6b5acc)
![3](https://github.com/user-attachments/assets/6cadbf07-01ad-42de-8b0e-9e2c1f6f6fe7)


