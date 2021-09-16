## `aerospike:ce-5.6.0.10`

```console
$ docker pull aerospike@sha256:8b63cd0676fbdd5254b51b0cc84a2a9ade1d7dcc8ebab49a8ce92b7200f6807a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.6.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:e48ccdd4d7a01aa8e2998e82fa8b6c4b2d6ecd11837136abbb5476eed3db5850
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80606260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd592bb96ad0ad1b557f2e7154b38ea2b531a64c1c4f05acba5ae501051621b1`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 03 Sep 2021 01:21:46 GMT
ADD file:4ff85d9f6aa246746912db62dea02eb71750474bb29611e770516a1fcd217add in / 
# Fri, 03 Sep 2021 01:21:46 GMT
CMD ["bash"]
# Thu, 16 Sep 2021 19:19:22 GMT
ENV AEROSPIKE_VERSION=5.6.0.10
# Thu, 16 Sep 2021 19:19:48 GMT
ENV AEROSPIKE_SHA256=66611cfe9eed889fe40a6d57c2f05a67a0ff459d6147776cf907d10df346b387
# Thu, 16 Sep 2021 19:20:06 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Thu, 16 Sep 2021 19:20:07 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Thu, 16 Sep 2021 19:20:07 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Thu, 16 Sep 2021 19:20:07 GMT
EXPOSE 3000 3001 3002
# Thu, 16 Sep 2021 19:20:07 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Thu, 16 Sep 2021 19:20:08 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:a330b6cecb98cd2425fd25fce36669073f593b3176b4ee14731e48c05d678cdd`  
		Last Modified: Fri, 03 Sep 2021 01:28:19 GMT  
		Size: 27.1 MB (27145844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f851332cad0d05a991daba7f6bde1ae60ce8bcc7f780a89b00e8f883fa81d7`  
		Last Modified: Thu, 16 Sep 2021 19:20:43 GMT  
		Size: 53.5 MB (53458397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d57ad62436ba30e207a8714b56c2d6bedae8261cc4f437509c5bbced306c01`  
		Last Modified: Thu, 16 Sep 2021 19:20:34 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6365b7d2fd23fb39e7369a807ad8f5fdfe914b73ab46714712c96c191f1fd39e`  
		Last Modified: Thu, 16 Sep 2021 19:20:34 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
