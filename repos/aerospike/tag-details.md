<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.1.0.25`](#aerospike51025)
-	[`aerospike:5.2.0.17`](#aerospike52017)
-	[`aerospike:5.3.0.8`](#aerospike5308)
-	[`aerospike:5.4.0.3`](#aerospike5403)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.1.0.25`

```console
$ docker pull aerospike@sha256:be0712da6461db10a480b47e8529ec69795466dad48ae923f4eac6e7518e110a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.1.0.25` - linux; amd64

```console
$ docker pull aerospike@sha256:b29349386d8e667e25d44311d2eaa47af2a4716593f516aeb66ac5f1f95b752b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76362255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152c7ca80ae99d79aff472305ff20d6973f286a551228a6ced6c550bfc97a579`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Wed, 27 Jan 2021 22:00:34 GMT
ENV AEROSPIKE_VERSION=5.1.0.25
# Wed, 27 Jan 2021 22:00:34 GMT
ENV AEROSPIKE_SHA256=1c6e2aa92a86a31fcfca1e8597ae81b6a2e9d16557722b8ff3cd12be9e751401
# Wed, 27 Jan 2021 22:00:58 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 27 Jan 2021 22:00:59 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 27 Jan 2021 22:00:59 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 27 Jan 2021 22:00:59 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 27 Jan 2021 22:00:59 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 27 Jan 2021 22:01:00 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38b89d7460de718fe1099d8b18c5036d3de3f394dec9882343fe0cb29970752`  
		Last Modified: Wed, 27 Jan 2021 22:02:56 GMT  
		Size: 53.8 MB (53831596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f216a273a6c6d33df43b32a3525ce77e37c277792f64fc3ed2c115e72ab605d9`  
		Last Modified: Wed, 27 Jan 2021 22:02:46 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4af2d5fbb88539b9653dfff9d791ba7bd26ada7d98aae713173acce9cb0c84`  
		Last Modified: Wed, 27 Jan 2021 22:02:46 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.2.0.17`

```console
$ docker pull aerospike@sha256:2506d34084841b81bae2452bb7a7cd570d816681f259dc92b8ab23f4820be3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.2.0.17` - linux; amd64

```console
$ docker pull aerospike@sha256:478f308f60c790c0bdb841de8844a41aabf1336fcd1069725d8985f46fac1aae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76281180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d2de50c3d8ee2b6dce1becaf4572a5a55b568081b084ea0278a426a6c72e8f`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Wed, 27 Jan 2021 22:01:08 GMT
ENV AEROSPIKE_VERSION=5.2.0.17
# Wed, 27 Jan 2021 22:01:08 GMT
ENV AEROSPIKE_SHA256=e23d065fff9306a9bd532a2d08844f8a3cb751c79c094d3431f5f7cc1f61c3b7
# Wed, 27 Jan 2021 22:01:32 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 27 Jan 2021 22:01:33 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 27 Jan 2021 22:01:33 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 27 Jan 2021 22:01:33 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 27 Jan 2021 22:01:33 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 27 Jan 2021 22:01:33 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e2048023e315097e9bdadbf2c5c00e4f95014f404ed71adaaee207d40352f3`  
		Last Modified: Wed, 27 Jan 2021 22:03:09 GMT  
		Size: 53.8 MB (53750520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e13b119cd670dc98511e55e3c936c3fabac3db48c790831d759ce70a6e860f7`  
		Last Modified: Wed, 27 Jan 2021 22:03:01 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f66fbfc02e9062699382d04e2253559111333190ab20f552c8b917afaaaad1`  
		Last Modified: Wed, 27 Jan 2021 22:03:01 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.3.0.8`

```console
$ docker pull aerospike@sha256:c38287c88cf8a91e77a3c9e241d63d2bce8bee8b2071f1a9ea950f40ac78045d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:584772007e2e5ee12f1f8fe5d2efc1cbcb571f597012d4b7ee1c8ebc4d3cb3b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74711365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c09463ae00a5c213a2c0aa9427de82a286bf8b3aaf6a811d01aa115fa23bde`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Wed, 27 Jan 2021 22:01:37 GMT
ENV AEROSPIKE_VERSION=5.3.0.8
# Wed, 27 Jan 2021 22:01:37 GMT
ENV AEROSPIKE_SHA256=9b192d8ad06e92da180800b810e970c18056f70db4dc3ffcc2441a4171fe7895
# Wed, 27 Jan 2021 22:02:01 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 27 Jan 2021 22:02:01 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 27 Jan 2021 22:02:01 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 27 Jan 2021 22:02:02 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 27 Jan 2021 22:02:02 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 27 Jan 2021 22:02:02 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea40da0e6737282412a66cd53038e635043e7238b1dc5da7bcf509d18230fe94`  
		Last Modified: Wed, 27 Jan 2021 22:03:22 GMT  
		Size: 52.2 MB (52180705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3668e8300b005e19c6ba28f03831013559a8d343124c28efb4fb8174a06198c`  
		Last Modified: Wed, 27 Jan 2021 22:03:12 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a977b3c2b4a9ea4e28defbc9b58865196c2c75a69028f139f843570d7b10c658`  
		Last Modified: Wed, 27 Jan 2021 22:03:13 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.4.0.3`

```console
$ docker pull aerospike@sha256:4e365ec05b08118418d83d7df09baeaea064e1760b37e1abf50e327f1050435c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.4.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:ac3c1bb90907136fdcba0d6c348e88ab6a14a5497dffd24e8800ea9f2694bd85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74729811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f0263228dbe7a2edb80d610c8684e20899cdffeaa63a45ff8848da9e1fbef9`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Wed, 27 Jan 2021 22:02:07 GMT
ENV AEROSPIKE_VERSION=5.4.0.3
# Wed, 27 Jan 2021 22:02:07 GMT
ENV AEROSPIKE_SHA256=31468e3c70e0296f59b2f865dbe2f3329885459db069143fc6ee94e265a060bc
# Wed, 27 Jan 2021 22:02:35 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 27 Jan 2021 22:02:35 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 27 Jan 2021 22:02:36 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 27 Jan 2021 22:02:36 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 27 Jan 2021 22:02:36 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 27 Jan 2021 22:02:36 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd01fc5f2a9859e0d480ad109cc6e310c75d49c32e84f5591a743a2db8b528b`  
		Last Modified: Wed, 27 Jan 2021 22:03:34 GMT  
		Size: 52.2 MB (52199148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c99f5234b3ac6376961de35814e002d83b532411f03ca3f60b6691611c9409`  
		Last Modified: Wed, 27 Jan 2021 22:03:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7905191371a96a2fd0264e8fe1f5f683ebaf0e609acfdb6b88bf4eea1cd326`  
		Last Modified: Wed, 27 Jan 2021 22:03:25 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:4e365ec05b08118418d83d7df09baeaea064e1760b37e1abf50e327f1050435c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:ac3c1bb90907136fdcba0d6c348e88ab6a14a5497dffd24e8800ea9f2694bd85
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74729811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f0263228dbe7a2edb80d610c8684e20899cdffeaa63a45ff8848da9e1fbef9`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Wed, 27 Jan 2021 22:02:07 GMT
ENV AEROSPIKE_VERSION=5.4.0.3
# Wed, 27 Jan 2021 22:02:07 GMT
ENV AEROSPIKE_SHA256=31468e3c70e0296f59b2f865dbe2f3329885459db069143fc6ee94e265a060bc
# Wed, 27 Jan 2021 22:02:35 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 27 Jan 2021 22:02:35 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 27 Jan 2021 22:02:36 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 27 Jan 2021 22:02:36 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 27 Jan 2021 22:02:36 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 27 Jan 2021 22:02:36 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd01fc5f2a9859e0d480ad109cc6e310c75d49c32e84f5591a743a2db8b528b`  
		Last Modified: Wed, 27 Jan 2021 22:03:34 GMT  
		Size: 52.2 MB (52199148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c99f5234b3ac6376961de35814e002d83b532411f03ca3f60b6691611c9409`  
		Last Modified: Wed, 27 Jan 2021 22:03:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7905191371a96a2fd0264e8fe1f5f683ebaf0e609acfdb6b88bf4eea1cd326`  
		Last Modified: Wed, 27 Jan 2021 22:03:25 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
