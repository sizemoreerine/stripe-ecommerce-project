# Erin Sizemore's Stripe Written Project
# 11/07/19

OVERVIEW

This is an e-commerce website for selling coffee mugs called Duke's Coffee Mugs World. This website displays product items and enables users to add and remove these items from their cart while also specifying the quantity of each. 

When users add an item to their cart, they see an order summary page that enables them to update item quantity, delete items, continue shopping, or proceed to checkout. When they checkout, users specify their shipping and billing addresses,redeem an optional promo code, and choose the Stripe payment option. 

As they continue to checkout, a payment page displays enabling the user to enter credit card information, choose to use a default saved card, and then submit their payment. The user can also choose to save the card they used as their default card. Upon successful payment, a confirmation message displays.

HOW IT WAS BUILT

This website was built by starting with code available in GitHub: github.com/justdjango/django-ecommerce. It uses a Django framework, Python language, a Bootstrap template, allauth authentication, Stripe iFrames/forms, Stripe error handling code, and Stripe APIs.

STRIPE APIs

The "Create a Charge" Stripe API was used: stripe.Charge.create. 

HOW I APPROACHED THIS

I needed to find a framework to start this project. I haven't tackled an entire project where I am doing all the coding, so I needed to find a solid starting point. I found a YouTube video that walked through creating an e-commerce website using Django, Python, and Stripe APIs. The video also provided a link to the completed project in GitHub. I now had my starting point.

WHY I PICKED PYTHON AND DJANGO

Most of my familiarity with web develpment coding is with PHP, Python, and JavaScript. I chose Python and Django because Django is a framework built for Python. Django provides command-line untilities (makemigrations, migrate) to create database tables automatically. This gave me the freedom from having to use MySQL or another DB solution. Django also provides an admin interface that is very intuitive and customizable, via admin.py. Django also claims to be fast and scalable.

HOW THIS PROJECT COULD BE EXTENDED

Refunds: Currently, an admin can mark an order as "refund requested" or "refund granted." However, there is not functionality to actually apply a refund to a customer's credit card. I would use the "Create a Refund" Stripe API stripe.Refund.create and the stripe_charge_id variable to create a new refund for an order and refund the charge previously created. Using this API, funds could be refunded to the credit card originally charged on the order.

End User Account Management: Currently, only an admin can change user information such as first name, last name, and email address. End users could have the ability to manage their account if functionality was added to the website to enable them to do that. They could manage personal information, orders, request refunds, or look at an order history.
