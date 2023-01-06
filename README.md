[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=9691294&assignment_repo_type=AssignmentRepo)

products_in_stock = [{"product_id": 1,
"product_name":"ice cream",
"product_price":3,},
{"product_id":2,
"product_name":"chips",
"product_price":2,},
{"product_id":3,
"product_name":"juices",
"product_price":3,},
{"product_id":4,
"product_name":"chocolates",
"product_price":4,},
{"product_id":5,
"product_name":"soft drinks",
"product_price":5,},
{"product_id":6,
"product_name":"water",
"product_price":2,},]

is_check = False 
product = ''

while is_check == False:
    print("Hello, Welcome to the vending machine")
    for i in products_in_stock:
        print(f"Product name: {i['product_name']} - Price: {i['product_price']} - ID: {i['product_id']}")
    question = int(input("Press the ID of the product you will like to have: "))
    for i in products_in_stock:
        if question == i["product_id"]:
            product = i
    if product == '':
        print("INCORRECT ID")
    else:
        print(f"Significant, {product['product_name']}would charge you {product['product_price']} dirhams")

        value  = int(input(f"Press {product['product_price']} dirhams to acquire:"))
        if value == product['product_price']:
            print(f"Thanks for purchasing the item, here is your {product['product_name']}")
        else:
            print(f"Kindly, enter only {product['product_price']} dirhams")

    question = input("To vacate the machine enter v and to resume purchasing enter anything:")
    if question == 'r':
        is_check = False
    else:
        is_check = True
    print('')



