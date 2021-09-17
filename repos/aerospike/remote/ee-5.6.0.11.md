## `aerospike:ee-5.6.0.11`

```console
$ docker pull aerospike@sha256:06cc5f711b2a813e34bc74d8bb7247c4e6382b7a7f520ebea62c8aea8a65adb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.6.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:de05a6a41292f9b52a7bfd75b3907192b79d1912be72062236db492a29a4f66c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82472480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda4ff480791ffdf171661f5ea475971fe4d4bad8ffbf416454bfcbe14e7ded`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 17 Sep 2021 19:19:17 GMT
ENV AEROSPIKE_VERSION=5.6.0.11
# Fri, 17 Sep 2021 19:19:17 GMT
ENV AEROSPIKE_SHA256=17c73dea4213a587d4d2335f78c2094c0f77369d2311473d6d13ecc07df31aa9
# Fri, 17 Sep 2021 19:19:38 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 17 Sep 2021 19:19:39 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Fri, 17 Sep 2021 19:19:39 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Fri, 17 Sep 2021 19:19:39 GMT
EXPOSE 3000 3001 3002
# Fri, 17 Sep 2021 19:19:39 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 17 Sep 2021 19:19:40 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aead6367e37542bda0896d0d3238e4b95d7a28e9f916b4319429f778d4f12e3`  
		Last Modified: Fri, 17 Sep 2021 19:20:27 GMT  
		Size: 55.3 MB (55324557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027b39d1407c5eb3ed3b613c17b739ee9efdf72ee63875b23bf30b2adac4568a`  
		Last Modified: Fri, 17 Sep 2021 19:20:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d7abe895fb08c99f9f31f9d381514a4d1726ceb489dd6895c42ac845597289`  
		Last Modified: Fri, 17 Sep 2021 19:20:17 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
