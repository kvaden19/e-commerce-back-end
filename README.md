# e-commerce-back-end

## TODOs:

### Models: 

- Set up the following models:
* `Product`
  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment
  * `product_name`
    * String.
    * Doesn't allow null values
  * `price`
    * Decimal.
    * Doesn't allow null values.
    * Validates that the value is a decimal
  * `stock`
    * Integer.
    * Doesn't allow null values.
    * Set a default value of `10`.
    * Validates that the value is numeric
  * `category_id`
    * Integer.
    * References the `Category` model's `id`
* `Tag`
  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.
  * `tag_name`
    * String.
* `ProductTag`
  * `id`
    * Integer.
    * Doesn't allow null values.
    * Set as primary key.
    * Uses auto increment.
  * `product_id`
    * Integer.
    * References the `Product` model's `id`.
  * `tag_id`
    * Integer.
    * References the `Tag` model's `id`.




- Set up associations:
* `Product` belongs to `Category`, and `Category` has many `Product` models, as a category can have multiple products but a product can only belong to one category.
* `Product` belongs to many `Tag` models, and `Tag` belongs to many `Product` models. Allow products to have multiple tags and tags to have many products by using the `ProductTag` through model.
> **Hint:** Make sure you set up foreign key relationships that match the column we created in the respective models.


### Routes:
- WHEN I open API GET routes in Insomnia Core for categories, products, or tags THEN the data for each of these routes is displayed in a formatted JSON
- WHEN I test API POST, PUT, and DELETE routes in Insomnia Core THEN I am able to successfully create, update, and delete data in my database

### Testing:
- WHEN I enter schema and seed commands (npm run seed) THEN a development database is created and is seeded with test data- 
- WHEN I enter the command to invoke the application THEN my server is started and the Sequelize models are synced to the MySQL database

