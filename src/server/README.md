# Overview
The is project is prototyping use of the TTAM api for authentication and retreival genotyping results from the TTAM result set.

## Stage 1 - gather references
https://api.23andme.com/dev/  
https://api.23andme.com/help/  
https://groups.google.com/forum/#!forum/23andme-api  
https://api.23andme.com/docs/reference/  
https://api.23andme.com/docs/authentication#scopes  

<a href="https://api.23andme.com/authorize/?redirect_uri=https://exampleapp.com/receive_code/&response_type=code&client_id=8c5bc3cd41932f405c80612248b7ae43&scope=basic rs123">Connect with 23andMe</a>

https://api.23andme.com/authorize/?redirect_uri=http://localhost:5000/receive_code/&response_type=code&client_id=69db0a89634206ce0c40f21915e03be6&scope=basic


hbanaharis@mac.com
avalonista

bellesamelbourne@hotmail.com
JuJiP00Ji

banaharisavalon@gmail.com
seva4eva

## Stage 2 - Test auth API via client and cURL

## Stage 3 - Implement Rudimentary UI

curl https://api.23andme.com/token/ \
    -d client_id=69db0a89634206ce0c40f21915e03be6 \
    -d client_secret=188a92d74b82387168ce8ffbb98f5e94 \
    -d grant_type=authorization_code \
    -d code=771ebf7dc8dc9cc2e1fcab142c8ac0ea \
    -d redirect_uri=http://localhost:5000/receive_code/ \
    -d "scope=basic"

    -d "scope=basic%20names%20email%20ancestry%20report:all%20rs3094315%20genomes%20phenotypes:read:all"


https://api.23andme.com/token/
?client_id=69db0a89634206ce0c40f21915e03be6
&client_secret=188a92d74b82387168ce8ffbb98f5e94
&grant_type=authorization_code
&code=3bfc572a22263b178f45548cd2556354
&redirect_uri=http://localhost:5000/receive_code/
&scope=basic%20names%20email%20ancestry%20report:all%20rs3094315%20genomes%20phenotypes:read:all

https://api.23andme.com/token/
?client_id=69db0a89634206ce0c40f21915e03be6
&client_secret=188a92d74b82387168ce8ffbb98f5e94
&grant_type=authorization_code
&code=7699173b85bd765cd79594f47b579f91
&redirect_uri=http://localhost:5000/receive_code/
&response_type=code
&scope=basic%20names%20email%20ancestry%20report:all%20rs3094315%20genomes%20phenotypes:read:all

https://www.getpostman.com/oauth2/callback

curl -d '' 'https://api.23andme.com/token/?redirect_uri=http://localhost:5000/receive_code/&client_id=69db0a89634206ce0c40f21915e03be6&client_secret=188a92d74b82387168ce8ffbb98f5e94&grant_type=authorization_code&code=3fe9849a277e6e23178a9255fca4fbb7&scope=basic%20names%20email%20ancestry%20report:all%20rs3094315%20genomes%20phenotypes:read:all'

curl -d 'redirect_uri=http://localhost:5000/receive_code/&client_id=69db0a89634206ce0c40f21915e03be6&client_secret=188a92d74b82387168ce8ffbb98f5e94&grant_type=authorization_code&code=154ceadb7e3c14706ad31b0fc766c662&scope=basic%20names%20email%20ancestry%20report:all%20rs3094315%20genomes%20phenotypes:read:all' \
https://api.23andme.com/token/

redirect_uri=http://localhost:5000/receive_code/&client_id=69db0a89634206ce0c40f21915e03be6&client_secret=188a92d74b82387168ce8ffbb98f5e94&grant_type=authorization_code&code=518e5e8ef76416573343bdae4c1fd8f9&scope=basic%20names%20email%20ancestry%20report:all%20rs3094315%20genomes%20phenotypes:read:all

curl -d 'redirect_uri=http://localhost:5000/receive_code/&client_id=69db0a89634206ce0c40f21915e03be6&client_secret=188a92d74b82387168ce8ffbb98f5e94&grant_type=authorization_code&code=7d510ef544c453df81c9ec72c29c644e&scope=basic' \
https://api.23andme.com/token
