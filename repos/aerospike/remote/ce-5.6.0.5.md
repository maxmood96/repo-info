## `aerospike:ce-5.6.0.5`

```console
$ docker pull aerospike@sha256:29fd51c1f9347550bbb196b8fe8f7de7a666e187f494fc00c79fc0b7db6ded62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ce-5.6.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:45826eade4fda2837ef1d9a1d6083884bd306a6a8023c8b133d47084389c519c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80604786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9398428e2aba0f6ca891e0fa27fccbea574c65702fb4e8c499297c48a703f16c`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:48:39 GMT
ENV AEROSPIKE_VERSION=5.6.0.5
# Wed, 23 Jun 2021 00:49:15 GMT
ENV AEROSPIKE_SHA256=a173e5fabe9a0c6f51d717f0989b26fb22313f9de971de9ac296209123e654ef
# Wed, 23 Jun 2021 00:49:42 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 23 Jun 2021 00:49:43 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Wed, 23 Jun 2021 00:49:43 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Wed, 23 Jun 2021 00:49:43 GMT
EXPOSE 3000 3001 3002
# Wed, 23 Jun 2021 00:49:43 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 23 Jun 2021 00:49:44 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9dea05ba2dbe8dc748a6b9ff366b4d744d0b1a3dfd950a233f84689b7cbf9b`  
		Last Modified: Wed, 23 Jun 2021 00:50:28 GMT  
		Size: 53.5 MB (53456915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa3f220712dd799a2cee4d259ffa0a874c7b23fdc05027d1be1ea05fa369b70`  
		Last Modified: Wed, 23 Jun 2021 00:50:17 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2092cad4b2f07f5c4b582b00130e8235eba4d922f1c496051c1401c5432fab`  
		Last Modified: Wed, 23 Jun 2021 00:50:17 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
