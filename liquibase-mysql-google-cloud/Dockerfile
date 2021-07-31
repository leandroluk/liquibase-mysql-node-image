FROM leandroluk/liquibase-mysql

# install dependencies
RUN apk add --update --no-cache --quiet gettext make ca-certificates wget openssl python3 py3-pip curl jq py-pip git &&\
    update-ca-certificates

# install google cloud
RUN wget https://dl.google.com/dl/cloudsdk/release/google-cloud-sdk.tar.gz &&\
    mv google-cloud-sdk.tar.gz / &&\
    tar zxf /google-cloud-sdk.tar.gz -C / &&\
    /google-cloud-sdk/install.sh &&\
    rm /google-cloud-sdk.tar.gz &&\
    export PATH=/google-cloud-sdk/bin:${PATH} &&\
    gcloud --quiet components update

# install cloud sql proxu
RUN wget https://dl.google.com/cloudsql/cloud_sql_proxy.linux.amd64 -O cloud_sql_proxy &&\
    chmod +x cloud_sql_proxy