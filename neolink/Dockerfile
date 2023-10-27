FROM quantumentangledandy/neolink:feature-push_mqtt

RUN apt-get update && \
    apt-get install -y \
        jq && \
    apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Copy data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

ENV RUST_LOG neolink=debug

CMD [ "/run.sh" ]
