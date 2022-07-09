# Sort-Authors-Github-

DESCRIPTION
--------------------------------------------------------------------------------------
Returns a text file containing the top commit authors for a repo during a particular period and their individual total commits 


REQUIREMENTS
--------------------------------------------------------------------------------------
This script requires the following to function:

.[NODEJS] V14.15.1 or higher  
.[GIT] V2.29.2 or higher 
.[ShellJS] V0.8.5 or higher



INSTALLATION
-------------------------------------------------------------------------------------
Install NODE globally as normal. Visit
  https://nodejs.org/en/

Install GIT globally as normal. Visit 
  https://git-scm.com/
  
Install SHELLJS within the repo package you're working with. Run 
  `npm i shelljs (windows)` 
  

  
CONFIGURATION
-------------------------------------------------------------------------------------
Place the script within the root directory of the repo you're working with.
Adjust the following variable as desired:

1. Starting date for period of data retrieval = startDate FORMAT(string)  "Dec 9 2021"
2. Ending date for the period of data retrieval = endDate FORMAT(string)  "July 9 2022"
3. Desired number of Authors to return = count FORMAT(number) 12 



RUN
-------------------------------------------------------------------------------------
Within terminal. Run
  `node sortAuthors.js`
  


OUTPUT
-------------------------------------------------------------------------------------
Text file titled "authors" will be created within the root directory of the repo with the top authors for the given period. With the total number of commits listed on the left as well as their names and email addresses. The total authors will also be printed to the terminal but this can be ignored since the text file will have it properly organized.

EXAMPLE:
    312	Zuul <zuul@review.opendev.org>
     90	Rodolfo Alonso Hernandez <ralonsoh@redhat.com>
     52	Slawek Kaplonski <skaplons@redhat.com>
     33	yatinkarel <ykarel@redhat.com>
     13	Jakub Libosvar <libosvar@redhat.com>
     12	LIU Yulong <i@liuyulong.me>
     12	elajkat <lajos.katona@est.tech>
      9	Oleg Bondarev <oleg.bondarev@huawei.com>
      8	zhouhenglc <zhouhenglc@inspur.com>
      5	Arnau Verdaguer <averdagu@redhat.com>
      5	Frode Nordahl <frode.nordahl@canonical.com>
      5	Luis Tomas Bolivar <ltomasbo@redhat.com>

Troubleshooting
------------------------------------------------------------------------------------
When running the script multiple times be sure to clear the authors.txt file or delete it entirely because the information will be appended to the existing info and this could be confusing.

The count variable will have to be adjusted according to the number of authors within the repository for a given period. If the number is adjust to be more than the amount of commit authors avaliable the script will return undefined for the additional entries. 
