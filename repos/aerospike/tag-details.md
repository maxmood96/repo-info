<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.1.0.23`](#aerospike51023)
-	[`aerospike:5.2.0.15`](#aerospike52015)
-	[`aerospike:5.3.0.6`](#aerospike5306)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.1.0.23`

```console
$ docker pull aerospike@sha256:7e5c3fa7e5f642962728275998dabe91890f596d041e3de4cdd4c6b6bf23162e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.1.0.23` - linux; amd64

```console
$ docker pull aerospike@sha256:621abffe78baf70a9b1fa9acfde409be4a12f5309ca05273709ce5ca6522c788
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76360140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111ae3e33f57be0e2de2863fbdd4377645dd6480e51fa0b7d41f14b88e96a4bb`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:20:33 GMT
ENV AEROSPIKE_VERSION=5.1.0.23
# Tue, 12 Jan 2021 00:20:33 GMT
ENV AEROSPIKE_SHA256=18081de8fc495cbb0dbeedad0dc91374320d88838c887c3f4708e06f84cd98a6
# Tue, 12 Jan 2021 00:20:55 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 12 Jan 2021 00:20:56 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Jan 2021 00:20:56 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 12 Jan 2021 00:20:56 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 12 Jan 2021 00:20:56 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Jan 2021 00:20:56 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bb8386a207a0b7b58d772fd43d99aa6aca4d99e3382efd28199964154a7f93`  
		Last Modified: Tue, 12 Jan 2021 00:22:16 GMT  
		Size: 53.8 MB (53830228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69afb819a134518d0063855c308879bd0f06c1b81768906ae40988e2d101bcb9`  
		Last Modified: Tue, 12 Jan 2021 00:22:08 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a396db1e6381e9cf2050d0479e08abd0fadb67ddf245400f8c0b579db39446a1`  
		Last Modified: Tue, 12 Jan 2021 00:22:07 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.2.0.15`

```console
$ docker pull aerospike@sha256:d8bd87968e7a7db7de3df3b3091ca7212fe754f66b966b0f63610be2573aaafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.2.0.15` - linux; amd64

```console
$ docker pull aerospike@sha256:184c31ec891d6fce2658f7b9736606e2ea494cd1e71e61e77408684b9e5ae61e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76278455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4926fedd847a45a18134f6739eff7e8543f17dd7d8d5be4092fc4893a57c523`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:21:02 GMT
ENV AEROSPIKE_VERSION=5.2.0.15
# Tue, 12 Jan 2021 00:21:02 GMT
ENV AEROSPIKE_SHA256=06464ca5f9ddc26166a10af9aaa42db880423cd64e507c163ec6ceb010aaaae3
# Tue, 12 Jan 2021 00:21:24 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 12 Jan 2021 00:21:25 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Jan 2021 00:21:25 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 12 Jan 2021 00:21:25 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 12 Jan 2021 00:21:25 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Jan 2021 00:21:25 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868e193d62acd45d10d24d60427c7fb6867d5f17290c19fbcf6f6c2764b74b78`  
		Last Modified: Tue, 12 Jan 2021 00:22:29 GMT  
		Size: 53.7 MB (53748540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558ed5d2ef410fb48bd5576b0ca76d41d9ea3691e9ee6a8efd71e04c93c47ae1`  
		Last Modified: Tue, 12 Jan 2021 00:22:22 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb546a146adb97e826830c505c0ca6a575807f61563409e51cc6ce4d3c3bfa57`  
		Last Modified: Tue, 12 Jan 2021 00:22:21 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.3.0.6`

```console
$ docker pull aerospike@sha256:bb37c0dadc90754744c3c22cd6397fd9afd920fce320b8cd3e62769dd486733e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.6` - linux; amd64

```console
$ docker pull aerospike@sha256:3b8a13201f6efe83d2fc01806cc5c5c21d5c177df007a65ee08a5c25899ee219
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db413a561186e4bfeb27f54039fecbff828ca5c1a5982f5342f1cd10a9014d52`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:21:31 GMT
ENV AEROSPIKE_VERSION=5.3.0.6
# Tue, 12 Jan 2021 00:21:31 GMT
ENV AEROSPIKE_SHA256=f8d19a6274923c3585810cdbdcac0aa3c3aaa507f032c6733c0168692bb188c5
# Tue, 12 Jan 2021 00:21:54 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 12 Jan 2021 00:21:54 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Jan 2021 00:21:54 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 12 Jan 2021 00:21:54 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 12 Jan 2021 00:21:55 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Jan 2021 00:21:55 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88a7a594e66f9bebdf8a26517efb1c122452ca2f31b8902b38ac3ab16f6950c`  
		Last Modified: Tue, 12 Jan 2021 00:22:46 GMT  
		Size: 52.2 MB (52177504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965975e1febd6ec81b32165c9475c12d4d9cae8bd8364bdb950bd63236510628`  
		Last Modified: Tue, 12 Jan 2021 00:22:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574e5a66699492afe0747311a4d25dca3658dbdd45a3e72fe194adbf2c64f597`  
		Last Modified: Tue, 12 Jan 2021 00:22:36 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:bb37c0dadc90754744c3c22cd6397fd9afd920fce320b8cd3e62769dd486733e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:3b8a13201f6efe83d2fc01806cc5c5c21d5c177df007a65ee08a5c25899ee219
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db413a561186e4bfeb27f54039fecbff828ca5c1a5982f5342f1cd10a9014d52`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:21:31 GMT
ENV AEROSPIKE_VERSION=5.3.0.6
# Tue, 12 Jan 2021 00:21:31 GMT
ENV AEROSPIKE_SHA256=f8d19a6274923c3585810cdbdcac0aa3c3aaa507f032c6733c0168692bb188c5
# Tue, 12 Jan 2021 00:21:54 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 12 Jan 2021 00:21:54 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Jan 2021 00:21:54 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 12 Jan 2021 00:21:54 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 12 Jan 2021 00:21:55 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Jan 2021 00:21:55 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88a7a594e66f9bebdf8a26517efb1c122452ca2f31b8902b38ac3ab16f6950c`  
		Last Modified: Tue, 12 Jan 2021 00:22:46 GMT  
		Size: 52.2 MB (52177504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965975e1febd6ec81b32165c9475c12d4d9cae8bd8364bdb950bd63236510628`  
		Last Modified: Tue, 12 Jan 2021 00:22:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574e5a66699492afe0747311a4d25dca3658dbdd45a3e72fe194adbf2c64f597`  
		Last Modified: Tue, 12 Jan 2021 00:22:36 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
