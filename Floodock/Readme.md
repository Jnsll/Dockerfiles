# Floodock Image

## Goal : To be able to run the ref modflow model version of 12th april 2019

### Command to run image / lauch container with lauching simulation (while creating a specific input_file.txt)
`docker run -t -d floodock python settings_model.py -p trimester`
### Acces to the container 
`docker exec -i -t <container name> /bin/bash`
