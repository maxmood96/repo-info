<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.1.0.23`](#aerospike51023)
-	[`aerospike:5.2.0.15`](#aerospike52015)
-	[`aerospike:5.3.0.6`](#aerospike5306)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.1.0.23`

```console
$ docker pull aerospike@sha256:457c00df02123d9b8309c3c491fb5a8da6b8aee55042541628886de78a7b5151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.1.0.23` - linux; amd64

```console
$ docker pull aerospike@sha256:2d658b8288b3185edc78b2bd0394fea035ecfbfc51cc1bd95604fece7427739b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76360811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a831ab9698a9e1f86b31f9919f002647f0c7689136b5877dbbe07b72a125bb7`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:46:14 GMT
ENV AEROSPIKE_VERSION=5.1.0.23
# Tue, 12 Jan 2021 03:46:15 GMT
ENV AEROSPIKE_SHA256=18081de8fc495cbb0dbeedad0dc91374320d88838c887c3f4708e06f84cd98a6
# Tue, 12 Jan 2021 03:46:41 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 12 Jan 2021 03:46:41 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Jan 2021 03:46:41 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 12 Jan 2021 03:46:42 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 12 Jan 2021 03:46:42 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Jan 2021 03:46:42 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10dd2ac8629c6cf6b61ea81228b89922d2e6c11c138c4b94ac18859d27258290`  
		Last Modified: Tue, 12 Jan 2021 03:48:18 GMT  
		Size: 53.8 MB (53830147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3a7ce6cfcf3a6cf00b9646b4c7b69658540d743c8ab7c6093fd09065fa134d`  
		Last Modified: Tue, 12 Jan 2021 03:48:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bd1a1f7c0d57bac59e3b07ff2156f5fbe64ccc6165707580cf0c7ac20ed522`  
		Last Modified: Tue, 12 Jan 2021 03:48:06 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.2.0.15`

```console
$ docker pull aerospike@sha256:24f4566ba193a81d2e679960b7ab9d0d2cd918f54b2f28727c91cac17e48e173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.2.0.15` - linux; amd64

```console
$ docker pull aerospike@sha256:026587fd703cf97015475ba2c0330cdedf4e4a5995d884a71fa18d257884fc45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76279366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5384c411b72a4611212f5d337e5808326a66b9ad254c5c53807ddd901f0d1ab6`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:46:49 GMT
ENV AEROSPIKE_VERSION=5.2.0.15
# Tue, 12 Jan 2021 03:46:49 GMT
ENV AEROSPIKE_SHA256=06464ca5f9ddc26166a10af9aaa42db880423cd64e507c163ec6ceb010aaaae3
# Tue, 12 Jan 2021 03:47:14 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 12 Jan 2021 03:47:14 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Jan 2021 03:47:15 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 12 Jan 2021 03:47:15 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 12 Jan 2021 03:47:15 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Jan 2021 03:47:15 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2562163e301119cf1d0fc6b79cd4e5578e868683c18139bc0f6b677fa7d603`  
		Last Modified: Tue, 12 Jan 2021 03:48:35 GMT  
		Size: 53.7 MB (53748705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9bb0cd3596b7fb727bdbc29b0a16c9b042732191eb4ef53313079c0e30a4fc`  
		Last Modified: Tue, 12 Jan 2021 03:48:25 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2419274b8bea066a63c72527d3685664cfa83971dff885faf1d52caae3b78258`  
		Last Modified: Tue, 12 Jan 2021 03:48:25 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.3.0.6`

```console
$ docker pull aerospike@sha256:32e56a5bf5985bd18c383bacb725b8464a7d244ded7f427cf67fe9fff410636a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.6` - linux; amd64

```console
$ docker pull aerospike@sha256:ed91f1bb3b8d35345251418a627e2f402f0eac9366e858bf74775079d04ce53f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa936e7c99dd618bef0b3bea593afd62a06000a2850919a05012513fc0c87355`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:47:23 GMT
ENV AEROSPIKE_VERSION=5.3.0.6
# Tue, 12 Jan 2021 03:47:23 GMT
ENV AEROSPIKE_SHA256=f8d19a6274923c3585810cdbdcac0aa3c3aaa507f032c6733c0168692bb188c5
# Tue, 12 Jan 2021 03:47:50 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 12 Jan 2021 03:47:50 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Jan 2021 03:47:50 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 12 Jan 2021 03:47:50 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 12 Jan 2021 03:47:51 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Jan 2021 03:47:51 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03aa6a67cd971ae107ff3b1d08ce3e8b8e523cc73977bb3af7fc77298f5bf1b8`  
		Last Modified: Tue, 12 Jan 2021 03:48:59 GMT  
		Size: 52.2 MB (52177170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1eb842f1b2f21886cccf540ab2d4bf5cfae1721e79845e9b7a606b1077a2ca`  
		Last Modified: Tue, 12 Jan 2021 03:48:51 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1ac9951efe779e44760f07a5779c04736156b1f2011ad7340d18527a6fcb46`  
		Last Modified: Tue, 12 Jan 2021 03:48:52 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:32e56a5bf5985bd18c383bacb725b8464a7d244ded7f427cf67fe9fff410636a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:ed91f1bb3b8d35345251418a627e2f402f0eac9366e858bf74775079d04ce53f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa936e7c99dd618bef0b3bea593afd62a06000a2850919a05012513fc0c87355`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 03:47:23 GMT
ENV AEROSPIKE_VERSION=5.3.0.6
# Tue, 12 Jan 2021 03:47:23 GMT
ENV AEROSPIKE_SHA256=f8d19a6274923c3585810cdbdcac0aa3c3aaa507f032c6733c0168692bb188c5
# Tue, 12 Jan 2021 03:47:50 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 12 Jan 2021 03:47:50 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Jan 2021 03:47:50 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 12 Jan 2021 03:47:50 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 12 Jan 2021 03:47:51 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Jan 2021 03:47:51 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03aa6a67cd971ae107ff3b1d08ce3e8b8e523cc73977bb3af7fc77298f5bf1b8`  
		Last Modified: Tue, 12 Jan 2021 03:48:59 GMT  
		Size: 52.2 MB (52177170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1eb842f1b2f21886cccf540ab2d4bf5cfae1721e79845e9b7a606b1077a2ca`  
		Last Modified: Tue, 12 Jan 2021 03:48:51 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1ac9951efe779e44760f07a5779c04736156b1f2011ad7340d18527a6fcb46`  
		Last Modified: Tue, 12 Jan 2021 03:48:52 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
