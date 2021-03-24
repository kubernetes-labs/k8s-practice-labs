npm init -y
npm install ronin-server ronin-mocks
Create server.js file with below content

```nodejs
const ronin     = require( 'ronin-server' )
const mocks     = require( 'ronin-mocks' )

const server = ronin.server()

server.use( '/', mocks.server( server.Router(), false, true ) )
server.start()
```

Start server using **node server.js**
Execute the **post.sh** and **get.sh** files from curl directory to test the application.
