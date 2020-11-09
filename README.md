# Gruppe 3 - Uptight Wealth
*Ikke vores valg af gruppenavn*

**Gruppemedlemmer:**
- Cahit
- Marcus
- Michael

# The Python Cult

<img src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/bb485920-261e-46b9-896a-cb18fda5d929/dbvl0da-050b7754-242a-4a9f-adff-e4a4c8652fcd.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOiIsImlzcyI6InVybjphcHA6Iiwib2JqIjpbW3sicGF0aCI6IlwvZlwvYmI0ODU5MjAtMjYxZS00NmI5LTg5NmEtY2IxOGZkYTVkOTI5XC9kYnZsMGRhLTA1MGI3NzU0LTI0MmEtNGE5Zi1hZGZmLWU0YTRjODY1MmZjZC5wbmcifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6ZmlsZS5kb3dubG9hZCJdfQ.39OiImVLazb8JFOfhDJWFl2529SJ7obSvPHoSpKNka4" alt="Cult Symbol" width="200">

## Assignment 1: Organize your cult

1. Read in the random names in the file ***Random_Names.txt*** into a list ***cultist_names***.
2. Make a support method ***recruit_cultist***, that takes a string **name**, and returns a dict with *skills* as below, each assigned a random int between 0 and 5:
```python
min_score = 0
max_score = 5
cultist = {
  'name': {
    'stealth': random.randint(min_score, max_score), 
    'influence': random.randint(min_score, max_score), 
    'endurance': random.randint(min_score, max_score), 
    'lore': random.randint(min_score, max_score), 
    'economic': random.randint(min_score, max_score), 
    'strength': random.randint(min_score, max_score), 
    'insanity': random.randint(min_score, max_score)
  }
}
```
3. Run all names from ***cultist_names*** thought the ***recruit_cultist*** method, and gather all the results in a ***cult*** dict
4. Make the following dict ***cult_roles*** as below. Each value represents how importent a skill is for the given role:
```python
cult_roles = {
'Priest': {'stealth': -1, 'influence': 3, 'endurance': 2, 'lore': 4, 'economic': 1, 'strength': 0, 'insanity': 5},
'Enforcer': {'stealth': 1, 'influence': 3, 'endurance': 4, 'lore': 0, 'economic': -1, 'strength': 5, 'insanity': 2},
'Assassin': {'stealth': 5, 'influence': -1, 'endurance': 4, 'lore': 1, 'economic': 0, 'strength': 2, 'insanity': 3},
'Recruiter': {'stealth': 1, 'influence': 5, 'endurance': 0, 'lore': 3, 'economic': 2, 'strength': -1, 'insanity': 4},
'Accountant': {'stealth': 2, 'influence': 1, 'endurance': 3, 'lore': 4, 'economic': 5, 'strength': 0, 'insanity': -1},
'Advisor': {'stealth': 2, 'influence': 4, 'endurance': -1, 'lore': 5, 'economic': 3, 'strength': 0, 'insanity': 1}
}
```
5. Make a method ***assign_cult_roles***, that takes the ***cult*** and ***cult_roles*** dicts, and returns a ***all_cultists_roles*** dict, where each cultist's name from the cult is the key, and each has it's given role as value. Each role should be assign on which of the roles have the highest 'score' when dotted between the name dict and the cult_roles.
6. Show how many cultist the cult have occupying each role. *(print is fine here)*



<img src="https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/be796ae1-a2db-40a4-ab06-6aa42a607e91/dd7vv03-f5d37c61-a181-4185-84b5-866857e0965b.png?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOiIsImlzcyI6InVybjphcHA6Iiwib2JqIjpbW3sicGF0aCI6IlwvZlwvYmU3OTZhZTEtYTJkYi00MGE0LWFiMDYtNmFhNDJhNjA3ZTkxXC9kZDd2djAzLWY1ZDM3YzYxLWExODEtNDE4NS04NGI1LTg2Njg1N2UwOTY1Yi5wbmcifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6ZmlsZS5kb3dubG9hZCJdfQ.R7fnou_nsvV9raJk_o1eyJ14ETdryFbAm8a4wLdUQ2M" alt="Cultist">

## Assignment 2: Cult Recruitment Statistics
1. Save the data from the ***cult_statistics.csv*** file in a variable ***cult_data*** *(You can use panda here)*
2. Plot new recruits as a function to amount_spend.
3. Plot new recruits as a function to total_amount.
4. Make a model object from *klearn linear regression model* to use for the following assignments.
5. Predict new recuits if amount_spend doubles the amount from 2020
6. Predict new recuits if total_amount decrease by 20% of the amount from 2020
7. Reverse the data, to predict how much amount_spend should be, to make new_recruits equal to 2020

**Bonus:** See how many cultist have left/died each year from the dataset. When you have the result, you know why to join the cult!

<img src="https://thebingbutt.files.wordpress.com/2019/01/buttcultgathering.jpg" alt="Cult Gathering">

_______________________

Vi benytter datasættene: [Random Names](https://raw.githubusercontent.com/Micniks/Python-Week10-Group-3-Assignments/main/Random_Names.txt) & [Cult Statistics](https://raw.githubusercontent.com/Micniks/Python-Week10-Group-3-Assignments/main/cult_statistics.csv)

Dette github repository er tilrettet opgavestillinger, så udspecifieret her: [Uge7 Opgave](https://docs.google.com/document/d/1ojSiBWwLo4-Rc7763vx6aVEYdNluATOMja9qqk4dodU/edit#) 
