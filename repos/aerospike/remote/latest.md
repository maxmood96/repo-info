## `aerospike:latest`

```console
$ docker pull aerospike@sha256:95a5bca1ecbf68515d6283a3465275a7de8fd4dd14777f97f8192945650e9595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:4eed5811a1f8cc650836047e9e260445db2ad4ecf21b45c8af7ebf86e304f570
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83907640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc22888ec931259255fe71363bc6a4d54966d93c7c02c986af1a6394dd4035be`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Wed, 23 Mar 2022 15:19:19 GMT
ENV AEROSPIKE_VERSION=5.7.0.12
# Wed, 23 Mar 2022 15:19:19 GMT
ENV AEROSPIKE_SHA256=a63a6d6d749011a3eb89ca30bb8e48dc122af9a5a87caa854c9ae6da864a1935
# Wed, 23 Mar 2022 15:19:19 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Wed, 23 Mar 2022 15:19:39 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 23 Mar 2022 15:19:40 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Wed, 23 Mar 2022 15:19:40 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Wed, 23 Mar 2022 15:19:40 GMT
EXPOSE 3000 3001 3002
# Wed, 23 Mar 2022 15:19:40 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Wed, 23 Mar 2022 15:19:40 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5504b8ba76ac8c0799541e688ba24bb21c6c6dadd7b0a00bcbc62f93eff7fa77`  
		Last Modified: Wed, 23 Mar 2022 15:20:20 GMT  
		Size: 56.8 MB (56751732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0df782bb0f2b871b5d0a0ae6f8a69cf5f5bf849a8c297e6d3ef9614358e40e8`  
		Last Modified: Wed, 23 Mar 2022 15:20:12 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61ed9ebf64be0f3e2f7f3c096fc7a4b06aacf575a681442b6b66532cf21b269`  
		Last Modified: Wed, 23 Mar 2022 15:20:12 GMT  
		Size: 907.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
