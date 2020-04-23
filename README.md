## kitabisa

#### To start the program
    

`go mod vendor`

`go run main.go`

 and there would be two available http endpoint `/` and `/token`

#### to generate new token : 
      curl -H "Content-Type: application/x-www-form-urlencoded" \
           -d "username=myusername&password=mypassword" \
           http://localhost:8080/token

#### After succesfully got a token then you can request to the main resource
      curl -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE1ODc2MzMxODQsImlhdCI6MTU4NzYyOTU4NCwidXNlciI6Im15dXNlcm5hbWUifQ.y06-01LCfwRgBJw7lgSMuv50Vza6xkXc8X0SK0rUTmM" \
           -H "Content-Type: application/json" \
           http://localhost:8080
