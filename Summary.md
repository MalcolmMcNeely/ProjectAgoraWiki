Project Agora is an bespoke internet forum board catered for World of Warcraft guilds. In addition to basic forum requirements there is a need to build guild specific tools for raid and information management.

#Technologies
We are investing heavily in Microsoft Azure because we are cool kids who do cool things. However, because this project will reach go beyond proof of concept into product, the costs of running this is a concern when choosing technologies. This solution does not need to scale, we expect approx 50 - 100 active users, so this doesn't need to be an explicit concern.

##[Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/)
We will use an Azure App Service (Platform as a Service) to serve up a [ReactJS](https://reactjs.org/docs/getting-started.html)/[Redux](https://redux.js.org/api/api-reference) based front end. App Services run on an [App Service Plan](https://docs.microsoft.com/en-us/azure/app-service/overview-hosting-plans) and having a basic plan [will cost £0.056](https://azure.microsoft.com/en-us/pricing/details/app-service/windows/) at time of writing although we will start with the Free tier and scale up as necessary.

###UI Framework
The prime candidate for this is [Material UI](https://material-ui.com/) for our React project.

##[Azure Functions](https://docs.microsoft.com/en-us/azure/azure-functions/functions-overview)
This will act as our [serverless (Functions as a Service)](https://martinfowler.com/articles/serverless.html) backend which will interact with our persistent data. This allows us to run code on-demand without having to provision or manage infrastructure and we only pay for the time spent running our code.

###Event Sourcing
Because we are extremely cool kids, we will be using the [StreamStone](https://github.com/yevhen/Streamstone) NuGet package which is a small, non-opinionated library which facilitates [Event Sourcing](https://martinfowler.com/eaaDev/EventSourcing.html) with Azure Table Storage.

##Authentication
[Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/) is, to my knowledge, free but we also have the option in utilizing Blizzard's [Battle.net OAuth2 API](https://develop.battle.net/documentation/guides/using-oauth) which will require us to register something-or-other at the [Battle.net developer portal](https://develop.battle.net/). An example of how to use Blizzard's authentication in NodeJS can be found [here](https://github.com/Blizzard/passport-bnet). If we do pursue this route then we will need to provide the ability for forum admin to override forum access in case of a user account being compromised.

##Data Persistence
Primarily due to cost we will be using [Azure Table Storage](https://docs.microsoft.com/en-us/azure/storage/) for our persistence. Another good reason to use it is the natural fit it has with StreamStone. Because of our EU overlords we will need to be GDPR compliant.

##Communication - WIP
Between our app service and backend can be done using the [Hypertext Application Language (HAL) specification](http://stateless.co/hal_specification.html) (JSON variant for readability).

##Data Migration - WIP
Because we are making a replacement forum we will need to migrate existing data over to our new solution. The current SQL database should be accessible but reading from one database into our persistence is a future concern.

##Discord Integration
Discord offers a [seemingly painless way to shove in a server widget](https://blog.discordapp.com/add-the-discord-widget-to-your-site-d45ffcd718c6). This would be quite nice to have.
