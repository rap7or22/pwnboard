# PWNboard
PWNboard for RIT redteam engagements and competitions

Modified version of ztgrace/pwnboard

# Running the PWNboard
## Install
```
apt-get install -y redis-server python3-redis python3-flask python3-yaml
git clone https://github.com/micahjmartin/pwnboard
```
## Configure
Configure the topology json file by running `./scripts/generate_topo.py` or by
hand modifying the sample config `toplogy.json`.


Setup slack information in the `config.yml` file and modify the database settings
if you are running the Redis DB somewhere else.

**Update the server IP and port in `config.yml`**

## Setup Frameworks
If you are adding hooks to frameworks such as cobaltstrike or empire,
run the install scripts for each framework and client.
The install scripts will be rendered based off of the current configuration file.

### Currently supported frameworks:
**CobaltStrike** `http://localhost/install/cobaltstrike/ or `/install/cs`

**Empire** `https://localhost/install/empire`

## Run
Run `./pwnboard.py` from the commandline

# Future Features
* Init script to help configure and use the program
* Reset the db before starting an engagement
* Click on a host to track the beacons REQUIRE DB UPDATE


![pwnboard](https://raw.githubusercontent.com/micahjmartin/pwnboard/master/img/PWNboard.png)
