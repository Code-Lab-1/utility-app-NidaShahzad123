[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=9691294&assignment_repo_type=AssignmentRepo)

answer= str(input("Welcome to the vending machine,would you like to buy anything?(Yes/no)"))
while answer == "yes":
    column = " id: \t  \t price (dirhams):"
    products_in_stock = " ice cream:1 \t 3 \n chips:2 \t 2 \n juices:3 \t 3 \n chocolates:4 \t 4 \n soft drinks:5 \t 5 \n water:6 \t 2" 
    print (column)
    print (products_in_stock)
    wanted_item=int(input(" enter the id of the product you would like:"))
    if wanted_item==1:
        price=3
        print("please pay:",price)
    elif wanted_item==2:
        price=2
        print("please pay:",price)
    elif wanted_item==3:
        price=3
        print("please pay:",price)
    elif wanted_item==4:
        price=4
        print("please pay:",price)
    elif wanted_item==5:
        price=5
        print("please pay:",price)
    elif wanted_item==6:
        price=6
        print("please pay:",price)
    else :
        print("error")

    value=int(input("please enter the amount you would like to pay:"))
    if value > price:
        change= value-price
        print ("your change is ",change,"dirham,thank you for buying this product")
    elif value == price:
        print("thank you for buying this product")
    else:
        while value < price:
            print ("not enough money,please try again")
            value=int(input("please enter the amount you would like to pay:"))
            if value > price:
                change= value-price
                print ("your change is ",change,"dirham,thank you for buying this product")
            else:
                print("thank you for buying this product")
    answer=str(input("would you like anything else?"))
print("thank you for using this vending machine")

