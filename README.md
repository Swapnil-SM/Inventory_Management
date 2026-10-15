# Location Insights Demo

The idea is you lookup a location and we show you a number of insights about it using our Location Insights product.

## Running the app

To run the app locally:

```
$ cd streamlit-location-insights-demo
$ python3 -m venv .venv
$ 
$ source .venv/bin/activate
$ pip install --upgrade pip
$ pip install -r requirements.txt
$ 
$ streamlit run main.py
```

You'll need to get an API token by following the instructions at [https://docs.predicthq.com/api/authenticating](https://docs.predicthq.com/api/authenticating) and create a [Streamlit secrets](https://docs.streamlit.io/streamlit-community-cloud/get-started/deploy-an-app/connect-to-data-sources/secrets-management) file `.streamlit/secrets.toml` with the following contents:

```
api_key = "<your API token>"
groq_api_key = "<your Groq API key>"

# Keep this only if another part of the app needs Google Places later.
google_api_key = "<your Google API key>"

title = "Discover and unlock the power of event intelligence for your locations:"
suggested_radius_industry = "accommodation"
```

The current address lookup uses OpenStreetMap, so `google_api_key` is not required to run this version. Keep `secrets.toml` private and run the app from the project folder with `streamlit run main.py`.

