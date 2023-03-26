  # Spooderman's Webhook module

  Hello and welcome to my very easy to use webhook module. Below is the documentation.

  # Requiring the module

  To require the module, Put this at the start of your code:

  ```lua
  local module = loadstring(game:HttpGet("https://raw.githubusercontent.com/spooderman11/Spooderman.rocks/main/WebhookModule.lua", true))()
  ```

  To require it in a studio enviroment, Open your `ServerScriptService` Object in your explorer, then check the `LoadstringEnabled` attribute. Then put your code in a script.

  # Initializing the module

  To initialize the module, put this in your code:

  ```lua
  --[[
      Executor: <bool>  If you want to use the executor, put true, if not, put false.
      Webhook: <string> The webhook you want to use.
  ]]

  local main = module:Init({
      Executor = false,
      Webhook = "https://discord.com/api/webhooks/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
  })
  ```

  # Sending a message

  To send a message, put this in your code:

  ```lua
  --[[
      Message: <string> The message you want to send.
  ]]

  main:Message({
      Message = "Hello, World!"
  }):Send()
  ```

  # Sending an embed

  To send an embed, put this in your code:

  ```lua
  --[[
      Title: <string> The title of the embed.
      Description: <string> The description of the embed.
      Color: <string> The color of the embed.
      Footer: <string> The footer of the embed.
      Image: <string> The image of the embed.
      Thumbnail: <string> The thumbnail of the embed.
      Fields: <table> The fields of the embed.
  ]]

  main:Embed({
      Title = "Hello, World!",
      Description = "This is an embed!",
      Color = 0x00FF00,
      Footer = "This is a footer!",
      Image = "https://i.imgur.com/xxxxxxxxxxxx.png",
      Thumbnail = "https://i.imgur.com/xxxxxxxxxxxx.png",
      Fields = {
          {
              ["name"] = "Field 1",
              ["value"] = "This is a field!",
              ["inline"] = true
          },
          {
              ["name"] = "Field 2",
              ["value"] = "This is a field!",
              ["inline"] = true
          }
      }
  }):Send()
  ```
  
  # Notes
  
  You can make the embed/message object a `Local` Object using a `local` Variable before defining the object to do things like:
  
  ```lua
  local embed = module:Embed(info)

  embed:Send()
  ```
