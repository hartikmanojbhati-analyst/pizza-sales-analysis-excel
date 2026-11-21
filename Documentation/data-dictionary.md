# Data Dictionary – Pizza Sales Dataset

## 1. pizzas

| Column | Description |
|---|---|
| pizza_id | Unique identifier for each pizza size and type |
| pizza_type_id | Identifier connecting the pizza to its type |
| size | Pizza size (S, M, L, etc.) |
| price | Selling price of the pizza |

## 2. pizza_types

| Column | Description |
|---|---|
| pizza_type_id | Unique identifier for each pizza type |
| name | Full name of the pizza |
| category | Pizza category |
| ingredients | Ingredients used in the pizza |

## 3. orders

| Column | Description |
|---|---|
| order_id | Unique order identifier |
| date | Date on which the order was placed |
| time | Time at which the order was placed |

## 4. order_details

| Column | Description |
|---|---|
| order_details_id | Unique identifier for each order detail record |
| order_id | Identifier connecting the detail to an order |
| pizza_id | Identifier connecting the detail to a pizza |
| quantity | Number of pizzas ordered |

## Table Relationships

- `orders.order_id` connects to `order_details.order_id`.
- `pizzas.pizza_id` connects to `order_details.pizza_id`.
- `pizza_types.pizza_type_id` connects to `pizzas.pizza_type_id`.

These relationships connect order information with pizza products, categories, prices, and quantities.
