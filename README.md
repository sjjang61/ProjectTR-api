# ProjectTR
ganymede's indi-game

# Install
'''
pip install -r requirements.txt
'''


## To-do
---
protocol struct

-- 파티
struct squad
{
   int heroIdx;
   int posX;
   int posY;
}

struct AccountInfo
{
    string id;
    int level;
    string name;
    int score;
    int[] heroes; ### ???
    list<squad> squad;
}


MatchInfo
{
   AccountInfo enemyAccountInfo;
   list<squad> squad;
   int channelNo;
}


----------------------


sendLogin
-> string id 

recvLogin
< - AccountInfo myAccountInfo;

---------------------------

sendMatch
-> string id;
-> n초 대기 


recvMatch
<- MatchInfo matchInfo;
---
windows
set FLASK_ENV=development
set FLASK_APP=serverApplication.py
flask run

linux
export FLASK_ENV=development
export FLASK_APP=serverApplication.py
flask run

