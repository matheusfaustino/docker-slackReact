# Docker slackReact
Docker container that I use to develop [slackReact](https://github.com/matheusfaustino/slackReact/)
It does not contain something magic or anything else. I shared it because it could help you running the project.

### Using
Building(repo's root folder): `docker-compose up`
Going inside the container: `docker exec -it <container_name> bash`

### Attention
Before build the image, check if the [path](/docker-compose.yml#L7-L8) of the project is right for you. 

### License
It is under the MIT license. For the full copyright and license information, please read the [LICENSE](/LICENSE) file that was distributed with this source code.
