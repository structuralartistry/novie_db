What to do next:

  - Include your webpack assets to your application layout. Change hello-world-bundle as needed.

      <%= javascript_pack_tag 'hello-world-bundle' %>

  - Run the foreman command to start the rails server and run webpack in watch mode.

      foreman start -f Procfile.dev

  - Change this line app/views/hello_world/index.html.erb to `prerender: true` to see
    server rendering (right click on page and select "view source").

      <%= react_component("HelloWorldApp", props: @hello_world_props, prerender: true) %>

  - Run the foreman command to start the rails server and run webpack in HMR mode. Be sure
    to change your development/dev_server/hmr setting to true to see HMR in action.
    Note, you cannot use the default Procfile.dev-server setup with server rendering.

      foreman start -f Procfile.dev-server

  - You may run the commands in the Procfiles in separate shells rather than using foreman.

  - See the documentation on https://github.com/rails/webpacker/blob/master/docs/webpack.md
    for how to customize the default webpack configuration.

  - Visit http://localhost:3000/hello_world and see your React On Rails app running!

