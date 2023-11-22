FROM anchore/syft as syft
FROM scratch

ARG TRIPLET=x86_64-unknown-linux-musl

ENTRYPOINT [ "/server" ]
CMD [ "-o" ]
EXPOSE 8080

COPY --from=syft /syft /syft
COPY target/$TRIPLET/release/server /server
