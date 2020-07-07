# nginx-rtmp-multi-stream

Docker Compose setup to push a stream to multiple providers like facebook, twitch or youtube. Using stunnel to support rtmps for facebook. This project is based on the work of [Sebastián Ramírez](https://github.com/tiangolo/nginx-rtmp-docker) and [Jessica Hamilton](https://github.com/jessicah/nginx-rtmp-stunnel).

## How to use

Install Docker: https://www.docker.com/get-started <br>
Install Docker Compose: https://docs.docker.com/compose/install/ <br>
Install OBS: https://obsproject.com

#### 1. Edit nginx.conf:
- Remove push rtmp://... lines if you don't want to use this provider (or add other ones below the lines)
- Replace streamkey with the key from your provider

#### 2. Start the rtmp server:
- Open your terminal, go into the nginx-rtmp-multi-stream folder and enter: ```docker-compose up```

#### 3. Edit the stream settings in OBS:
  - Set Service to Custom
  - Enter as Server: rtmp://0.0.0.0/live
  - Use a custom Stream Key you want
  
## Credits
- [Sebastián Ramírez](https://github.com/tiangolo)
- [Jessica Hamilton](https://github.com/jessicah) 

## License

This project is licensed under the terms of the MIT License.
