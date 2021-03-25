# Fifteen Group: Developers Take-Home Test

## Introduction
We intend this test to take in the region of 4-5 hours once you have familiarised yourself with the requirements. However, do not worry if you cannot complete all tasks in this amount of time. If you do not complete all tasks prior to submission, please consider including pseudo code or documentation explaining the approaches you would have taken and estimates for remaining time. 

With this in mind, commit often, with good messages that explain your workflow. Please do not submit your full solution as a single commit. 

Feel free to use any front-end scaffolding and technology you’re comfortable with to speed up setup. We recommend a 1st-party starter kit like [Breeze or Jetstream](https://laravel.com/docs/8.x/starter-kits), but this is open to you. Do not worry about design (unless you want to show off your skills!)—the UI needs only be functional.

Please also include tests wherever you feel they are appropriate.

At least 24 hours before your Stage 2 interview, share with us a repository on GitHub or Bitbucket, with your implementation of the tasks (whether complete or incomplete).

## Stage 1
Set up a new installation of Laravel as you would if you were starting a new long-term project. Copy over the provided table migrations, factories, and seeders. For each resource type, define models with relationships that will work with the tables and factories. Run the migrations and seeders to validate that they work as expected, without changing the factories at this stage. 

Once your project is set up, provide a brief outline of how to get the project running locally in your chosen development environment, in a README in the repository.

At the end of this stage, add a `stage-1-complete` tag to your last commit.

## Stage 2
Implement CRUD pages allowing orders to be recorded against a contact and modified after creation. Each order must store a unique reference number and one or more order items.

Each order item must contain a product name and a price. It is fine for these values to be typed in as free text at the point of adding the order item—there is no need to create a separate “product” list to reference.

On the orders index, display both the company name and the name of the contact for each order, using relationships. Be mindful that the page should remain performant even when displaying thousands of records (the page should default to displaying at least 500 orders, if pagination is used).

From this point forwards you may modify the factories if desired.

At the end of this stage, add a `stage-2-complete` tag to your last commit.

## Stage 3
Add sorting to the orders management index screen. It must be possible to sort by both the number of items in the order, as well as the total monetary value of the order.

Lastly, add functionality to automatically send a notification to all users 30 minutes after an order is created, with the content “A new order has been created for `{$contactName}` at `{$companyName}`”.

The notification should display as a banner somewhere on screen. Once it has been displayed to the user once, they should not see it again. There is no need to check for new notifications asynchronously—it is fine to simply display a notification on page load if one is available.

At the end of this stage, add a `stage-3-complete` tag to your final commit.
