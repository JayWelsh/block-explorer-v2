FROM ghcr.io/fuellabs/fuel-core:v0.10.1

ARG IP=0.0.0.0
ARG PORT=4000
ARG MIN_GAS_PRICE=0
ARG DB_PATH=./mnt/db/

ENV IP="${IP}"
ENV PORT="${PORT}"
ENV DB_PATH="${DB_PATH}"
ENV MIN_GAS_PRICE="${MIN_GAS_PRICE}"

WORKDIR /root/

COPY chainConfig.json .

CMD exec ./fuel-core \
    --ip ${IP} \
    --port ${PORT} \
    --db-path ${DB_PATH} \
    --utxo-validation \
    --min-gas-price ${MIN_GAS_PRICE} \
    --vm-backtrace \
    --predicates \
    --chain ./chainConfig.json

EXPOSE ${PORT}
