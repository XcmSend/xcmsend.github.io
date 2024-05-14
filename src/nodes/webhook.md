# Webhook Node

- A webhook node allows you to receive data from anywhere. 

- A webhook can only be used at the beginning of the workflow. 

- Just generate a webhook endpoint URL, send some data there (via an http request using cURL, or Postman, etc), then when the event object data is received it can be and used your workflow. 

- The event can also trigger you workflow to activate. 



<div style="text-align: center; font-style: italic"> 
    <img src="/img/webhook/webhook-0.png" width="300">

Above is a webhook node that has been dragged on to the canvas. 

</div>


## 1. Create a Webhook Endpoint
<div style="text-align: center; font-style: italic">
    <img src="/img/webhook/webhook.png" width="500">

Create and name a webhook endpoint. 
</div>


## 2. Activate the Webhook. 

To active this endpoint you need to send it some data. It's important what data you send it because the data structure is saved and can be used by downstream nodes in the form of pills. 

### Click "Start Listening"

