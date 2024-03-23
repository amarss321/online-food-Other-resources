-------------------------------------------------------------------------------------------------
create database restaurantdb;
show databases;
use  restaurantdb;
show tables;
CREATE TABLE Restaurant (
    id INT,
    name VARCHAR(255),
    address VARCHAR(255),
    city VARCHAR(255),
    restaurantDescription VARCHAR(255),
    PRIMARY KEY (id)
);

desc Restaurant;

INSERT INTO Restaurant (id, address, city, name, restaurantDescription) VALUES
(1, '123 Main Street', 'Anytown', 'The Hungry Hut', 'A cozy family-owned restaurant offering a diverse menu of international cuisines. From sizzling steaks to mouthwatering pasta dishes, we have something to satisfy every craving'),
(2, '456 Elm Avenue', 'Townsville', 'Spice Fusion', 'Experience the vibrant flavors of India at Spice Fusion. Our talented chefs blend traditional Indian spices with a modern twist, creating a culinary journey that will delight your taste buds'),
(3, '789 Oak Lane', 'Metropolis', 'Seafood Paradise', 'Indulge in the freshest catch of the day at Seafood Paradise. With a prime waterfront location, our restaurant offers a wide selection of seafood delicacies, prepared with a touch of coastal flair'),
(4, '321 Maple Road', 'Riverside', 'Tandoori Delight', 'Step into a slice of Italy at La Bella Trattoria. Our charming trattoria-style restaurant serves authentic Italian dishes made from scratch using the finest ingredients. Buon appetito!'),
(5, '987 Pine Street', 'Lakeside', 'The Green Garden', 'Embrace healthy eating at The Green Garden. Our vegetarian and vegan-friendly restaurant showcases the best of plant-based cuisine, with colorful salads, hearty bowls, and nutritious smoothies.'),
(6, '555 Chestnut Avenue', 'Belleview', 'Curry House', 'The Savory Bistro offers an exquisite dining experience with a focus on seasonal, locally sourced ingredients. Our talented chefs create artful plates that blend flavors from around the world, ensuring a memorable culinary adventure'),
(7, '222 Walnut Street', 'Harborview', 'Saffron Sizzlers', 'Sushi Haven invites you to savor the art of Japanese cuisine. Our skilled sushi chefs meticulously craft an array of fresh sushi rolls, sashimi, and delectable tempura, all served in a modern and elegant setting'),
(8, '777 Oakwood Drive', 'Summitville', 'Fireside Grill & Bar', 'Set against a rustic backdrop, Fireside Grill & Bar is the perfect spot for a cozy meal. Our menu features hearty grilled favorites, signature cocktails, and a warm ambiance that will make you feel right at home');
select * from Restaurant;

----------------------------------------------------------------------


create database foodcataloguedb;
use foodcataloguedb;
show tables;
CREATE TABLE FoodItem (
    id INT AUTO_INCREMENT PRIMARY KEY,
    itemName VARCHAR(255),
    itemDescription TEXT,
    isVeg BOOLEAN,
    price BIGINT,
    restaurantId INT,
    quantity INT DEFAULT 0
);INSERT INTO FoodItem (id, itemName, itemDescription, isVeg, price, restaurantId, quantity) VALUES
(1, 'Vegetable Biryani', 'Delicious vegetarian dish', true, 300, 1, 0),
(2, 'Butter Chicken', 'Succulent chicken in a creamy sauce', false, 310, 1, 0),
(3, 'Dal Tadka', 'Mouthwatering lentil curry', true, 350, 2, 0),
(4, 'Rogan Josh', 'Spicy and flavorful lamb curry', false, 315, 2, 0),
(5, 'Aloo Tikki', 'Crispy and spicy potato patties', true, 500, 3, 0),
(6, 'Tandoori Paneer Tikka', 'Paneer cubes marinated in tandoori spices', true, 900, 3, 0),
(7, 'Chicken Biryani', 'Fragrant and aromatic rice dish', false, 120, 4, 0),
(8, 'Vegetable Korma', 'Mixed vegetable curry', true, 110, 4, 0),
(9, 'Goan Prawn Curry', 'Spicy and tangy shrimp curry', false, 140, 5, 0),
(10, 'Naan', 'Fluffy Indian bread', true, 300, 5, 0),
(11, 'Chicken Tikka', 'Chicken marinated in yogurt and spices', false, 100, 6, 0),
(12, 'Kheer', 'Aromatic rice pudding', true, 600, 6, 0),
(13, 'Medu Vada', 'Savory lentil donuts', true, 400, 7, 0),
(14, 'Masala Dosa', 'Crispy crepe filled with spiced potatoes', false, 800, 7, 0),
(15, 'Mango Lassi', 'Refreshing yogurt-based drink', true, 500, 8, 0),
(16, 'Basket of Rotis', 'Assorted Indian bread basket', false, 700, 8, 0),
(17, 'Dal Fry', 'Lentils cooked with mixed spices', true, 350, 1, 0);
select * from FoodItem;



-------------------------------------------------------------------------------------------------------------------------------------

create database userdb;
use userdb;
CREATE TABLE User (
    userId INT AUTO_INCREMENT PRIMARY KEY,
    userName VARCHAR(255),
    userPassword VARCHAR(255),
    address VARCHAR(255),
    city VARCHAR(255)
);
show tables;
INSERT INTO User (userName, userPassword, address, city)
VALUES ('code', 'pass123', 'dummy add Whitefield', 'Banglore');
select * from User;



---------------------------------------------------------------------------------------------------------

