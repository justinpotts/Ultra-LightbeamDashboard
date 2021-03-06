# Ultra-Lightbeam Dashboard + RESTful API
This repository serves as a home for the [Ultra-Lightbeam](https://github.com/FrancescoSTL/Ultra-Lightbeam) Dashboard and RESTful API. The Dashboard will soon allow users to see crowd-sourced data on ad-content load times for major ad networks on the web, while the RESTful API serves as the web-extension's trusty end-point to log benchmarking details to our server. 

## Installing Ultra-Lightbeam Dashboard

Clone the repository by running:

```
git clone https://github.com/FrancescoSTL/ultra-lightbeamdashboard.git
```

Download and install [Node.js](https://nodejs.org/en/download/)

## Running Ultra-Lightbeam Dashboard

Once you've cloned the repo and installed Node.js, you can start sherlock by running:

1. `npm install`
2. `node ./bin/www.js`
3. Navigate to `https://localhost:3000/`

## Testing the Ultra-Lightbeam RESTful API Locally

1. Start running the ultra-lightbeam dashboard as instructed above
2. Run `curl -d 'Data to send' http://localhost:3000/log/`

You should recieve back the message: `Data successfully recieved by Ultra-Lightbeam. Thanks :-).`

Congrats, you just successfully set up the local version of Ultra-Lightbeam's Dashboard!

## Example API JSON

Want to start writing some dashboards? Below you'll find an example (shortened) JSON object we recieved after one user browsed to cnn.com:
```
{"assets":[{"assetCompleteTime":430,"originUrl":"www.cnn.com","adNetworkUrl":"cdn.krxd.net","assetType":"script","fileSize":"16385"},{"assetCompleteTime":456,"originUrl":"www.cnn.com","adNetworkUrl":"ads.rubiconproject.com","assetType":"script","fileSize":"22247"},{"assetCompleteTime":490,"originUrl":"www.cnn.com","adNetworkUrl":"widgets.outbrain.com","assetType":"script","fileSize":"20006"}]}
```