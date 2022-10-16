# Twiiter-hashtag-crawler-on-Dataproc-PySpark


##Create cluster 

gcloud beta dataproc clusters create hw2 \
--region=us-east1 \
--optional-components=ANACONDA,JUPYTER \
--image-version=1.4 \
--enable-component-gateway \
--initialization-actions=gs://dataproc-initialization-actions/python/pip-install.sh,gs://dataproc-initialization-actions/connectors/connectors.sh \
--metadata "PIP_PACKAGES=requests_oauthlib google-cloud-bigquery tweepy==3.1.0" \
--metadata gcs-connector-version=1.9.16 \
--metadata bigquery-connector-version=1.0.0 \
--project big-data-6893-362317 \
--bucket 6893_data_taolue \
--single-node
