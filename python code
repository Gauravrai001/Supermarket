class Supermarket:
    def __init__(self):
        self.items = {
            "toffee": {"phase": 1, "price": 5},
            "biscuit": {"phase": 1, "price": 30},
            "bread": {"phase": 1, "price": 40},
            "milk": {"phase": 1, "price": 60},
            "vegetables": {"phase": 1, "price": 80},
            "fruits": {"phase": 1, "price": 120},
            "soap": {"phase": 2, "price": 25},
            "shampoo": {"phase": 2, "price": 180},
            "brush": {"phase": 2, "price": 35},
            "toothpaste": {"phase": 2, "price": 85},
            "facewash": {"phase": 2, "price": 150},
            "men shirt": {"phase": 3, "price": 800},
            "women shirt": {"phase": 3, "price": 750},
            "t shirt": {"phase": 3, "price": 500},
            "polos": {"phase": 3, "price": 600},
            "jean": {"phase": 3, "price": 1200},
            "men watch": {"phase": 4, "price": 1500},
            "women watch": {"phase": 4, "price": 2000},
            "children watch": {"phase": 4, "price": 800},
            "bracelets": {"phase": 4, "price": 300},
            "necklace": {"phase": 4, "price": 2500},
            "anklet": {"phase": 4, "price": 200},
            "ring": {"phase": 4, "price": 1500},
            "tv": {"phase": 5, "price": 25000},
            "washing machine": {"phase": 5, "price": 18000},
            "microwave": {"phase": 5, "price": 8000},
            "dishset": {"phase": 5, "price": 2000},
            "dishwasher": {"phase": 5, "price": 15000},
            "oven": {"phase": 5, "price": 12000}
        }

    def customer_cart(self):
        cart = []
        total = 0
        
        print("\n Shopping Cart")
        print("Enter items one by one. Type 'done' when finished.")
        
        while True:
            item = input("\nEnter item name: ").strip().lower()
            if item == 'done':
                break
            if item in self.items:
                try:
                    quantity = int(input(f"Enter quantity for {item}: "))
                    if quantity > 0:
                        item_total = self.items[item]['price'] * quantity
                        cart.append({
                            'name': item,
                            'phase': self.items[item]['phase'],
                            'price': self.items[item]['price'],
                            'quantity': quantity,
                            'total': item_total
                        })
                        total += item_total
                        print(f"Added {quantity} {item}(s)")
                    else:
                        print("Quantity must be greater than 0")
                except ValueError:
                    print("Please enter a valid number for quantity")
            else:
                print(f"Item '{item}' not available!")
        
        if cart:
            self.print_receipt(cart, total)
        else:
            print("Cart is empty!")

    def print_receipt(self, cart, total):
        print("\n" + "=" * 70)
        print("                      SUPERMARKET RECEIPT")
        print("=" * 70)
        print(f"{'S.No':<5} {'Item':<20} {'Phase':<8} {'Price':<10} {'Qty':<8} {'Total':<10}")
        print("-" * 70)
        
        for i, item in enumerate(cart, 1):
            print(f"{i:<5} {item['name'].title():<20} {item['phase']:<8} ₹{item['price']:<9} {item['quantity']:<8} ₹{item['total']:<9}")
        
        print("-" * 70)
        print(f"{'GRAND TOTAL:':<50} ₹{total}")
        print("=" * 70)

    def employee_menu(self):
        while True:
            print("\n" + "=" * 40)
            print("     EMPLOYEE MENU")
            print("=" * 40)
            print("1. Add Item")
            print("2. Remove Item")
            print("3. Update Price")
            print("4. View All Items")
            print("5. Back to Main Menu")
            
            choice = input("\nEnter choice: ").strip()
            
            if choice == '1':
                self.add_item()
            elif choice == '2':
                self.remove_item()
            elif choice == '3':
                self.update_price()
            elif choice == '4':
                self.view_all_items()
            elif choice == '5':
                break
            else:
                print("Invalid choice! Enter 1-5.")

    def add_item(self):
        name = input("Enter item name: ").strip().lower()
        if name in self.items:
            print("Item already exists!")
            return
        
        try:
            phase = int(input("Enter phase (1-5): "))
            price = int(input("Enter price: "))
            if 1 <= phase <= 5:
                self.items[name] = {"phase": phase, "price": price}
                print(f"Item '{name}' added successfully!")
            else:
                print("Phase must be between 1-5")
        except ValueError:
            print("Please enter valid numbers!")

    def remove_item(self):
        name = input("Enter item name to remove: ").strip().lower()
        if name in self.items:
            del self.items[name]
            print(f"Item '{name}' removed successfully!")
        else:
            print("Item not found!")

    def update_price(self):
        name = input("Enter item name: ").strip().lower()
        if name in self.items:
            try:
                new_price = int(input("Enter new price: "))
                self.items[name]['price'] = new_price
                print(f"Price updated for '{name}' to ₹{new_price}")
            except ValueError:
                print("Please enter a valid number!")
        else:
            print("Item not found!")

    def view_all_items(self):
        print("\nAll Items:")
        print("=" * 50)
        for item, info in self.items.items():
            print(f"{item:20} | Phase {info['phase']} | ₹{info['price']}")

    def start(self):
        while True:
            print("\n" + "=" * 40)
            print("     SUPERMARKET SYSTEM")
            print("=" * 40)
            print("1. Customer")
            print("2. Employee")
            print("3. Exit")
            
            user_type = input("\nAre you Customer or Employee? Enter 1 or 2: ").strip()
            
            if user_type == '1':
                self.customer_cart()
            elif user_type == '2':
                self.employee_menu()
            elif user_type == '3':
                print("Thank you for visiting!")
                break
            else:
                print("Invalid choice! Enter 1, 2 or 3.")

if __name__ == "__main__":
    market = Supermarket()
    market.start()
