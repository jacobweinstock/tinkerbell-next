# get initramfs-x86_64 and vmlinuz-x86_64 from OSIE and hook
# put them in their respective directories of bootloaders/
FROM scratch
COPY ./osie /bootloaders/osie/
COPY ./hook /bootloaders/hook/
COPY linuxkit-linux-amd64 /

EXPOSE 9090
ENTRYPOINT ["/linuxkit-linux-amd64", "serve", "-port", ":9090", "-directory", "/bootloaders"]