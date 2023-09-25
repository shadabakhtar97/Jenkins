# Jenkins
### Learn Jenkins Deep Dive by Shadab Akhtar-9148627170

### Jenkins user details at the time of installation
![image](https://github.com/shadabakhtar97/Jenkins/assets/43212251/8f252dba-2c0e-4a78-a9ed-a00f66935fd8)



# Jenkins terminology such as "master" and "slave" nodes was commonly used. Jenkins is a popular open-source automation server that is often used for building, deploying, and automating software development tasks. However, it's worth noting that the Jenkins project has made some changes in terminology to promote more inclusive and neutral language, so you may want to use terms like "controller" and "agent" instead of "master" and "slave." Nevertheless, I'll provide an overview of how Jenkins integration between a master and slave (or controller and agent) works:

**1. Master/Controller:**
   - The Jenkins master/controller is the central server that manages and controls the entire Jenkins environment.
   - It's responsible for scheduling and managing builds, as well as storing configuration and job information.
   - The master serves the Jenkins web interface, allowing users to configure and monitor jobs, pipelines, and nodes.

**2. Slave/Agent:**
   - Jenkins slaves/agents are worker nodes that perform the actual build and automation tasks.
   - Slaves/agents are typically located on separate machines (physical or virtual) from the master/controller.
   - Agents can have different operating systems, software configurations, and tools installed to accommodate various build and test environments.

**Integration Steps:**

Here are the steps to integrate and configure Jenkins master and slave nodes:

**Step 1: Install Jenkins:**
   - First, you need to install Jenkins on the machine that will serve as your master/controller. You can download Jenkins from the official website and follow the installation instructions for your specific platform.

**Step 2: Install Java:**
   - Jenkins requires Java to run. Ensure that Java is installed on both the master and slave nodes.

**Step 3: Configure the Master:**
   - Access the Jenkins web interface by opening a web browser and navigating to the URL where Jenkins is running (usually http://localhost:8080 if running locally).
   - Install any necessary plugins for your build and deployment processes.
   - Configure global settings and security options as needed.

**Step 4: Set Up Slave Nodes:**
   - Install Jenkins agents (formerly known as slaves) on the machines you want to use as build agents.
   - For each agent, you'll need to download and run the Jenkins agent JAR file. You can do this via the command line, providing the master's URL and agent secret token for authentication.

**Step 5: Connect Agents to the Master:**
   - In the Jenkins web interface, go to "Manage Jenkins" > "Manage Nodes and Clouds."
   - Click "New Node" to add a new agent.
   - Specify the agent's name, select the appropriate type (e.g., Permanent Agent), and configure any necessary settings, such as labels or the number of executors.
   - Save the agent configuration.

**Step 6: Run Jobs on Slave Nodes:**
   - When configuring Jenkins jobs, you can specify which agent(s) should execute the job. You can do this by using labels or directly selecting a specific agent.

**Step 7: Monitor and Scale:**
   - Monitor the status and workload of your agents through the Jenkins web interface.
   - You can scale your Jenkins environment by adding more agents as needed to distribute the workload.

Remember that Jenkins has a rich ecosystem of plugins and integrations, so you can customize your setup to meet your specific requirements, including support for cloud-based agents.
