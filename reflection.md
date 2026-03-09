# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?
The game would not give me a new game everytime i pressed the new game button. Sometime sthe number would be higher and it would state that its lower, even though thats not true. It would only store 4 Items in the history or past inputs. not sure what the final score and final hint was about, it was giving random numbers and show hint was not showing anything, blank button. Attemps allowed is all over the place its not working correctly.
There was a hit registry like i had to click twice


---

## 2. How did you use AI as a teammate?

I used claude
One example that Ai suggestion was incorrect is when it tried to discard the hint section. it discarded the hint section because it wasnt funcitoning properly
One example that was correct was when it found out that the new game button did not fully reset and only resetted the attempts and secret number.
its also not giving me if im getting a higher guess or lower guess anymore and the show hint im not finding any hints

## 3. Debugging and testing your fixes


I ran the test to determine whether it passed or failed
I tried running a prompt to fix a show hint where i was confused what its job was and because of human error the Ai decided to remove it completely and its giving a hard time to fix it
Im trying to fix the code where i changd the attempts allowed for each mode but for some reason its ending the attempts at 5 when i Put 6 so i am debugging that code and to test it I just have to manually press # of times required for each mode to satisfy the test case.
I also had to decide where it was showing that my first hint was not working in conjuction with the first guess and it would only show up after the 2nd hint because the computer was picking it up as #0 and #1 so i had to debug this and run the test case to figure out if it passed or not
i also figured that the difficulty resets the sercrets but does not correlate exactly to the difficulty so  i made sure that it updates the difficulty and the secret number whenever the difficulty is changed
---

## 4. What did you learn about Streamlit and state?


The secret number kept changing in the original because it was not being stored it would just replace the old secret with new ones.
streamlit apps reruns the entire file and rebuilds the page with the new input and session state is the way that streamlit remembers the stuff like a storage box
I stored the secret number in st.session_state and only generated it once and after that it resues the same saved secret insteadof making a new one
---

## 5. Looking ahead: your developer habits


I need to learn how to use git in a more efficient way and make sure my folder and files are in the correct spots
one thing iwould do differently is to make sure to be specific so it doesnt change the code too much
this project didnt change much of the way i think about code
