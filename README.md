# CMPE283-assignment-1 - Harsh Vaghasiya (016053102)

## Team Members:
1) Harsh Vaghasiya - 016053102 - (Just me)

## Questions and Answers:
1) For each member in your team, provide 1 paragraph detailing what parts of the lab that member implemented / researched. (You may skip this question if you are doing the lab by yourself). <br><br>
**Answer: I did the whole assignment by myself.** <br><br>
----------------------
2) Describe in detail the steps you used to complete the assignment. Consider your reader to be someone skilled in software development but otherwise unfamiliar with the assignment. Good answers to this question will be recipes that someone can follow to reproduce your development steps. <br>
**Note:** I may decide to follow these instructions for random assignments, so you should make sure they are accurate. <br><br>
**Answer:**<br><br>
**Step-1: Created project in GCP.** <br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 7 42 46 AM" src="https://user-images.githubusercontent.com/52853300/200430735-d36c403d-300e-4125-a1e5-c84eeb0fcab7.png">
<br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 7 43 45 AM" src="https://user-images.githubusercontent.com/52853300/200430835-c2e6e299-4c56-4360-b826-e4a3f3ae1b00.png">
<br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 7 44 11 AM" src="https://user-images.githubusercontent.com/52853300/200430873-0ab5f677-fdce-4bd4-9638-15b85b080b4a.png">
<br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 9 09 21 AM" src="https://user-images.githubusercontent.com/52853300/200430934-1808d7c0-3e7b-486b-a696-ecfdb40fb0dc.png">
<br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 9 09 48 AM" src="https://user-images.githubusercontent.com/52853300/200431009-7a086814-7ebe-43b6-bf43-4a34aa40bf95.png">
<br><br>

**Step-2: Enabled Compute Engine API in order to create VM instance. Opened Google Cloud Shell and created VM instance with enabled nested virtualization in this project.** <br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 9 13 31 AM" src="https://user-images.githubusercontent.com/52853300/200431309-a5fa7050-b780-472b-b965-4a474ccf70a0.png">
<br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 9 13 46 AM" src="https://user-images.githubusercontent.com/52853300/200431320-0994bb0d-71ee-45cb-a8a5-7cc385d9d7c2.png">
<br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 9 10 01 AM" src="https://user-images.githubusercontent.com/52853300/200431153-7bf37eb8-3496-4e0a-9fdb-25b984e4caeb.png">
<br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 9 40 41 AM" src="https://user-images.githubusercontent.com/52853300/200431387-086a059f-eddb-4604-af95-3818ea14ff89.png">
<br><br>

**Step-3: Logged into the VM instance using SSH.** <br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 9 59 11 AM" src="https://user-images.githubusercontent.com/52853300/200432398-d6a8899f-92e2-4436-88ff-c00a6e303f7e.png">
<br><br>

**Step-4: Created the project directory at root folder of Linux VM Instance. Uploaded code file and Makefile in this directory. Updated the code file using Intel SDM Manual.** <br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 10 00 12 AM" src="https://user-images.githubusercontent.com/52853300/200432466-5e082234-7685-4924-944b-589d377e4716.png">
<br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 10 29 56 AM" src="https://user-images.githubusercontent.com/52853300/200432574-2593785f-f552-4a1f-902e-6abd55547b56.png">
<br><br>

**Step-5: Installed "make" command into instance. Checked the kernel information using "uname -r" command and then installed Linux Headers accordingly for that specific version of the kernel.** <br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 10 31 18 AM" src="https://user-images.githubusercontent.com/52853300/200432649-8bb71aff-0de4-4236-9b9a-a06f76cac6cc.png">
<br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 10 32 25 AM" src="https://user-images.githubusercontent.com/52853300/200432683-abbc3829-0118-4f8d-85af-16345ccfeff8.png">
<br><br>

**Step-6: Built the kernel module using make command.** <br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 10 36 59 AM" src="https://user-images.githubusercontent.com/52853300/200435096-640febfc-030b-47a2-a060-5f06366e7701.png">
<br><br>

**Step-7: Inserted this kernel module using "insmod" command. And finally checked the VMX Features availability using "dmesg" command.** <br><br>

<img width="1512" alt="Screen Shot 2022-11-07 at 10 38 29 AM" src="https://user-images.githubusercontent.com/52853300/200435185-97e620b1-a162-4ff2-b748-42c43491ad0a.png">
<br><br>

**Output:**

<img width="1512" alt="Screen Shot 2022-11-07 at 10 44 42 AM" src="https://user-images.githubusercontent.com/52853300/200435348-d915cd14-9d0f-464d-8ccd-5c770bde3210.png">
<br><br>

<img width="1510" alt="Screen Shot 2022-11-07 at 10 45 20 AM" src="https://user-images.githubusercontent.com/52853300/200435363-6fbb42a9-50a8-43a1-9e3f-44db2103adf1.png">
<br><br>

**Explanation for not trying tertiary procbased control:**

From the output of primary procbased controls, I got to know that I do not have permission to set tertiary procbased control. Hence, I wrote the code for tertiary procbased controls but did not run it(hence commented it). <br><br>

Note: If you try to call MSR for Tertiary Procbased Controls and if you do not have access to set it just like in my case, you will get an error as following: <br><br>

<img width="1481" alt="Screen Shot 2022-11-07 at 1 58 23 PM" src="https://user-images.githubusercontent.com/52853300/200435837-b7e6c589-db9c-4d0a-bba0-bb846bbe28bb.png">



