
export APPS_JSON_BASE64=$(base64 -w 0 apps-cardinal.json)

docker build --no-cache --build-arg=APPS_JSON_BASE64=$APPS_JSON_BASE64 --tag=ghcr.io/victorarocha/cardinal-erp:latest --file=images/cardinal-erp/Containerfile .

