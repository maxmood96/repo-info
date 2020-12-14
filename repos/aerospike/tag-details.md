<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.1.0.19`](#aerospike51019)
-	[`aerospike:5.2.0.11`](#aerospike52011)
-	[`aerospike:5.3.0.2`](#aerospike5302)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.1.0.19`

```console
$ docker pull aerospike@sha256:f25b81d5f9c491e11e88a1ab825aeef489fd483e04fad7236e8832499b262565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.1.0.19` - linux; amd64

```console
$ docker pull aerospike@sha256:7830f85f8d58b15be87f9c919dff0e731481a760b0a71956ab57289e8624dbdc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76357104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f723ef9b411fcdf4151c4ed983be88729a22080ddbcee3fba6474c104c8559`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 20:19:58 GMT
ENV AEROSPIKE_VERSION=5.1.0.19
# Mon, 14 Dec 2020 20:19:58 GMT
ENV AEROSPIKE_SHA256=beeacac98acfccedf9e7ffe923937f69d3c266f528f6a6e676a241ac9f173514
# Mon, 14 Dec 2020 20:20:21 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 14 Dec 2020 20:20:21 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 14 Dec 2020 20:20:21 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 14 Dec 2020 20:20:22 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 14 Dec 2020 20:20:22 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Mon, 14 Dec 2020 20:20:22 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3094321e44e3d35b8335a7030c5df1a07952634cd17eec25cffd11577100085`  
		Last Modified: Mon, 14 Dec 2020 20:21:41 GMT  
		Size: 53.8 MB (53827191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:311924579c5f3fdce36edea0f2db682a6ad27b29d1461158f81f6be651be0d91`  
		Last Modified: Mon, 14 Dec 2020 20:21:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f155a89d5398b53806d5dd84c185fa45fe65e33085baa50df24f6f20987a8348`  
		Last Modified: Mon, 14 Dec 2020 20:21:31 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.2.0.11`

```console
$ docker pull aerospike@sha256:e7e994c8753090879ea97fd0aa18aa48e61b5ea1f9caa880d3574f49664e97a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.2.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:9ae54fa52f093111ad3799f8dc127e4f836dc0239ed0ee3e1c5fc22ce6ec8d2e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76273613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ec5f79bffc9bfb4e307b67a7056cd3ff2897ac9d8bd180acce126ade632a1a`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 20:20:27 GMT
ENV AEROSPIKE_VERSION=5.2.0.11
# Mon, 14 Dec 2020 20:20:27 GMT
ENV AEROSPIKE_SHA256=125988a398a008981079cd7a31c9257c392348415ca14b4eccdb70412031c3be
# Mon, 14 Dec 2020 20:20:50 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 14 Dec 2020 20:20:50 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 14 Dec 2020 20:20:50 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 14 Dec 2020 20:20:51 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 14 Dec 2020 20:20:51 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Mon, 14 Dec 2020 20:20:51 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71f22c74ded034d06652c56b764f68d806d60f51ce06b77a605532dfe8cac97`  
		Last Modified: Mon, 14 Dec 2020 20:21:54 GMT  
		Size: 53.7 MB (53743699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba5bb9388bade9dc0aae6bb0d92fc06f2b4f7d81a2dd3f6ac35be0746c3b6f6`  
		Last Modified: Mon, 14 Dec 2020 20:21:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1033c0f9ec36f310f9133d30bfdf4ba69a85544aa87812f1f12743b22f1e92f`  
		Last Modified: Mon, 14 Dec 2020 20:21:45 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.3.0.2`

```console
$ docker pull aerospike@sha256:4a36344ad0aa5558bfb3075cc701db689831237d743c95bef69b48024ef013c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:628d718c901663c18229fd02b28e06ac7038db074c62b8ee4cd9f9757f4a5c59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74704557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b35556ab7f65ccf44d05b5164530c45f3f1f92204f6cd4b98267c8b8d56465e`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 20:20:57 GMT
ENV AEROSPIKE_VERSION=5.3.0.2
# Mon, 14 Dec 2020 20:20:57 GMT
ENV AEROSPIKE_SHA256=11f33419443e486821608e74bf7db318e184686503043cc1a3e7e07ab90eb059
# Mon, 14 Dec 2020 20:21:19 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 14 Dec 2020 20:21:20 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 14 Dec 2020 20:21:20 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 14 Dec 2020 20:21:20 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 14 Dec 2020 20:21:20 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Mon, 14 Dec 2020 20:21:20 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb9b2d282ca24425006dc718f434682c165c652fac20fedec88636754776c0e`  
		Last Modified: Mon, 14 Dec 2020 20:22:08 GMT  
		Size: 52.2 MB (52174645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db2f7caae59bd95d73fe74c26a6fa7767cc9387d671039aad5b81f18e2226d`  
		Last Modified: Mon, 14 Dec 2020 20:21:59 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9324f2aa3ee701db23764111a044c3a0e027a103763a695d8b54b26e1d956e`  
		Last Modified: Mon, 14 Dec 2020 20:21:59 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:4a36344ad0aa5558bfb3075cc701db689831237d743c95bef69b48024ef013c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:628d718c901663c18229fd02b28e06ac7038db074c62b8ee4cd9f9757f4a5c59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74704557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b35556ab7f65ccf44d05b5164530c45f3f1f92204f6cd4b98267c8b8d56465e`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Mon, 14 Dec 2020 20:20:57 GMT
ENV AEROSPIKE_VERSION=5.3.0.2
# Mon, 14 Dec 2020 20:20:57 GMT
ENV AEROSPIKE_SHA256=11f33419443e486821608e74bf7db318e184686503043cc1a3e7e07ab90eb059
# Mon, 14 Dec 2020 20:21:19 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 14 Dec 2020 20:21:20 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 14 Dec 2020 20:21:20 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 14 Dec 2020 20:21:20 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 14 Dec 2020 20:21:20 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Mon, 14 Dec 2020 20:21:20 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb9b2d282ca24425006dc718f434682c165c652fac20fedec88636754776c0e`  
		Last Modified: Mon, 14 Dec 2020 20:22:08 GMT  
		Size: 52.2 MB (52174645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db2f7caae59bd95d73fe74c26a6fa7767cc9387d671039aad5b81f18e2226d`  
		Last Modified: Mon, 14 Dec 2020 20:21:59 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9324f2aa3ee701db23764111a044c3a0e027a103763a695d8b54b26e1d956e`  
		Last Modified: Mon, 14 Dec 2020 20:21:59 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
