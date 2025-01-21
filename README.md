Create a function named calculate_discount(price, discount_percent) that calculates the final price after applying a discount. The function should take the original price (price) and the discount percentage (discount_percent) as parameters. If the discount is 20% or higher, apply the discount; otherwise, return the original price.

def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount.

    Parameters:
    price (float): The original price of the item.
    discount_percent (float): The discount percentage to be applied.

    Returns:
    float: The final price after applying the discount, or the original price if the discount is less than 20%.
    """
    if discount_percent >= 20:
        final_price = price * (1 - discount_percent / 100)
        return round(final_price, 2)  # Optional: round to 2 decimal places
    else:
        return price

 Using the calculate_discount function, prompt the user to enter the original price of an item and the discount percentage. Print the final price after applying the discount, or if no discount was applied, print the original price.
 
def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount.

    Parameters:
    price (float): The original price of the item.
    discount_percent (float): The discount percentage to be applied.

    Returns:
    float: The final price after applying the discount, or the original price if the discount is less than 20%.
    """
    if discount_percent >= 20:
        final_price = price * (1 - discount_percent / 100)
        return round(final_price, 2)  # Round to 2 decimal places
    else:
        return price


# Prompt the user for inputs
try:
    original_price = float(input("Enter the original price of the item: "))
    discount_percentage = float(input("Enter the discount percentage: "))

    # Calculate and display the final price
    final_price = calculate_discount(original_price, discount_percentage)

    if discount_percentage >= 20:
        print(f"The final price after applying a {discount_percentage}% discount is: ${final_price:.2f}")
    else:
        print(f"No discount applied. The original price is: ${original_price:.2f}")

except ValueError:
    print("Invalid input. Please enter numerical values for the price and discount percentage.")

