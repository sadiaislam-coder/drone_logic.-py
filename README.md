# Simple Drone Cost and Distance Tool
# Purpose: To check if a delivery is possible based on battery and distance.

def drone_delivery_check(distance, battery_min):
    # A drone usually takes 2 minutes per kilometer
    required_time = distance * 2
    
    print("--- Delivery Report ---")
    print(f"Distance to cover: {distance} km")
    print(f"Battery available: {battery_min} minutes")
    
    # Keeping 10 minutes extra as a safety buffer
    if battery_min > (required_time + 10):
        return "Result: Possible. The cost is within budget."
    else:
        return "Result: Not possible. Battery is too low for this distance."

# Testing the tool
print(drone_delivery_check(12, 40))
