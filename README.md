# cs561-assignment2-aws-mock-server

## Description

As part of the CS 561 class at OSU, created a mock server to mock the [OpenWeather API](https://openweathermap.org/api) using [apimocker](https://www.npmjs.com/package/apimocker).

## Usage

### Install [apimocker](https://www.npmjs.com/package/apimocker):
```sh
npm install -g apimocker
```

### Clone the repository:
```sh
git clone https://github.com/RN35/cs561-assignment2-aws-mock-server.git
```

Modify 'mockDirectory' attribute in [config.json](config.json) file to point to the location where you cloned the repo: 

eg: if you cloned your repo to /home/rockstart_developer/mock_server, 
```
  "mockDirectory": "/home/rockstart_developer/mock_server/"
```

### Start the mock server:
```sh
apimocker -c <path_to_config_file>
```
If your mock server is running you will get a message like this:
```
[ec2-user@ip-172-31-91-68 mocker_server]$ apimocker -c config.json
[apimocker] Loading config file: /home/ec2-user/mocker_server/config.json
[apimocker] Set route: GET data/2.5/weather : response.json
[apimocker] Mock server listening on port 7878
```

### Hit the endpoint:
If you are running this on your local machine, hit the endpoint using:
```url
http://localhost:7878/data/2.5/weather
```

If you are running this on a remote server, hit the endpoint using:
```url
http://your-domain-or-ip-address:7878/data/2.5/weather
```
> :warning: Remember to open the port on which the mock server is running!  

You can configure the port number by modifying the "port" attribute in the [config.json](config.json) file.


