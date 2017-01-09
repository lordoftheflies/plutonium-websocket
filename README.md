# plutonium-websocket

Wrapper for browser-native WebSocket client. It's built using the Polymer 1.0.

## Usage

1. Import Web Components' polyfill:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents-lite.min.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/plutonium-websocket/plutonium-websocket.html">
    ```

3. Start using it!

    ```html
    <plutonium-websocket url="ws://{host}:{port}" protocol="{sub-protocols}"></plutonium-websocket>
    ```

## Options

Attribute       | Options                   | Default             | Description
---             | ---                       | ---                 | ---
`url`           | *string*                  | `undefined`         | WebSocket server endpoint to connect to.
`protocol`      | *string*                  | `undefined`         | A subset protocol to be used as part of the communication with the server.

## Methods

Method        | Parameters   | Returns     | Description
---           | ---          | ---         | ---
`send()`   | message String       |     | Used to send messages to the server.
`close()`   | None      |     | Close socket.

## Events

Event         | Description
---           | ---
`ws-message` | Triggers when a message from the server is received.
`ws-error` | Triggers when there is an error triggered by WebSocket client
`ws-open` | Triggers when a socket is first open
