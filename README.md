#Summary

This repo contains various templates used for First Data email confirmations. The templates utilize handlebars.js.

#Sending Test Emails

##Prereqs for testing

- Java Runtime (8, or latest should work fine)

Navigate to the development directory and run `java -jar handlebars-proto-2.0.0.jar` to get usage details.

##Process

When developing/changing templates, you may find it useful to send test emails before deploying your changes. Use the following steps to test:

- Update the email template file you'd like as necessary
- Ensure you have an example .json file in the root of the project that is the same name as the template you are testing. For example, if testing gifting-email-template.hbs, there should be a gifting-email-template.json in the same directory (root). It's helpful to grab this JSON from the actual request. See the order-placed-email-template.json.example for an example.
- Run `java -jar handlebars-proto-2.0.0.jar -dir path/to/templates/`. In the case of being in the development directory in this project, the command would be: `java -jar handlebars-proto-2.0.0.jar -dir ../../EmailTemplates/`
- Visit the URL that the command instructs you