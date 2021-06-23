<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-5.6.0.5`](#aerospikece-5605)
-	[`aerospike:ee-5.6.0.5`](#aerospikeee-5605)

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

## `aerospike:ee-5.6.0.5`

```console
$ docker pull aerospike@sha256:f2c761676b7b11878c512bb2e8bb528255df6c87953a5a7acc5dfd6967e05d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ee-5.6.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:6e5f65c58f58284ca6bcfeba84993d7c55bea74b263092ca3d105ddf22f0b796
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82468478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2774f2bc417f18e982f817d6402f826bc11281520eb7644d37e5fd566e295a`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:48:39 GMT
ENV AEROSPIKE_VERSION=5.6.0.5
# Wed, 23 Jun 2021 00:48:39 GMT
ENV AEROSPIKE_SHA256=4beb4c5858e24736c9414da70a74e3c29a8d2c796bf1c3982cc502661f892bf1
# Wed, 23 Jun 2021 00:49:09 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 23 Jun 2021 00:49:10 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Wed, 23 Jun 2021 00:49:10 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Wed, 23 Jun 2021 00:49:10 GMT
EXPOSE 3000 3001 3002
# Wed, 23 Jun 2021 00:49:11 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 23 Jun 2021 00:49:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b531ee452848eb7f1034f0572f2f70a865e5a50e87bb69c5a4c40fcff4294da`  
		Last Modified: Wed, 23 Jun 2021 00:50:09 GMT  
		Size: 55.3 MB (55320547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a240b8cba9df11006062b08a1c108ecec8ed30eb1da8cf61b0a6df4a68fd1575`  
		Last Modified: Wed, 23 Jun 2021 00:49:58 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d68a7352d718855abd5390a452d2a6374daecbb9e2cc2b4dd68eb65349a91b2`  
		Last Modified: Wed, 23 Jun 2021 00:49:58 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
