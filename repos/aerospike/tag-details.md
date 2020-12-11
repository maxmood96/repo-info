<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.0.0.21`](#aerospike50021)
-	[`aerospike:5.1.0.18`](#aerospike51018)
-	[`aerospike:5.2.0.10`](#aerospike52010)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.0.0.21`

```console
$ docker pull aerospike@sha256:49979c0436f8b710f34587f90d419770918b32e289144cb223002f0ff705fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.0.0.21` - linux; amd64

```console
$ docker pull aerospike@sha256:0bd59b0e4cdd720a52fa9c8c7c9e0512d9c6e0ec1b6ded1affe0999c0a0672c7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59783498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4233b7637063d1bdec9e41c9c906b03d60ed761a44e985bfd1e052204159dc3`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:33:38 GMT
ENV AEROSPIKE_VERSION=5.0.0.21
# Fri, 11 Dec 2020 20:33:38 GMT
ENV AEROSPIKE_SHA256=67f3e77588ed17f75da1599f787373bdd2ef032fdc8e479a757b8b3f3289e007
# Fri, 11 Dec 2020 20:33:56 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Fri, 11 Dec 2020 20:33:56 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Fri, 11 Dec 2020 20:33:56 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Fri, 11 Dec 2020 20:33:56 GMT
EXPOSE 3000 3001 3002 3003
# Fri, 11 Dec 2020 20:33:56 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 11 Dec 2020 20:33:57 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271992f3199bc914598b77bdc1085a84593014c8ebf336837d20395e99bd996`  
		Last Modified: Fri, 11 Dec 2020 20:35:07 GMT  
		Size: 37.3 MB (37253586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d468546b08235a1cd1c22903a7b72b44e0fe83e04c731df29c19bb29b3623b`  
		Last Modified: Fri, 11 Dec 2020 20:35:01 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2d16a8cd32663c41ae3635fe58194f1a2e2aeb3a5ce00fdaf71565010ea5a6`  
		Last Modified: Fri, 11 Dec 2020 20:35:01 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.1.0.18`

```console
$ docker pull aerospike@sha256:73272813ca8b4f4a453f0ef30a5adcbc80b465b0ef4250612b1978443bdff1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.1.0.18` - linux; amd64

```console
$ docker pull aerospike@sha256:597345bd71d28d0db385e3581865400912981e4c6f673f73db3978899aef6868
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67216663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9606396a03198508844c242c3d06d192ae91cc3cda3277206c9e4f6549e2b397`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:34:03 GMT
ENV AEROSPIKE_VERSION=5.1.0.18
# Fri, 11 Dec 2020 20:34:03 GMT
ENV AEROSPIKE_SHA256=372d6c8dbdf00226908607d1561d717cd856f384bb6bd87a3269d1bc2533d555
# Fri, 11 Dec 2020 20:34:21 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Fri, 11 Dec 2020 20:34:21 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Fri, 11 Dec 2020 20:34:22 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Fri, 11 Dec 2020 20:34:22 GMT
EXPOSE 3000 3001 3002 3003
# Fri, 11 Dec 2020 20:34:22 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 11 Dec 2020 20:34:22 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c5fb9e9eed65bc154324ad9db1897ff451343cac0fde4e0e5e1b2c7043ea06`  
		Last Modified: Fri, 11 Dec 2020 20:35:20 GMT  
		Size: 44.7 MB (44686748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf0023fe989ed90eb6c5fe521a926f600a13e05b3f0f0c3fcb813969c307393`  
		Last Modified: Fri, 11 Dec 2020 20:35:13 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2747508c3297d7c71233d07a8861fae050ca801cdcde0ccf6418a34a28d8cc`  
		Last Modified: Fri, 11 Dec 2020 20:35:12 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.2.0.10`

```console
$ docker pull aerospike@sha256:2cbe03563f44546bd5d6c70ed953a53224bc150c2a94fa2ec7e758d4d99f8ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.2.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:ffcc6f82106da2bbb1db694e4bd98856590891fcecf1ab4e36fd1b32e03e2eb0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67133627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34a33e05549038c3f0a1a718d9bfe0065cabb66f9e4dc38472238c35ee36721`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:34:28 GMT
ENV AEROSPIKE_VERSION=5.2.0.10
# Fri, 11 Dec 2020 20:34:28 GMT
ENV AEROSPIKE_SHA256=7b765d77cc391d7ea3991c335801972b703e01ac19b9116d266b5c0b57f1ca8d
# Fri, 11 Dec 2020 20:34:47 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Fri, 11 Dec 2020 20:34:47 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Fri, 11 Dec 2020 20:34:47 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Fri, 11 Dec 2020 20:34:47 GMT
EXPOSE 3000 3001 3002 3003
# Fri, 11 Dec 2020 20:34:47 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 11 Dec 2020 20:34:48 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeedefa0514d607e5223cd91ad9f0b67952f575d813658607cc6ad358c54bfa`  
		Last Modified: Fri, 11 Dec 2020 20:35:32 GMT  
		Size: 44.6 MB (44603713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d606ec9198a004ca6e9817da932a950b94a51b55d56ce40adf2a82fb910064d`  
		Last Modified: Fri, 11 Dec 2020 20:35:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfca89a6d881e487ac78fd1a560c3936efe35a5c68cb9dfb2e7dfc7d84c82e3`  
		Last Modified: Fri, 11 Dec 2020 20:35:25 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:2cbe03563f44546bd5d6c70ed953a53224bc150c2a94fa2ec7e758d4d99f8ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:ffcc6f82106da2bbb1db694e4bd98856590891fcecf1ab4e36fd1b32e03e2eb0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67133627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34a33e05549038c3f0a1a718d9bfe0065cabb66f9e4dc38472238c35ee36721`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:34:28 GMT
ENV AEROSPIKE_VERSION=5.2.0.10
# Fri, 11 Dec 2020 20:34:28 GMT
ENV AEROSPIKE_SHA256=7b765d77cc391d7ea3991c335801972b703e01ac19b9116d266b5c0b57f1ca8d
# Fri, 11 Dec 2020 20:34:47 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Fri, 11 Dec 2020 20:34:47 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Fri, 11 Dec 2020 20:34:47 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Fri, 11 Dec 2020 20:34:47 GMT
EXPOSE 3000 3001 3002 3003
# Fri, 11 Dec 2020 20:34:47 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Fri, 11 Dec 2020 20:34:48 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeedefa0514d607e5223cd91ad9f0b67952f575d813658607cc6ad358c54bfa`  
		Last Modified: Fri, 11 Dec 2020 20:35:32 GMT  
		Size: 44.6 MB (44603713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d606ec9198a004ca6e9817da932a950b94a51b55d56ce40adf2a82fb910064d`  
		Last Modified: Fri, 11 Dec 2020 20:35:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfca89a6d881e487ac78fd1a560c3936efe35a5c68cb9dfb2e7dfc7d84c82e3`  
		Last Modified: Fri, 11 Dec 2020 20:35:25 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
