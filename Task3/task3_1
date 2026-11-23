import numpy as np
import matplotlib.pyplot as plt

# Physical parameters, we choose simple values to visualize the solution
L = 1.0         # rod length, x in [0, 1]
T = 1.0         # simulation time,  t in [0, 1]
alpha = 0.1     # thermal diffusivity constant

# Closed-form solution of 1D heat equation
def analytical_solution(x, t):
    return np.sin(np.pi * x / L) * np.exp(
        -alpha * (np.pi / L)**2 * t
    )
# Time points for evaluating the solution, we use 200 for a smooth curve
t = np.linspace(0, T, 200)

# Choose five positions along the first half of the rod
x_positions = [0.1, 0.2, 0.3, 0.4, 0.5]

plt.figure(figsize=(8, 5))

# Plot the temperature over time at each position
for x in x_positions:
    u = analytical_solution(x, t)
    plt.plot(t, u, label=f"x = {x:.1f}")

plt.xlabel("Time (t)")
plt.ylabel("Temperature u(x, t)")
plt.title("Closed-form Solution of the 1D Heat Equation")
plt.legend()
plt.grid(alpha=0.3)
plt.tight_layout()
plt.show()
