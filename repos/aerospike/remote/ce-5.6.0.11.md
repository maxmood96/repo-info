## `aerospike:ce-5.6.0.11`

```console
$ docker pull aerospike@sha256:3e8aee339716f69a26241845bb871a249d99a9ff1ea553c4d99464e2d46425a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.6.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:49a291b733188f024afb285a77285548a50e4967113f4f8bd3d1d9b589c6e32e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80604538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea44d2ff1eb98db2ea449ef982e019a158055e64a412e6af409a1c8a467b090b`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Fri, 17 Sep 2021 19:19:17 GMT
ENV AEROSPIKE_VERSION=5.6.0.11
# Fri, 17 Sep 2021 19:19:47 GMT
ENV AEROSPIKE_SHA256=08dbef7b8a4dd4fabdf4a04f3fc1e6b5c124d7084f7faa6b352fd7689ede1d1f
# Fri, 17 Sep 2021 19:20:07 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Fri, 17 Sep 2021 19:20:07 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Fri, 17 Sep 2021 19:20:07 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Fri, 17 Sep 2021 19:20:08 GMT
EXPOSE 3000 3001 3002
# Fri, 17 Sep 2021 19:20:08 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 17 Sep 2021 19:20:08 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca033892737fbc83b8f72c0902e6b09bf8ed156cc0f5caa3b5f36605edc940f`  
		Last Modified: Fri, 17 Sep 2021 19:20:44 GMT  
		Size: 53.5 MB (53456674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb30a240b6d66c50e68dd6cbed9245882dffba82fb7ba4b8050bb52d0ed9d97`  
		Last Modified: Fri, 17 Sep 2021 19:20:34 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84e47c7947897631ff3f35bba5e58c0de4cbc34a3edafd38aca55ba274e4558`  
		Last Modified: Fri, 17 Sep 2021 19:20:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
