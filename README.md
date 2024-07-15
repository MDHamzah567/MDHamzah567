import matplotlib.pyplot as plt
import numpy as np

def quadratic_model(time):
    # Hard-coded coefficients for the quadratic equation
    a = float(input("Enter the value a: "))
    b = int(input("Enter the value b: "))
    c = int(input("Enter the value c: "))

    # Quadratic equation representing temperature change
    temperature = a * (time ** 2) + b * time + c
    return temperature

def main():
    # Time values from 0 to 10 (for example)
    time_values = np.linespace(0, 10, 50)

    # Calculate temperatures using hard-coded coefficients
    temperature_hardcoded = quadratic_model(time_values)

    # Plot the results
    plt.plot(time_values, temperature_hardcoded, label='Hard-coded Coefficients')
    plt.xlabel('Time')
    plt.ylabel('Temperature')
    plt.legend()
    plt.title('Weather Modeling with Quadratic Equation (Hard-coded Coefficients)')
    plt.show()

if _name_ == "_main_":
  main()
  
