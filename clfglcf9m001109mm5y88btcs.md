---
title: "DevOps90DaysChallenge"
datePublished: Mon Mar 20 2023 08:54:51 GMT+0000 (Coordinated Universal Time)
cuid: clfglcf9m001109mm5y88btcs
slug: devops90dayschallenge-1-1-1-1-1-1-1-1-1-1
tags: python, python3, devops, python-beginner, python-for-devops

---

# Hi 👋there,

# Now we are on the Day 15 task

# **Basics of Python(Libraries for DevOps)**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679302666556/632ece4c-cfc4-4bfd-b25d-647d4238b22f.png align="center")

<mark>Checkout the below link for Day 15 task:</mark>

[https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day15/tasks.md](https://github.com/LondheShubham153/90DaysOfDevOps/blob/master/2023/day15/tasks.md)

# **Reading JSON and YAML in Python**

As a DevOps Engineer, you should be able to parse files, be it txt, json, yaml, etc.

You should know what libraries one should use in Python for DevOps.

Python has numerous libraries like `os`, `sys`, `json`, `yaml` etc that a DevOps Engineer uses in day-to-day tasks.

# **Tasks**

**Create a Dictionary in Python and write it to a json File.**

JSON stands for JavaScript Object Notation. It means that a script (executable) file which is made of text in a programming language, is used to store and transfer the data.

![5 Ways to Convert Dictionary to JSON in Python | FavTutor](https://favtutor.com/resources/images/uploads/Dict_to_JSON_Python.png align="left")

**Function Used:**

* json.dumps()
    
* json.dump()
    

Here we will be using **json.dumps()**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679163807152/51a9dc27-2421-4a40-a8b8-1214e031aa5d.png align="center")

**OUTPUT:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679163906180/9b59ab55-6b14-4d04-a0c7-c1e8345440d0.png align="center")

***Read a JSON file*** `services.json` ***kept in this folder and print the service names of every cloud service provider.***

output:

aws: ec2 azure: VM gcp: compute engine

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679169452865/6cb7b44a-dc5a-4f75-a1ac-92009662fbae.png align="center")

**OUTPUT:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679169510372/b7d5b78a-ab40-469b-9d4d-fafb3557adc0.png align="center")

Here we first read the JSON file, on the left side of the image, kept in this folder and parse by using the loads() function then we print this file data by print function.

***Read the YAML file using python, file*** `services. yaml` ***and read the contents to convert YAML to JSON.***

[PyYAML](https://pyyaml.org/) is a YAML parser and emitter for Python.

To install pyYAML module use command.

We need to use PyYAML module’s `yaml.load()` function. This function parses and converts a YAML object to a Python dictionary (`dict` object).

This process is known as Deserializing YAML into a Python.

* First, we write the file data to the Yaml file using the dump() function & Then we fetch all data from Yaml by using the safe\_load function.
    
* File data is available in the YAML file as we see on the left side of the image.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679302136987/19d476ec-d6ec-4645-be14-2ad5a2523682.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679302184624/2971d5db-87d1-44df-ac0b-1a269765a8a3.png align="center")

* Then we converted the Yaml file to a JSON file and formatted the JSON file can be seen on the right side image as a result.
    

**Please, feel free to drop any questions in the comments below. I would be happy to answer them.**

**If you find this post helpful😊🙂, please follow and click the heart❤❤ button below to show your support.**

**\_ Thank you for reading**

**\_sandhya kumari**