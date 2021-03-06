# Sector D17

## Prepare environment
1. Clone [docker](https://github.com/sectord17/docker) to directory `docker`
1. Clone [server-game](https://github.com/sectord17/server-game) to directory `server-game`
2. Clone [server-slave](https://github.com/sectord17/server-slave) to directory `server-slave`
3. Clone [server-master](https://github.com/sectord17/server-master) to directory `server-master`

## Setup
1. Copy file containing environment variables

    ```bash
    cp .env.example .env
    ```

2. Set your ip address as a value of the **IP** variable in `.env` file

    ```bash
    IP=192.0.2.1
    ```

3. Run
    
    ```bash
    docker-compose up --build -d
    ```
    
## Testing
1. Create example server

    ```bash
    curl -X POST -d "name=test123" http://127.0.0.1:3001/games
    ```

2. Get list of servers

    ```bash
    curl http://127.0.0.1:3001/games
    ```