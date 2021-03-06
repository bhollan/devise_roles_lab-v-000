# Devise with Roles

## Learning Objectives

  1. Explain the use of role-based authorization with Devise.
  2. Design a set of roles to model a forum with different permission levels.
  3. Set up Devise roles to implement such a model.

## Data Model

In this lab, we're going to make a simple discussion board.

We'll have a Post model, and three user roles: user, vip, and admin.

* Users can read anyone's Posts, and create, read, update, and delete their own posts.
* VIPs can do everything a User can do, and update and delete other users posts.
* Admins can do anything to any Post and any other User.

## Instructions

Provided is a Rails skeleton with the Devise gem installed.

1. Run the migrations. A basic User model and migrations have been set up for you as part of the devise install.
2. Add roles to the user model. The specs will tell you what roles are expected of the model.
3. Add authentication and authorization filters to your users controller. Ensure that only administrators can update or destroy users.
4. Run `rails generate devise:views` to generate the views.

Once you've reached this point, all the specs should be passing. For the next part, we'll create a `Post` model, which has different permissions for different user roles.

You will need to write specs for the `Post` model and controller. You can reference the feature and model specs for the `Users` controller to see how to write these.

1. Create a `Post` model and migration. Posts have an owner and content.
2. Create a posts controller. Ensure that it enforces the following requirements:
  - Posts can be created by any user
  - Anyone can read any post
  - Users can edit or delete Posts they own
  - VIPs can edit or delete anyone's Posts
  - Admins can do anything to any post.
3. Write views for your posts.
4. Try it out!

## References

* [Devise]

[Devise]: https://github.com/plataformatec/devise
