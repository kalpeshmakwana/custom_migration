# custom_migration

This application is for creating custom migraiotn in the django.

Migration is mianly for keeping data model up-to-date.All this is managed by table named "django_migrations" which gets created when we first apply the migrations.

We then need to build our custom migration. It needs to have 6 steps :
    1. Create the new Customer model in the database, with all the necessary fields.
    2. Create a nullable customer foreign key on Order
    3. Set the Order fields to transfer as nullable
    4. Transfer the data from the Order model to the Customer model.
    5. Set the new customer field on Order as non-nullable
    6. Remove the old fields from the Order model.