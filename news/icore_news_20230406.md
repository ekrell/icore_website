# iCORE Newsletter – 2023/03/20

![logo](../img/logo_plain_sm.jpg)

The iCORE newsletter highlights events and information related to the [innovation in COmputing REsearch (iCORE) lab](https://icore.tamucc.edu/),
as well as the broader GSCS/CS programs at Texas A&M University - Corpus Christi and whatever else might interest that community.
If you have any news or resources you would like to share, send an email to [Evan Krell](https://scholar.google.com/citations?user=jLuwYGAAAAAJ&hl=en) (ekrell@islander.tamucc.edu).

[See past newsletters.](https://github.com/ekrell/icore_website/tree/main/news)

## Welcome

![Teo Chew Temple](../img/houston_chinatown_temple.jpg)

- Scenes from the Teo Chew Temple in Houston. 
- Evan Krell should be back in Corpus Christi in time to present at the [Symposium for Student Innovation, Research, and Creative Activities](https://www.tamucc.edu/research/student-symposium/index.php).
- iCORE will be well represented with poster or oral presentations from Abhishek Phadke, Josh Boyd, Miranda White, and Evan Krell. _(Anyone else?)_
- Also, Abhishek Phadke submitted an entry to the [Research Image Student Competition](https://www.tamucc.edu/research/ri-week/risc.php).

## iCORE Meetings

**[iCORE Teams meeting link](https://teams.microsoft.com/l/meetup-join/19%3Ameeting_MDdlZDBiMTgtYzVjNS00YjhhLWE5OTctY2Y5YzMyYTljNzU5%40thread.v2/0?context=%7B%22Tid%22%3A%2234cbfaf1-67a6-4781-a9ca-514eb2550b66%22%2C%22Oid%22%3A%22994c008b-0707-4f3c-8ac0-73b65e733430%22%2C%22MessageId%22%3A%220%22%7D)**

### Previous meeting: 

- Mahmoud Eldefrawy finished up his 2-part series [_A Gentle Introduction to Machine Learning_](https://github.com/ekrell/icore_website/blob/main/news/icore_news_20230227.md).
- Soon, we will make all of the Jupyter Notebooks available that Mahmoud presented.
- We had good attendance and many great questions for Mahmoud, so thanks to all who came.

### Next meeting: April 14, 2:00-4:00pm

**Meeting Theme**: _computer science + domain expertise**

- The purpose of these meeting is to share experiences where computer science has been applied to other fields.
- Seeking volunteers who are either:
  1. **outside CS** to share how they are using programming and CS in their research.
  2. **inside CS** who have worked with domain experts to solve problems that required their expertise
- The goal is to share knowledge and find opportunities for collaboration 
  - CS students can learn how their knowledge can be applied to research in other fields
  - Non-CS can get potentially get feedback on techniques and tools they likely don't know about


| **Name**        | **Program** | **Domain** | **Description**                                                                                                              |
|-----------------|-------------|------------|------------------------------------------------------------------------------------------------------------------|
| Florian Morvais | CMSS | Atmospheric science        | Using machine learning to predict phenomena such as lightning rate and clouds' maximum echo top heights from satellite data.  |
| Josh Boyd       | GSCS | Robotics & surveying       | Swarm array imaging: a swarm of drones capture synchronous imagery over dynamics environments.                                |
|       |       |     |                                                                                                                                                         |
| Evan Krell      | GSCS | Atmospheric science        | Using machine learning to detect wildfire-driven thunderstorms (pyroCbs) from satellite imagery and atmospheric model data.   |

- **Help us fill out this table: contact Evan Krell (ekrell@islander.tamucc.edu) if you want to present!**
- **Or share this newsletter with someone you know**


## Tech Tips

### Monitor your processes

- This week, there was a bit of an incident with the TAMUCC _deep learning_ server. 
- Suddenly, jobs were running _veeeeeery_ slowly. Why?
- Remember, when you spawn a batch of processes, they are not always killed just because you terminated the program that spawned them.
- For example, consider a script `run_experiments.sh` that launches 5 machine learning training runs.
- If I am debugging this script, I might run it and kill it a large number of times: each time spawning 5 more!
- As each one uses up more memory, none can make any progress and the machine grinds to a halt.
- It is critical to make sure that the **spawned processes are also killed!**
- In this case, the person thought that they had 0 running jobs, but in fact had over 200: each using up amost 2 GB of memory!

How to monitor running processes:

    top
    
Example output:

    top - 14:24:01 up 2 days,  2:08,  5 users,  load average: 0.94, 0.97, 1.00
    Tasks: 412 total,   1 running, 411 sleeping,   0 stopped,   0 zombie
    %Cpu(s):  3.3 us,  1.9 sy,  0.0 ni, 94.9 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
    MiB Mem :  15606.8 total,   1737.1 free,   7187.0 used,   6682.7 buff/cache
    MiB Swap:   2048.0 total,   2042.7 free,      5.2 used.   6171.9 avail Mem 

        PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                                                                                                                      
     288418 ekrell    20   0 3079336 499560 138600 S  15.2   3.1  31:23.07 Isolated Web Co                                                                                                                              
     384028 ekrell    20   0 7229752 563236 285768 S  11.6   3.5  63:13.25 zoom                                                                                                                                         
       2025 ekrell    20   0 7916844 394300 163700 S   8.9   2.5  98:25.57 gnome-shell                                                                                                                                  
       3739 ekrell    20   0 1394708 125992  82104 S   8.3   0.8  27:47.95 Xwayland                                                                                                                                     
       1812 ekrell     9 -11 3292524  31180  23272 S   7.6   0.2  81:35.07 pulseaudio                                                                                                                                   
     288178 ekrell    20   0   13.2g 836736 282196 S   7.0   5.2  81:47.45 firefox                                                                                                                                      
     288408 ekrell    20   0 3182584 595636 111160 S   5.6   3.7  26:07.90 Isolated Web Co             

The first column has the process ID or PID. You can use this number to kill processes. 

How to kill a process using a PID:

    kill -9 PID

How to kill a range of processes:

    kill -9 {PID1..PID2}      # e.g.   kill -9 {10..20}

- Make sure to kill only processes that should be killed. 
- Thankfully, you only have permission to kill processes that you own, so mine are safe if you use the wrong PID

## Weekly Snack Report

- Since Evan is still in Houston, he has continued to explore everything edible in Houston's Chinatown. 
- Despite the name, it is as much a Vietnamese town as Chinese. There is a _Hong Kong Mall_ that is almost exclusively Vietnamese establishments.




