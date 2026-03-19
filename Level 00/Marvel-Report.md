# **Manjunath.D Aviation Level 0 Report**

## **Task 1: 3D Printing**

## Objective
Understand the working of a 3D printer and its components. Learn what an STL file is, how to slice it using Ultimaker or Creality Slicer, and understand key printer settings. Finally, get an STL file from the internet, slice it, and put it for print.

## Learnings and Outcomes

**Working Principle:** The printer used FDM (Fused Deposition Modeling) — PLA filament is melted through a heated nozzle and deposited layer by layer to build up the model.

**STL Files and Slicing:** An STL file defines the surface geometry of a 3D model as a mesh of triangles. Since the printer can't read STL files directly, a slicer (Ultimaker Cura) converts it into G-code — the actual instructions the printer follows.

**Key printer settings learned:**

| Setting | Recommended Value |
|---|---|
| Nozzle Temperature | 190°C – 220°C (PLA) |
| Bed Temperature | 50°C – 60°C |
| Printing Speed | 40 – 60 mm/s |
| Layer Cooling Fan | 100% (after first layer) |
| Infill Density | 10–20% (light) to 100% (solid) |
| Layer Height | 0.12mm (fine) to 0.3mm (fast) |

**Post-printing:** PLA parts can be sanded, painted with acrylics, or joined using superglue or epoxy.

## My Print

I downloaded the STL file for a **Batarang** from the internet, sliced it in Ultimaker Cura with the settings above, and put it for print.

![3D Printed Batarang](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/3D-printing-Batarang.jpeg?raw=true)




## **TASK 2: API**

## Objective
To learn what an API is, how it works, and to build a user interface (a web app) that makes calls to an external API to fetch and display information.

This task focuses on integrating theoretical API knowledge with practical implementation using modern web technologies.

---

## **Outcomes and Learnings**

## 1. Theoretical Understanding of APIs

An **API (Application Programming Interface)** is a bridge that allows two different software systems to communicate with each other.
 

A simple analogy is a **restaurant waiter**:

- The user (**client**) places an order (**request**).
- The waiter (**API**) carries the request to the kitchen (**server**).
- The kitchen prepares the food (**processes data**).
- The waiter brings the food (**response**) back to the user.

![working-of-API](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/working-of-API.png?raw=true)

The user does not need to know how the kitchen works internally. Similarly, developers use APIs without needing access to the internal architecture of the system providing the service.

In this task, **NASA’s Open API** acts as the data provider. My application acts as the client that sends requests and displays the received information.


## **2. Practical Application: NASA Space Explorer App 🚀**

I developed a simple **NASA Space Explorer web application** using the technologies listed below:

- **Python** – For writing the core application logic  
- **Streamlit** – For building the interactive web interface  
- **Requests Library** – To send HTTP requests and fetch data from NASA’s API  

The project utilizes **NASA’s free and public Open API (APOD – Astronomy Picture of the Day)** to fetch real-time space data.


## How it Works

1. The user selects a date and clicks on the **“Get Space Data”** button.
2. The application sends an **HTTP GET request** to the NASA APOD API using the selected date.
3. If valid data is found, the API sends back a **JSON response** containing:

- Title of the image  
- Image or video URL  
- Date  
- Explanation  

4. The application extracts this data and displays it neatly on the webpage.

If the request fails (invalid API key, wrong date, or network issue), an **error message** is displayed to the user.


## Preview
![API_previem](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/API_Preview.png?raw=true)


## **Pokédex API Project**

## Introduction

Before making the **NASA Space Explorer application**, I also worked on creating a **Pokedex API-based project**.

This project helped me understand how APIs function in real-world applications and gave me hands-on experience in retrieving, processing, and displaying data from an external source.

The Pokedex project served as a foundation for my NASA API project because it helped me understand the complete flow of:

- API communication  
- Backend logic  
- Frontend integration  


## **Step-by-Step Learning Process**

## Step 1: Understanding API Requests

Initially, I focused on understanding how to send an **HTTP GET request** to an external API.

I wrote a simple Python script that:

- Sent a request to the **PokeAPI**
- Printed the response
- Checked the **status code**

When the terminal displayed:

```
<Response [200]>
```
![API_to_check_if_its_OK](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/API_to_check_ifOK.png?raw=true)

**I understood that the API request was successful.**

---

## Step 2: Retrieving JSON Data

Next, I learned how to extract actual data using:

```python
response.json()
```

This converted the API response into a **Python dictionary**.

From there, I accessed:

- Name  
- ID  
- Height  
- Weight  
- Stats  
- Image URL  

![json](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/data_set_full_library%20.png?raw=true)
---

## Step 3: Extracting Specific Data

After retrieving the full JSON data, I modified the code to extract only the necessary fields and print them clearly.

For example:

- Name  
- ID  
- Height  
- Weight  

At this stage, my working backend code was around **30 lines** and successfully fetched structured Pokémon data.

![pokenon_deta](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Pokemon_Deta.png?raw=true)

## Step 4: Connecting Backend to Frontend

After the backend worked in the terminal, I created a simple frontend webpage using:

- **HTML**
- **CSS**

Then I connected it to my **Flask backend** so that:

- User enters Pokémon name
- Backend fetches data
- Webpage displays the result

Initially, the webpage was very simple with basic formatting.

![Pokemon_api](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Pokemon_API.png?raw=true)

## Step 5: Improving the UI – Pokedex Design

After the basic version worked, I tried to make the webpage look like an actual **Pokedex**.

With AI assistance, I:

- Designed a **red Pokedex-style card**
- Added styling
- Displayed Pokémon sprite image
- Improved button and layout design

Although it was not a perfect Pokedex replica, it significantly improved the visual appearance.

![Pokemon_api_2](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Pokemon_API_2.png?raw=true)


## **Key Learnings from the Pokedex Project**

- Understanding how **HTTP requests** work  
- Learning the meaning of **status codes**  
- Working with **JSON data structure**  
- Extracting **nested data**  
- Learning **backend–frontend integration**  




Using this foundation, I was able to build the **NASA Space Explorer App** more efficiently and with better understanding.


## **Overall Conclusion**

Through the development of both the **Pokedex API project** and the **NASA Space Explorer application**, I gained strong practical understanding of how APIs work in real-world systems.

The **Pokedex project** was my foundation. It helped me understand how to:

- Send HTTP GET requests  
- Interpret status codes  
- Retrieve JSON data  
- Extract specific fields  
- Connect backend logic with a frontend webpage  

Starting from a simple terminal response and gradually building a working web interface helped me understand the **complete API workflow**.

Overall, these two projects helped me understand the full cycle of **API-based application development**. More importantly, they helped me move from just learning APIs theoretically to actually building **functional, real-world applications** using them.

## **TASK 3: Working with GitHub**

## Objective

To familiarize myself with GitHub integrated workflows such as forking, cloning repositories, creating branches, committing changes, pushing updates, and creating pull requests.

---

## Introduction

Git is a distributed version control system that helps developers track changes in their code and collaborate efficiently. GitHub is a cloud platform that hosts Git repositories and provides additional collaboration tools such as pull requests, issues, and workflow integration.

In modern software development, contributors usually follow a fork-and-pull workflow, where changes are made in personal repositories and then submitted to the main project through pull requests. Through this task, I gained practical experience with this workflow and understood how GitHub enables collaborative development.

---

## Steps Followed

### 1. Cloning the Repository

The first step was cloning the repository to my local system using Git Bash. Cloning creates a local copy of the remote repository so that changes can be made locally.

The command used was:

```bash
git clone https://github.com/Manjunath-D-18/git-task-3.git
```

This downloaded the repository and created a folder named **git-task-3** in my system.

![image1](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/git_task_3_a.JPG?raw=true)

---

### 2. Navigating to the Repository and Checking Status

After cloning the repository, I navigated to the repository directory using the `cd` command.

```bash
cd git-task-3
```

I then used the following command to check the repository status:

```bash
git status
```

This confirmed that the repository was properly cloned and that the working tree was clean.

![image2](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/git_task_3_b.JPG?raw=true)

---

### 3. Creating a New Branch

To make modifications safely without affecting the main branch, I created a new branch called **fix-add-function**.

The command used was:

```bash
git checkout -b fix-add-function
```

This created and switched to a new branch where the required code changes were implemented.

---

### 4. Fixing the Code

The task required fixing an incorrect addition logic in the `add` function.

Originally, the function returned:

```python
number_a + number_b + 1
```

This produced incorrect results during testing.

I corrected the function so that it returns the correct value:

```python
number_a + number_b
```

This fixed the logical error in the program.

---

### 5. Committing the Changes

After fixing the code, I staged and committed the changes using the following commands:

```bash
git add fix-add-function.py
git commit -m "Fix incorrect addition logic in add function"
```

This recorded the modification in the repository history.

![image3](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Capture.JPG?raw=true)

---

### 6. Pushing the Branch to GitHub

After committing the changes locally, I pushed the branch to my GitHub repository using:

```bash
git push origin fix-add-function
```

This uploaded my branch and changes to GitHub so they could be reviewed.

---

### 7. Creating a Pull Request

After pushing the branch, I created a **Pull Request** to merge my changes into the main repository.


GitHub also confirmed that there were **no conflicts with the base branch**, meaning the changes could be merged safely.
![image4](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Pull_request_complete.JPG?raw=true)

## Outcomes and Learnings

Through this task, I learned several important concepts:

- Cloning repositories from GitHub  
- Navigating and working with local repositories  
- Creating and managing branches  
- Staging and committing code changes  
- Pushing changes to remote repositories  
- Creating pull requests for collaboration  


## **Task 4: Command Line on Ubuntu**

## Objective
Get familiar with the command line on Ubuntu by completing a series of subtasks involving file and directory management.

## Commands Used

| Command | What it does |
|---|---|
| `mkdir test` | Creates a folder named `test` |
| `cd test` | Navigates into the `test` folder |
| `touch empty.txt` | Creates a blank file without a text editor |
| `ls` | Lists all files and folders in the current directory |
| `mkdir B{0001..2600}` | Creates 2600 folders in one go, named B0001 through B2600 |
| `cat file1.txt file2.txt` | Concatenates two text files and displays the output in the terminal |

---

## Working

![Creating folders and listing files](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/unbuntu-1.png?raw=true)

![Concatenating files](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/ubuntu-2.png?raw=true)



## Outcomes and Learnings

- Got comfortable navigating the file system using `cd` and `ls`.
- Learned that `touch` creates a blank file without needing to open any editor.
- Used brace expansion (`{}`) to create 2600 numbered folders in a single command — much faster than doing it manually.
- Used `cat` to merge the contents of two text files and print them to the terminal.






## **Task 5: Build Your Own Brain — Linear Regression from Scratch**

## Objective
Implement Linear Regression from scratch using Python, compare it against scikit-learn's implementation, and evaluate both on the California Housing dataset using standard performance metrics.


## What I Did Differently

I used **Multiple Linear Regression (with Polynomial Expansion)**. Polynomial feature expansion was applied to capture non-linear relationships between variables,(example: income², income × house_age, income × rooms. . .) increasing the feature space from 8 to 44 features. 

Most implementations use the 8 raw features from the California Housing dataset directly. I went a step further and applied **Polynomial Features (degree=2)** before training, which expanded the feature set from **8 → 44 features**. 

Here's why that happens: with 8 original features, `PolynomialFeatures(degree=2)` generates all possible combinations like, each original feature squared (x₁², x₂². . .)(8 terms), every pair multiplied together (x₁×x₂, x₁×x₃. . .) (28 combinations), plus the original 8 (x₁, x₂, . . . x₈). That gives 44 features in total. The benefit is that the model can now detect non-linear patterns in the data, not just straight-line relationships , which is why my R² scores came out better than a plain linear approach.

All 44 features were then standardized using `StandardScaler` (formula: `z = (x - mean) / std`) before being fed into the model.

---

## Key Concepts I Learned

**Train/Test Split** — The dataset is split so the model trains on one portion and is evaluated on data it's never seen. This checks if the model actually generalizes, not just memorizes.

**Gradient Descent** — Instead of solving for weights mathematically, gradient descent starts with random weights and nudges them step by step in the direction that reduces error. The learning rate controls how big each step is — too large and it overshoots, too small and it takes forever.

**Why sklearn usually wins** — The scratch model uses gradient descent, which is iterative and sensitive to the learning rate and number of epochs. Sklearn's `LinearRegression` solves the weights directly using a mathematical method (least squares), so it's faster and finds the exact optimal solution.

**MSE, MAE, R²** — MSE penalizes large errors more (squared), MAE is just the average absolute error, and R² tells you how much of the variation in housing prices your model explains (closer to 1 is better).


## Results

| Metric | Scratch Model | Sklearn Model |
|--------|--------------|---------------|
| MSE | 0.5047 | 0.4643 |
| MAE | 0.5176 | 0.4670 |
| R² | 0.6148 | 0.6457 |

Sklearn came out ahead on all three metrics, which makes sense given how it solves for weights.


## Output Graphs

![Scratch Model: Actual vs Predicted](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Best_final_results_scratch(1).png?raw=true)


![Sklearn Model: Actual vs Predicted](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Best_final_results_sklearn.png?raw=true)

Both graphs show predictions clustering around the red dashed line , with the sklearn model looking slightly tighter.


## Honest Reflection

I understood only the basics. I haven't fully grasped machine learning yet. I understand the key ideas: why we split data, what the metrics mean, how gradient descent works conceptually, and why feature scaling matters. But there's a lot more depth to this than one task covers, and I did take help from AI to get the code working properly.

What I found genuinely interesting was seeing how adding polynomial features pushed the accuracy up, and how even a model I built from scratch could produce R² ~0.61 on real housing data. This task opened more questions than it answered, which I think is the point. I'd like to keep going deeper into this gradient descent alone could be a week of study.

This is what I've learned so far, and there's a lot more ground to cover.







## **Task 6: The Matrix Puzzle — Decode with NumPy & Reveal the Image**

## Objective

The objective of this task was to decode a scrambled matrix using NumPy operations and visualize the hidden image using Matplotlib. This exercise helped in understanding array manipulation techniques such as reshaping, rotating, and visualizing matrices.

## Procedure

### 1. Loading the Encoded Matrix

The scrambled matrix was first downloaded and loaded into Python using NumPy's `np.load()` function. This function reads `.npy` files and stores the numerical data inside a NumPy array for further processing.

At this stage, the data was simply a collection of numbers representing pixel values rather than a recognizable image.

```python
import numpy as np
matrix = np.load("/encoded_array.npy")
```

---

### 2. Inspecting the Matrix Structure

After loading the matrix, the structure of the data was examined using:

- `matrix.shape` – to determine the dimensions of the matrix  
- `matrix.size` – to determine the total number of elements in the matrix  

The output showed:

```
Shape: (200, 50)
Total elements: 10000
```


---

### 3. Reshaping the Matrix

One of the clues suggested reshaping the array into a square. Since the total number of elements was **10,000**, the square root was calculated:

```
√10000 = 100
```

Therefore, the matrix was reshaped into a **100 × 100 square matrix**. As the hint was it's likely a square!.



---

### 4. Correcting the Orientation

After reshaping, the image appeared incorrectly oriented. To fix this, the matrix was rotated using the NumPy function:

```python
matrix = np.rot90(matrix, k=-1)
```

This rotated the matrix **90 degrees clockwise**, correcting the orientation.

---

### 5. Visualizing the Image

Finally, the matrix was visualized using Matplotlib

The `imshow()` function interprets the numerical matrix as pixel values and displays it as an image. The grayscale color map (`cmap='gray'`) was used to display the image clearly.

After applying the correct transformations, the hidden image was successfully revealed.


## Observations

### Before Reshaping

The image appeared distorted because the matrix dimensions were incorrect.

![Distorted Image](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/task_6_matrix-img0.JPG?raw=true)

---

### After Decoding

After reshaping and correcting the orientation, the hidden image was revealed successfully.

![Decoded Image](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/task_6_matrix-img1.JPG?raw=true)


---

## Outcome and Learning

Through this exercise, the following basic concepts were learned:

- Loading numerical datasets using **NumPy**
- Inspecting array dimensions using **shape** and **size**
- Reshaping arrays into new dimensions
- Rotating matrices to correct orientation
- Visualizing numerical data as images using **Matplotlib**

The task demonstrated how raw numerical data can represent visual information and how proper manipulation of matrix structures can reveal hidden patterns or images.

Overall, this is quite an interesting topic. I plan to look into it more, specifically steganography.






## **TASK 7: Create a Portfolio Webpage**

## Objective
To create a responsive personal portfolio website that showcases information about myself, my interests, projects, and social media profiles. The website should be responsive and the source code should be pushed to a GitHub repository.

## Outcomes and Learnings

For this task, I created a simple personal portfolio website using basic **HTML and CSS**. I currently know only the basics of HTML and CSS, so the website is simple but structured clearly.
I learnt how ensured that the webpage is **responsive**, so it adjusts properly on different screen sizes.

This task helped me understand the basics of **structuring a webpage**.

![image4](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/portfolio.JPG?raw=true)

[**Visit Live Site**](https://manjunath-d-18.github.io/MARVEL---UVCE/) 


## **TASK 8: Writing Resource Article Using Markdown**

## Objective
To write a technical resource article using Markdown on a particular use case or application related to UAVs or aerospace technology. This task helps improve technical understanding and documentation skills using Markdown formatting.

## Outcomes and Learnings

For this task, I wrote a technical resource article titled **"Comparison: Rafale vs Sukhoi Su-57 and Which Is Better for India?"** using Markdown.

Through this task, I learned how to structure a technical article using Markdown syntax such as headings, lists, and formatting. Compared to HTML, Markdown was easier and more convenient for writing technical documentation.


**GitHub Repository Link:** [Rafale vs Sukhoi Su-57](https://github.com/Manjunath-D-18/MARVEL---UVCE/blob/main/Level%2000/Marvel__Task08.md)


## **TASK 9: TINKERCAD**

## Objective

Create a Tinkercad account and familiarize yourself with the application. Simulate a simple circuit using an ultrasonic sensor to estimate the distance between an obstacle and the sensor and display the results on the serial monitor. Create a radar system using an ultrasonic sensor and a servo motor to detect objects within a certain range.


## Introduction to Tinkercad

Tinkercad is an online platform that allows users to design 3D models and simulate electronic circuits. It provides a virtual environment where components such as Arduino boards, sensors, motors, and displays can be connected and tested without physical hardware.

## Components Used

- Arduino UNO  
- HC-SR04 Ultrasonic Sensor  
- Micro Servo Motor  
- Breadboard  
- Jumper Wires  


## Circuit Schematics & Connections

![circuit](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/tinkercad_circuit.JPG?raw=true)

## Outcomes and Learnings

## 1. Ultrasonic Distance Measurement System

In the first part of the task, I built a simple circuit using an ultrasonic sensor to measure the distance between the sensor and an object.

The ultrasonic sensor works on the **time-of-flight principle**:

- It emits a burst of high-frequency sound waves.  
- These waves travel through the air and reflect back after hitting an object.  
- The sensor measures the time taken for the echo to return.  

Using the known speed of sound, the distance is calculated.

### Formula Used

```
Distance = (T × C) / 2
```

Where:

- **T** is the time taken for the echo to return  
- **C** is the speed of sound (approximately **343 m/s**)  

The division by **2** accounts for the round-trip travel of the sound wave.

This system displayed the measured distance on the **Serial Monitor**, allowing real-time observation of how the sensor responds when the object position changes.

Through this, I understood how ultrasonic sensors are used in real-world applications such as:

- Obstacle detection  
- Parking sensors  
- Robotics  

---
  ![principle](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/U-S_working_principle.JPG?raw=true)


## Radar System Using Ultrasonic Sensor and Servo Motor

In the second part, I extended the basic system by integrating a **servo motor** to create a radar-like scanning mechanism.

Sweep Range: The servo is programmed to oscillate between 0° and 180° to ensure stable readings. The Arduino sends control signals that determine the angle of rotation.

### In this project:

- The servo motor continuously rotated from **0° to 180°** and back.  
- At each angle, the ultrasonic sensor measured the distance.  
- The angle and distance were displayed on both the **Serial Monitor**.  

This setup simulates the working of a **basic radar system**:

1. A signal is transmitted.  
2. The reflected signal is received.  
3. Distance is calculated.  
4. The object's position is determined based on **angle and range**.

It was particularly interesting to observe how the servo’s movement and sensor readings worked together to create a **scanning detection system**.


## Simulation Image

![sim-USS](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/tinkercad_1.JPG?raw=true)

## Conclusion

Through this activity, I got a basic idea of how sensors detect objects and how motors can control movement in small Arduino projects.I first built a simple setup to measure the distance of an object using the ultrasonic sensor. After that, I expanded it into a small radar-like system where the sensor moves using a servo motor and scans the area for objects.


## **TASK 10: Speed Control of DC Motor**

**Objective**: Understand how to control DC motors using the L298N motor driver with an Arduino UNO. The goal is to control the speed of a 5V DC motor using an H-Bridge L298N driver.

---

### Methodology

The circuit was wired as shown below:



#### L298N Motor Driver Connections

| L298N Motor Driver | Components |
|--------------------|------------|
| ENA                | ~10 of Arduino UNO |
| IN1                | 8th digital pin |
| IN2                | ~9 of Arduino UNO |
| GND                | -ve of 9V power supply |
| 12V                | +ve of 9V power supply |
| Output 1           | One terminal of motor |
| Output 2           | 2nd terminal of motor |


![DC Motor Diagram](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/dc-motor-2.png?raw=true)

---

### Outcomes & Learnings

#### L298N Motor Driver — How it works

![L298N Components](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/dc-motor-4.jpg.png?raw=true)

The L298N has two screw terminal blocks for Motor A and Motor B outputs, and a third block with three connections: GND, VCC (motor supply), and a 5V pin that can work as either input or output depending on the setup.

The board has 6 logic input pins:
- **ENA / ENB** — Enable pins for Motor A and Motor B. With a jumper, the motor runs at full speed. Connect a PWM signal here to vary the speed. Connect it to GND to stop the motor entirely.
- **IN1 / IN2** — Control the direction of Motor A (HIGH/LOW combinations set forward or reverse).
- **IN3 / IN4** — Same as above, but for Motor B.

> **Important:** ENA and ENB *must* connect to PWM-capable pins on the Arduino UNO (marked with `~`). Without PWM, speed control won't work.

---

#### Speed Control via PWM

Motor speed is controlled by adjusting the average voltage delivered to the motor. PWM (Pulse Width Modulation) does this by rapidly switching the signal ON and OFF. The longer the signal stays ON within each cycle (higher duty cycle), the higher the average voltage — and the faster the motor spins. It's a simple and efficient way to regulate speed without needing a variable resistor or analog circuitry.

![image](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/dc-motor-3.jpg?raw=true)


<video width="100%" controls>
  <source src="https://raw.githubusercontent.com/Manjunath-D-18/MARVEL-Level-0-Images/main/how%20does%20a%20pwm%20work%20on%20motor%20-%20Google%20Search%20-%20Google%20Chrome%202026-03-19%2015-40-14.mp4" type="video/mp4">
</video>

Click here for : [[dc-motor-video]](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/dc-motor-vid.mp4)


## **Task 11: LED Toggle Using ESP32**

## Objective
Learn the working of an ESP32 and create a standalone web server that controls an LED connected to its GPIOs. Use the Arduino IDE to code and upload the program to the ESP32.


## Components and Connections

**Components used:**
- ESP32 development board
- LED
- Resistor (220Ω)
- Jumper wires
- Breadboard

![Circuit Connections](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/esp-toggle-pic-2.png?raw=true)


## Procedure

Added the ESP32 board to the Arduino IDE, fed in the required code with my mobile hotspot credentials, and set the baud rate to 115200. After successful compilation, the Serial Monitor displayed an IP address — pasted that into the browser and toggled the LED from the webpage.


## Outcomes and Learnings

- Got familiar with the ESP32 microcontroller and how to configure the Arduino IDE for it.
- Learned how the ESP32 can host a standalone web server without any external backend.
- Successfully toggled an LED via a browser using HTTP requests to the GPIO pins.

## Working

![Task in Action](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/esp-toggle-pic-1.jpeg?raw=true)

 **🎥**[**Click here to view the video**](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/esp-toggle-vid.mp4)

## **Task 12: Soldering Prerequisites**

## Objective
Learn about soldering equipment such as soldering iron, solder, flux, and soldering wick, and perform basic soldering on a perf board — for example, a simple LED circuit — under the supervision of a coordinator.


## Procedure

Got familiar with each piece of equipment first ,what it does and how to handle it safely. Then inserted the LED leads through the correct holes on the perf board, making sure the polarity was right. Heated the soldering iron, held it at the junction of the lead and the copper pad, and fed solder wire into the joint. After the solder cooled, checked the connections and powered the circuit with a 9V battery to verify it worked.


## Outcomes and Learnings

- Got hands-on with soldering equipment and learned how to use each tool correctly.
- Learned the proper technique for making clean solder joints and what a bad one looks like.
- Successfully soldered an LED circuit on a perf board and lit it up with a battery.
- Practiced desoldering with a wick to remove excess solder.


![Soldering in progress](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/soldering-2.jpeg?raw=true)


## **Task 13: Design a 555 Astable Multivibrator**

## Objective
Design a 555 IC astable multivibrator with a duty cycle of 60%, assemble it on a breadboard, and observe the output waveform on a Digital Storage Oscilloscope (DSO).


## Components Used

| Component | Value |
|---|---|
| 555 IC Timer | — |
| Capacitor C1 | 0.001 µF |
| Capacitor C2 (bypass) | 0.01 µF | 
| Resistor R1 | 4.7 kΩ | 
| Resistor R2 | 10 kΩ | 
| Power Supply | 5V | 

---

## Circuit Diagram

![Basic Astable 555 Oscillator Circuit](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Basic%20Astable%20555%20Oscillator%20Circuit.png?raw=true)


---

## Duty Cycle Calculation

The duty cycle for an astable 555 circuit is given by:

![Duty Cycle Formula](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/555-Duty-Cycle-formula.webp?raw=true)

Using R1 = 10 kΩ and R2 = 20 kΩ:

**Duty Cycle = (R1 + R2) / (R1 + 2×R2) × 100 = (4.7 + 10) / (4.7 + 20) × 100 = 59.5%**

## Oscilloscope Output

![Oscilloscope Output](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/555-timer-Oscilloscope%20Output.jpeg?raw=true)

## Internal Structure of the 555 IC
 
![555 IC Internal Circuit](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/555%20IC%20Internal%20Circuit.png?raw=true)

*Internal block diagram of the 555 IC — the voltage divider sets reference levels at 1/3 Vcc and 2/3 Vcc, the two comparators monitor the capacitor voltage, and the SR flip-flop controls the output and discharge transistor.*
 
![SR Flip-Flop Truth Table](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/555%20SR%20Flip-Flop%20Truth%20Table.png?raw=true)

*SR Flip-Flop truth table — S=1,R=0 sets the output HIGH; S=0,R=1 resets it LOW; both 0 holds the previous state; both 1 is an invalid condition.*
 
![SR Flip-Flop Working Example](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/555%20SR%20Flip-Flop%20Working%20Example.png?raw=true)

*SR Flip-Flop in action — when R=0, S=1 the output Q̄=0 (set), and when R=1, S=0 the output Q̄=1 (reset).*
 

## Outcomes and Learnings

- Got familiar with the 555 IC timer — its pin configuration, internal structure, and the three modes (astable, monostable, bistable).
- Learned how the capacitor's charge/discharge cycle between 1/3 Vcc and 2/3 Vcc produces the square wave output.
- Understood the role of the internal SR flip-flop in controlling the output state.
- Calculated R1 and R2 values to hit a target 60% duty cycle.
- Observed duty cycle of approximately **59.5%** on the Oscilloscope, which is very close to the theoretical 60%.

## **Task 14: Active Participation**

## KAGADA 2025 – Technical Project Presentation

I secured **2nd place** in the Technical Project Presentation at KAGADA 2025.

My project was an **IoT-Based Flood Monitoring and Alert System using ESP32** a real-time flood monitoring system that uses an ESP32 microcontroller paired with other ultrasonic sensor to continuously track rising water levels and trigger alerts when they exceed a set threshold.

Below is the image of my certificate:

![KAGADA 2025](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/KAGADA_2025.jpg?raw=true)

## **Task 15: Introduction to VR**

## What is VR?

Virtual Reality is a technology that places you inside a completely computer-generated environment through a head-mounted display. You're fully cut off from the real world — what you see, and sometimes hear, is entirely artificial. Controllers in both hands let you interact with that environment.

---

## VR vs AR

The core difference: VR replaces your reality, AR adds to it.

| Feature | VR | AR |
|---|---|---|
| Environment | Fully digital, real world blocked out | Digital overlaid on the real world |
| Hardware | Headsets (Meta Quest 3, HTC Vive) + controllers | Phones, tablets, AR glasses (Apple Vision Pro, Xreal) |
| User Presence | You're "somewhere else" | You're still in the room |
| Tracking |  tracks movement in 3D space | SLAM — anchors digital objects to real surfaces |

---

## Technology Stack

**Unity** is the go-to engine for cross-platform VR/AR development — lightweight, flexible, and works across most headsets.

**Unreal Engine 5** is the choice when visuals matter most. Its Lumen and Nanite systems push near-photorealistic rendering in real time, which is why it's used for high-end simulations and cinematic VR.

## Indian Companies in XR


- **AjnaLens** — builds their own AR/VR headsets (AjnaXR)
- **CHRP-India** — known for VR safety training in industrial environments like mines
- **TCS** — offers XR-as-a-Service, building metaverse environments for large enterprises

## Trends

Mixed Reality (blending VR and AR) is where most hardware is heading. Standalone headsets are getting lighter and cheaper. On the software side, AI-generated environments and spatial computing are the big bets right now.

## Personal Experience

I did try out the VR headset at the MARVEL lab ,it was genuinely fun. Played a few games and it was way more immersive than I expected.


# ***✈️ Aviation Domain Specific Tasks***

## **Task 1: History of Aviation**
Objective:
Explore the theory of aviation and different types of planes. Gain a brief understanding of the history of aviation and the pioneers of the field.

## Learning:
The history of aviation spans more than 2,000 years,moving from simple kites to advanced jet engines technology we use today. Below is the flowchart detailing this journey.

![Flow-chart](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/aviation_flowchart_final.png?raw=true)

## **TASK 2 (Aviation): Introduction to Flight Simulators**
Objective: To learn manual controls, stability handling, and motor mixing using a drone simulator.

## ***Learning:***

## 1. Channels in a Transmitter (Tx)
Channels are discrete signal pathways assigned to individual controls.
- The TX16S MKII offers 16 channels.
- Primary Channels: A minimum of 4 channels is required for **basic flight:** Throttle (L), Yaw (L), Pitch (R), and Roll (R).
- Additional Channels: Channels 5–16 are used for "extra" features like arming the drone, toggling flight modes. (Angle/Acro)
- Greater the channels, the more features and controls the Tx offers to the user.

## 2. Understanding the Euler angles (Pitch, Roll & Yaw):

### Understanding the basic Four Forces of Flight

![Four Forces of Flight](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Aviation%20(basic%20Four%20Forces).png?raw=true)

In level flight, lift cancels weight and thrust is greater then drag. This applies to both fixed-wing aircraft and quadcopters.


### 6 Degrees of Freedom & Along 3 Axes

![6 Degrees of Freedom](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Aviation(%20Axes%20of%20rotation).png?raw=true)

  *Pitch, Roll, and Yaw — all intersecting at the Center of Gravity*

An aircraft has 6 degrees of freedom: 3 translational (move forward/back, left/right, up/down) and 3 rotational. The primary flight controls only directly govern the 3 rotational axes:

- **Pitch** — nose up/down (right stick up/down)
- **Roll** — tilt left/right (right stick left/right)
- **Yaw** — rotate on vertical axis (left stick left/right)
- **Throttle** — altitude (left stick up/down)


### X-Configuration (Net Torque = 0)

![Hover Physics X-Configuration](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Aviation(X-cinfuguration).png?raw=true)
*Counter-rotating motor pairs cancel reaction torques, achieving a stable hover with Net Torque = 0*

In an X-configuration quadcopter, diagonal motor pairs spin in the same direction. Two spin CW and two spin CCW. Since every spinning propeller generates a reaction torque in the opposite direction, the four motors cancel each other out — the drone hovers without spinning.

---

###  Motor Mixing: Pitch and Roll

![Executing Pitch and Roll](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Aviation(Roll-Pitch).png?raw=true)

**To Pitch forward:** Front motors slow down, rear motors speed up. The imbalance tilts the nose down.

**To Roll right:** Left motors speed up, right motors slow down. The chassis rolls without changing total thrust.

In both cases, because we adjust one CW and one CCW motor equally, the net yaw torque stays at zero — the drone pitches or rolls without spinning.

---

### Yaw: Spinning Without Tilting

![Yaw Enigma](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Aviation%20(YAW).png?raw=true)


Yaw is handled differently. To spin the drone clockwise, the CW motor pair slows down and the CCW pair speeds up (or vice versa). The total thrust across all four motors stays the same, so the drone rotates flat without climbing or dropping. 


### Motor Mixing Summary Table

| Maneuver | Motor 1 (FR) | Motor 2 (BL) | Motor 3 (FL) | Motor 4 (BR) |
|---|---|---|---|---|
| Throttle (Up) | + | + | + | + |
| Pitch (Forward) | − | + | − | + |
| Roll (Right) | − | + | + | − |
| Yaw (CW) | − | − | + | + |

*(+ = speed increase, − = speed decrease)*


### Quadcopter vs Fixed-Wing

![Synthesis: Actuating 3D Space](https://github.com/Manjunath-D-18/MARVEL-Level-0-Images/blob/main/Aviation%20(Quadcopter%20vs%20Fixed-Wing).png?raw=true)



## Simulator Practice: Angle Mode(self-leveling)

Flying in Angle Mode means if you release the Throttle sticks, the drone self-levels. This lets you focus on learning the flight path without fighting instability.I performed the flight maneuvers in the simulator **On the MARVEL Open Day**, in the MARVEL Lab, and it was a pretty fun experience to see the concepts of motor mixing and stability handling applied in a Real setting.

## Outcomes and Learnings

- Understood all four primary RC channels (Throttle, Yaw, Pitch, Roll) and which stick controls which.
- Learned how the X-configuration uses counter-rotating motor pairs to cancel reaction torques at hover.
- Understood motor mixing logic — how individual motor speed changes produce pitch, roll, and yaw without interfering with each other.
- Got comfortable with Angle mode flight in the simulator.



## **TASK 3 (Aviation): Flying the Airblock Drone**

## Objective
Learn about the Airblock drone and fly it along a specified path under coordinator supervision.


## About the Airblock

The Airblock is a modular hexacopter drone by Makeblock, built from magnetized Expanded Polypropylene (EPP) foam blocks that snap together without any tools. It's controlled via the **MakeBlock app** over Bluetooth. The same blocks can be rearranged into four configurations — Drone, Hovercraft, Triangle, and Spider.

The below image shows the different variations of Airblock Drone:

![drone](https://www.robot-advance.com/userfiles/www.robot-advance.com/images/montage%20du%20drone%20airblock%20makeblock.gif)


| Parameter | Details |
|---|---|
| Material | EPP / PP foam |
| Battery | 7.4V, 700mAh |
| Flight Time | ~6 minutes |
| Control Range | 10 meters |
| Sensors | 6-axis gyroscope, Ultrasonic, Barometer |
| Control App | MakeBlock (Bluetooth) |

---


