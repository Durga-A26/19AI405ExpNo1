<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: DURGA A </h3>
<h3>Register Number: 212224210005</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>Temperature from patients, Location.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>Prescribe medicine if the patient in a random has a fever.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>

```
import random
import time

def medicine_prescribing_agent(iterations=10):
    performance = 0
    current_room = 1

    for step in range(iterations):
        # Randomly generate patient temperature between 97 and 102
        temperature = round(random.uniform(97.0, 102.0), 1)

        print(f"\nStep {step + 1}:")
        print(f"Agent is in Room {current_room}")
        print(f"Patient Temperature: {temperature}°F")

        # Check if patient is unhealthy
        if temperature > 98.5:
            print("Patient is unhealthy → Prescribing medicine.")
            performance += 1
        else:
            print("Patient is healthy → No medicine needed.")

        # Move to next room
        current_room = 2 if current_room == 1 else 1
        performance -= 1
        print(f"Agent moves to Room {current_room}. (Performance penalty applied)")

    print(f"\nFinal Performance Score: {performance}")

# Run simulation
medicine_prescribing_age
```
# Output 
<img width="574" height="488" alt="Screenshot 2025-09-22 112452" src="https://github.com/user-attachments/assets/14af8336-7e33-480d-a0b8-6dde92cf337d" />
<img width="599" height="488" alt="Screenshot 2025-09-22 112533" src="https://github.com/user-attachments/assets/32266bba-4073-4395-8f4b-4ab98c4139d4" />
<img width="650" height="642" alt="Screenshot 2025-09-22 112602" src="https://github.com/user-attachments/assets/e0823b42-ca77-40b8-a746-2d7558e4ac8a" />




