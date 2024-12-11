

ok i have this generated html page i use in n8n.

I need to add a button to the "actions" section of the salesforce matches.

The button should say, "Set" and when clicked it should make an api call to 

https://n8n.skoopsignage.dev/webhook-test/982hf89h2343juirosldk54?

with url parameters of

orgid=<insert Organization ID>

and the body of the api call should be a json object.
It can be all or some of the following key value pairs:
{
    "intercom_org_id": "string",
    "jira_asset_id": "string",
    "name": "string",
    "salesforce_account_id": "string",
    "skoop_db_org_id": "string",
    "stripe_customer_id": "string"
  }

however we should only include the key value pair that is being set, i.e. the button that is clicked and the label corresponding to the button.

so the final call should be something like 

https://n8n.skoopsignage.dev/webhook-test/982hf89h2343juirosldk54?orgid=10

with a json body of 

{
    "salesforce_account_id": "string"
}


in this case, we get the salesforce account id from the button that is clicked and take the value of the salesforce account entry in the table, similar to how we create the salesforce account view button.
