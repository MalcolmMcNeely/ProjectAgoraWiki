Project Agora is an bespoke internet forum board catered for World of Warcraft guilds. In addition to basic forum requirements there is a need to build guild specific tools for raid and information management.

#Technologies
We are investing heavily in Microsoft Azure because we are cool kids who do cool things. However, because this project will reach go beyond proof of concept into product, the costs of running this is a concern when choosing technologies. This solution does not need to scale, we expect approx 50 - 100 active users, so this doesn't need to be an explicit concern.

##[Azure App Service](https://docs.microsoft.com/en-us/azure/app-service/)
We will use an Azure App Service (Platform as a Service) to serve up a [ReactJS](https://reactjs.org/docs/getting-started.html)-based front end. App Services run on an [App Service Plan](https://docs.microsoft.com/en-us/azure/app-service/overview-hosting-plans) and having a basic plan [will cost £0.056](https://azure.microsoft.com/en-us/pricing/details/app-service/windows/) at time of writing.

##[Azure Functions](https://docs.microsoft.com/en-us/azure/azure-functions/functions-overview)
This will act as our serverless (Functions as a Service) backend which will interact with our persistent data. This allows us to run code on-demand without having to provision or manage infrastructure and we only pay for the time spent running our code.

##Authentication
[Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/) is, to my knowledge, free but we also have the option in utilizing Blizzard's [Battle.net OAuth2 API](https://develop.battle.net/documentation/guides/using-oauth) which will require us to register something-or-other at the [Battle.net developer portal](https://develop.battle.net/). An example of how to use Blizzard's authentication in NodeJS can be found [here](https://github.com/Blizzard/passport-bnet). If we do pursue this route then we will need to provide the ability for forum admin to override forum access in case of a user account being compromised.

# Ubiquitous Language
