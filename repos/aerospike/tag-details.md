<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.3.0.14`](#aerospike53014)
-	[`aerospike:5.4.0.9`](#aerospike5409)
-	[`aerospike:5.5.0.7`](#aerospike5507)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.3.0.14`

```console
$ docker pull aerospike@sha256:c52cdb6851e6c7fd20459f504fc21c00b98e1ac1f79d42fe2fc0e8bbe6e3a43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.14` - linux; amd64

```console
$ docker pull aerospike@sha256:a5736b02208a205e0d10e4842be5ae801b53712b2342792fdf1a099caebd36f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74708448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a57f360125e2648f436fd4807badf520acc5602b8bb5eaf61fb61934b84434c`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:08:37 GMT
ENV AEROSPIKE_VERSION=5.3.0.14
# Sat, 10 Apr 2021 06:08:37 GMT
ENV AEROSPIKE_SHA256=9a0d4f167d89a307822ed66f80da8b6feedb869c058baa1d0eab1891207999d5
# Sat, 10 Apr 2021 06:09:15 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 10 Apr 2021 06:09:16 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 10 Apr 2021 06:09:16 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 10 Apr 2021 06:09:16 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 10 Apr 2021 06:09:17 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 10 Apr 2021 06:09:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b105131748fd9387993ae829d007f4aee9a1cf1903cd8e805cdd46b17177bd7`  
		Last Modified: Sat, 10 Apr 2021 06:10:59 GMT  
		Size: 52.2 MB (52178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d28968a298f55a697c72cc6c9965bb54a894993e4c6051cc9e8969395e292c4`  
		Last Modified: Sat, 10 Apr 2021 06:10:49 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae4dd6572361c364ac7a1b2d94cac338e71a6ebb336526f6c5b1220f702a6a1`  
		Last Modified: Sat, 10 Apr 2021 06:10:50 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.4.0.9`

```console
$ docker pull aerospike@sha256:41d4962db3c1066876a1d6bc979ebfab07d12c9d2318ae076e3ca5fbdeb6cc55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.4.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:295e5c0b71e10326501005827aa7bbcff2830a8f38042d6a9c714b0d09735166
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74731323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee9861cc36fa0387b52a58a74c36a03815f02827b33a5c0e57a968027cea51e`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:09:28 GMT
ENV AEROSPIKE_VERSION=5.4.0.9
# Sat, 10 Apr 2021 06:09:29 GMT
ENV AEROSPIKE_SHA256=6262abe20f3ade81beecbc6b46766e0d63fb8c31c0ec1e20f543ff023f9479a3
# Sat, 10 Apr 2021 06:09:59 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 10 Apr 2021 06:09:59 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 10 Apr 2021 06:10:00 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 10 Apr 2021 06:10:00 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 10 Apr 2021 06:10:00 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 10 Apr 2021 06:10:00 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e095408aff281f7fafdcafb8402d5f245de9db7349fcef313a517f35c72eda45`  
		Last Modified: Sat, 10 Apr 2021 06:11:17 GMT  
		Size: 52.2 MB (52201005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538c0762d56bed46a0c2eb2f18b9ff4dca54b509ef4a7128fbffc6b86c80f3e3`  
		Last Modified: Sat, 10 Apr 2021 06:11:07 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172ae364fbe5779a86d76e66c0be73c1a0a931f042e995c8fc2119cb373ce51f`  
		Last Modified: Sat, 10 Apr 2021 06:11:07 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.5.0.7`

```console
$ docker pull aerospike@sha256:8f7c5a533c457b7a7a4e99341674ca0e8ee17ff74e1122f2d6532d06fec49c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.5.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:9712a70abbc455a29035aff519bfcff2fd13f2395e05661611b9e1eb4ca228d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74775088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5377e1918cb0ef0e71ba78d7e6e8d115da34c94e8dec79d193f82e18ab34fc51`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:10:04 GMT
ENV AEROSPIKE_VERSION=5.5.0.7
# Sat, 10 Apr 2021 06:10:04 GMT
ENV AEROSPIKE_SHA256=43cc7c0b135fa8a0186a8ce9b5f923660e59e3ef8ec32a742a5b533c1d3caaa3
# Sat, 10 Apr 2021 06:10:29 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 10 Apr 2021 06:10:29 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 10 Apr 2021 06:10:30 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 10 Apr 2021 06:10:30 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 10 Apr 2021 06:10:30 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 10 Apr 2021 06:10:30 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad8b703df239d9ef1039174116954bc74604106d065f0f0e3773f027ac7f6dd`  
		Last Modified: Sat, 10 Apr 2021 06:11:35 GMT  
		Size: 52.2 MB (52244768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20772210df85e3911e56d8d8794582c95c062e1782010df96b349cfc1683a516`  
		Last Modified: Sat, 10 Apr 2021 06:11:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db8ab26f8f395bf6a55411a5485990b23068c5d9b7463f8449e3c31b3e06571`  
		Last Modified: Sat, 10 Apr 2021 06:11:25 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:8f7c5a533c457b7a7a4e99341674ca0e8ee17ff74e1122f2d6532d06fec49c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:9712a70abbc455a29035aff519bfcff2fd13f2395e05661611b9e1eb4ca228d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74775088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5377e1918cb0ef0e71ba78d7e6e8d115da34c94e8dec79d193f82e18ab34fc51`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:10:04 GMT
ENV AEROSPIKE_VERSION=5.5.0.7
# Sat, 10 Apr 2021 06:10:04 GMT
ENV AEROSPIKE_SHA256=43cc7c0b135fa8a0186a8ce9b5f923660e59e3ef8ec32a742a5b533c1d3caaa3
# Sat, 10 Apr 2021 06:10:29 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 10 Apr 2021 06:10:29 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 10 Apr 2021 06:10:30 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 10 Apr 2021 06:10:30 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 10 Apr 2021 06:10:30 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 10 Apr 2021 06:10:30 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad8b703df239d9ef1039174116954bc74604106d065f0f0e3773f027ac7f6dd`  
		Last Modified: Sat, 10 Apr 2021 06:11:35 GMT  
		Size: 52.2 MB (52244768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20772210df85e3911e56d8d8794582c95c062e1782010df96b349cfc1683a516`  
		Last Modified: Sat, 10 Apr 2021 06:11:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db8ab26f8f395bf6a55411a5485990b23068c5d9b7463f8449e3c31b3e06571`  
		Last Modified: Sat, 10 Apr 2021 06:11:25 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
