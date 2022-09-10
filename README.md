# nodejs-orders
For MERN Web Development bootcamp
## Usage
- Fork the repo.
- Clone forked repo to your local machine.
- Resolve the the task.
- Push changes to the repo.
- Make a pull request.


## Idea
Small app receives an Http request from the client and returns list of orders and total price for all the orders as JSON response.

**Example**
```
{
    orders:[
        {
            customer:"Saif Marwan",
            address:{
                latitude:33.3266,
                longitude:44.3761
            },
            items:[
                {
                    name:"Milk",
                    count:1,
                    price:1.5,
                    total:1.5
                }
            ],
            total:1.5,
            discount:0,
            totalAfterDiscount:1.5
        },
        {
            customer:"Adel Ahmed",
            address:{
                latitude:33.3266,
                longitude:44.3761
            },
            items:[
                {
                    name:"Eggs",
                    count:30,
                    price:0.20,
                    total:6
                }
            ],
            total:6,
            discount:20,
            totalAfterDiscount:4.8
        }
    ],
    total:7.5
}
```
## Requirements
- Create Restful API with single endpoint:
    - Route Name: /orders
    - Method: GET
    - Returns a JSON response has orders list plus total price for all the orders.
- JSON response should match above schema as in the example.

## Orders File Description
`Orders.txt` file contains list of orders, each one belong to a customer, but to read the data from the file correctly you need to understand the dataset schema:
- comma character indicates the end of one order and starting the other.
- Order Block Details:
    - First line contains customer name.
    - Second line contains latitude and longitude as the address of the customer on the map.
    - Next lines are the items of the order.
    - Each item line contains (name, count, price, total price)
    - Last line contains (Total price for the order, discount percentage, Total price after the discount calculated).

- `Line 1:` Customer Name.
- `Line 2:` latitude longitude
- `Line 3:` itemName count price totalPrice
- `Line 4:` itemName count price totalPrice
- `Line 5:` itemName count price totalPrice
- `Line N - 1:` itemName count price totalPrice
- `Line N:` TotalPrice discount TotalPriceAfterDiscount


## Hints
- Comma seperate orders.
- Use space to split item details.
- Discount is percentage and not a constant value.
- Use `fs` to read data from orders text file.
- You may need to install `express.js` via npm.




