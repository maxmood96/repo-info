<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.26`](#neo4j4426)
-	[`neo4j:4.4.26-community`](#neo4j4426-community)
-	[`neo4j:4.4.26-enterprise`](#neo4j4426-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5.13`](#neo4j513)
-	[`neo4j:5.13-bullseye`](#neo4j513-bullseye)
-	[`neo4j:5.13-community`](#neo4j513-community)
-	[`neo4j:5.13-community-bullseye`](#neo4j513-community-bullseye)
-	[`neo4j:5.13-community-ubi8`](#neo4j513-community-ubi8)
-	[`neo4j:5.13-enterprise`](#neo4j513-enterprise)
-	[`neo4j:5.13-enterprise-bullseye`](#neo4j513-enterprise-bullseye)
-	[`neo4j:5.13-enterprise-ubi8`](#neo4j513-enterprise-ubi8)
-	[`neo4j:5.13-ubi8`](#neo4j513-ubi8)
-	[`neo4j:5.13.0`](#neo4j5130)
-	[`neo4j:5.13.0-bullseye`](#neo4j5130-bullseye)
-	[`neo4j:5.13.0-community`](#neo4j5130-community)
-	[`neo4j:5.13.0-community-bullseye`](#neo4j5130-community-bullseye)
-	[`neo4j:5.13.0-community-ubi8`](#neo4j5130-community-ubi8)
-	[`neo4j:5.13.0-enterprise`](#neo4j5130-enterprise)
-	[`neo4j:5.13.0-enterprise-bullseye`](#neo4j5130-enterprise-bullseye)
-	[`neo4j:5.13.0-enterprise-ubi8`](#neo4j5130-enterprise-ubi8)
-	[`neo4j:5.13.0-ubi8`](#neo4j5130-ubi8)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi8`](#neo4jcommunity-ubi8)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi8`](#neo4jenterprise-ubi8)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi8`](#neo4jubi8)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:ced59c30cdf4421b67c43d5ce746a96c649aaa2db6e5b34b5c12eca9afb906b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:f72f3ce6b7e8d04269830fc3ecb7ee78b9e23c11039ea630b93f7cced0076e9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298601690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98afcb7700029c7db8038a508605c87fff8c28fc601cbb227ba184bbba5b4660`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:45:36 GMT
COPY dir:2526dfaf6aedccef54b8de2f87890e86c6d3fe8431985d8e74dcfc29195b01ed in /opt/java/openjdk 
# Fri, 13 Oct 2023 13:43:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 13:43:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 13:43:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 13:43:10 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 13:43:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 13:43:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 13:43:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 13:43:22 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 13:43:22 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 13:43:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 13:43:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119a53a4a8795e7699b47fa3480b38b8b13e889bb26254f2a28ca9e57185096c`  
		Last Modified: Fri, 13 Oct 2023 13:05:54 GMT  
		Size: 144.8 MB (144826181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b5ff6ee817eac19b8e8c36c8e1c27ccdcdd23ab60e8f23bf4b90e6601561ca`  
		Last Modified: Fri, 13 Oct 2023 13:46:50 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c521b4cd3c137ddfcb1ab1f906429f8aea2bed45d67bdde5296e7a72ee9f01d`  
		Last Modified: Fri, 13 Oct 2023 13:46:51 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa40fb21e239590789c0e6fadcd2548304e2f064f6e5aa3b5c78f9219142f15d`  
		Last Modified: Fri, 13 Oct 2023 13:46:59 GMT  
		Size: 122.3 MB (122344492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5d5ad2dfd45b061f27ea0558a5eb0f4a816c8f86c8da0650f61b0d9a18a42fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293883247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5462747eeb929e9156eb13de1b271f40ef7af6d833e13680e79d25e63385ec6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:26:07 GMT
COPY dir:b4903e9e1c2782550c5bca9cb7b0f840b4fdb810848e07ca44af328ac9dd84f6 in /opt/java/openjdk 
# Fri, 13 Oct 2023 08:26:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 08:26:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 08:26:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 08:26:11 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 08:26:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:26:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:26:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 08:26:22 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 08:26:22 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 08:26:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 08:26:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe38f36b0480d7264c9d22fe6161aee59046ea148d7c5db5adf031ed382ecb6`  
		Last Modified: Fri, 13 Oct 2023 08:29:47 GMT  
		Size: 141.6 MB (141570598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaff1cdcfe3b58763da7f31369ab7c96d454f7b2b2740ce964ddd8ea51b8b24`  
		Last Modified: Fri, 13 Oct 2023 08:29:38 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e31d3044d23f3bb51298d832eb53e2b10beb5951961b79c277d291aea5402`  
		Last Modified: Fri, 13 Oct 2023 08:29:38 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212b787f731cce2ddbd26f5bf8867d522a844473bed7810d4adcaebdb275c235`  
		Last Modified: Fri, 13 Oct 2023 08:29:44 GMT  
		Size: 122.2 MB (122235378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:ced59c30cdf4421b67c43d5ce746a96c649aaa2db6e5b34b5c12eca9afb906b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:f72f3ce6b7e8d04269830fc3ecb7ee78b9e23c11039ea630b93f7cced0076e9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298601690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98afcb7700029c7db8038a508605c87fff8c28fc601cbb227ba184bbba5b4660`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:45:36 GMT
COPY dir:2526dfaf6aedccef54b8de2f87890e86c6d3fe8431985d8e74dcfc29195b01ed in /opt/java/openjdk 
# Fri, 13 Oct 2023 13:43:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 13:43:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 13:43:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 13:43:10 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 13:43:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 13:43:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 13:43:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 13:43:22 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 13:43:22 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 13:43:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 13:43:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119a53a4a8795e7699b47fa3480b38b8b13e889bb26254f2a28ca9e57185096c`  
		Last Modified: Fri, 13 Oct 2023 13:05:54 GMT  
		Size: 144.8 MB (144826181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b5ff6ee817eac19b8e8c36c8e1c27ccdcdd23ab60e8f23bf4b90e6601561ca`  
		Last Modified: Fri, 13 Oct 2023 13:46:50 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c521b4cd3c137ddfcb1ab1f906429f8aea2bed45d67bdde5296e7a72ee9f01d`  
		Last Modified: Fri, 13 Oct 2023 13:46:51 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa40fb21e239590789c0e6fadcd2548304e2f064f6e5aa3b5c78f9219142f15d`  
		Last Modified: Fri, 13 Oct 2023 13:46:59 GMT  
		Size: 122.3 MB (122344492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5d5ad2dfd45b061f27ea0558a5eb0f4a816c8f86c8da0650f61b0d9a18a42fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293883247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5462747eeb929e9156eb13de1b271f40ef7af6d833e13680e79d25e63385ec6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:26:07 GMT
COPY dir:b4903e9e1c2782550c5bca9cb7b0f840b4fdb810848e07ca44af328ac9dd84f6 in /opt/java/openjdk 
# Fri, 13 Oct 2023 08:26:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 08:26:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 08:26:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 08:26:11 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 08:26:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:26:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:26:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 08:26:22 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 08:26:22 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 08:26:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 08:26:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe38f36b0480d7264c9d22fe6161aee59046ea148d7c5db5adf031ed382ecb6`  
		Last Modified: Fri, 13 Oct 2023 08:29:47 GMT  
		Size: 141.6 MB (141570598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaff1cdcfe3b58763da7f31369ab7c96d454f7b2b2740ce964ddd8ea51b8b24`  
		Last Modified: Fri, 13 Oct 2023 08:29:38 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e31d3044d23f3bb51298d832eb53e2b10beb5951961b79c277d291aea5402`  
		Last Modified: Fri, 13 Oct 2023 08:29:38 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212b787f731cce2ddbd26f5bf8867d522a844473bed7810d4adcaebdb275c235`  
		Last Modified: Fri, 13 Oct 2023 08:29:44 GMT  
		Size: 122.2 MB (122235378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:6147e91d4dc90b65253a9f60092b2508fac2cdb61c66c96bae05c80e4ce5551a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:4cc26a2f7847cc0ab279c33f01b6b9bb57b128500cc5eab705b8c0ecefca0848
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.3 MB (405291263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9292a52ecc91db3335d3ddfb8ab02191cc77504bd2c4c81547856250a8831bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:45:36 GMT
COPY dir:2526dfaf6aedccef54b8de2f87890e86c6d3fe8431985d8e74dcfc29195b01ed in /opt/java/openjdk 
# Fri, 13 Oct 2023 13:43:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5059157293dee431cd78ad350b077792a481526b3994f5f043529d7145005914 NEO4J_TARBALL=neo4j-enterprise-4.4.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 13:43:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 13:43:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 13:43:27 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 13:43:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 13:43:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 13:43:42 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 13:43:43 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 13:43:43 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 13:43:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 13:43:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119a53a4a8795e7699b47fa3480b38b8b13e889bb26254f2a28ca9e57185096c`  
		Last Modified: Fri, 13 Oct 2023 13:05:54 GMT  
		Size: 144.8 MB (144826181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879bff131a52e6f6fe041ccae2f6b6363f074de9a8340979c34a183240617919`  
		Last Modified: Fri, 13 Oct 2023 13:47:12 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339562b07247bbeb492052b9877ab8fb52fa5c7a9c94a5c9878a9f1b98b044b1`  
		Last Modified: Fri, 13 Oct 2023 13:47:12 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bb57e5d768f666ca28089c15885ad98ca2754286f9e37814b32bbd735901c0`  
		Last Modified: Fri, 13 Oct 2023 13:47:26 GMT  
		Size: 229.0 MB (229034064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:600df6dbb641c766b4cbf42ce7cdc44b6969ac8b8c297a5fa0a6149c2a1f7df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.6 MB (400575896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16caeec53c3955f09ba7c901709b0ae755e35547ca77bea8072057bcb6542a10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:26:07 GMT
COPY dir:b4903e9e1c2782550c5bca9cb7b0f840b4fdb810848e07ca44af328ac9dd84f6 in /opt/java/openjdk 
# Fri, 13 Oct 2023 08:26:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5059157293dee431cd78ad350b077792a481526b3994f5f043529d7145005914 NEO4J_TARBALL=neo4j-enterprise-4.4.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 08:26:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 08:26:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 08:26:25 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 08:26:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:26:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:26:40 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 08:26:40 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 08:26:40 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 08:26:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 08:26:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe38f36b0480d7264c9d22fe6161aee59046ea148d7c5db5adf031ed382ecb6`  
		Last Modified: Fri, 13 Oct 2023 08:29:47 GMT  
		Size: 141.6 MB (141570598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf60a8179df5b04adb75a47ade0e633be738c0d12a2b4e13a060a99e38fcd06`  
		Last Modified: Fri, 13 Oct 2023 08:30:00 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0b4fc685734505c60b5449d25af64df03810f2a9eead56509d9477f2cfa315`  
		Last Modified: Fri, 13 Oct 2023 08:30:00 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df589bb5fc9125efa3513ee531abe64f013d9d41bf7b95ed9d1c4e2e49948b21`  
		Last Modified: Fri, 13 Oct 2023 08:30:17 GMT  
		Size: 228.9 MB (228928030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.26`

```console
$ docker pull neo4j@sha256:ced59c30cdf4421b67c43d5ce746a96c649aaa2db6e5b34b5c12eca9afb906b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.26` - linux; amd64

```console
$ docker pull neo4j@sha256:f72f3ce6b7e8d04269830fc3ecb7ee78b9e23c11039ea630b93f7cced0076e9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298601690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98afcb7700029c7db8038a508605c87fff8c28fc601cbb227ba184bbba5b4660`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:45:36 GMT
COPY dir:2526dfaf6aedccef54b8de2f87890e86c6d3fe8431985d8e74dcfc29195b01ed in /opt/java/openjdk 
# Fri, 13 Oct 2023 13:43:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 13:43:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 13:43:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 13:43:10 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 13:43:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 13:43:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 13:43:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 13:43:22 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 13:43:22 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 13:43:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 13:43:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119a53a4a8795e7699b47fa3480b38b8b13e889bb26254f2a28ca9e57185096c`  
		Last Modified: Fri, 13 Oct 2023 13:05:54 GMT  
		Size: 144.8 MB (144826181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b5ff6ee817eac19b8e8c36c8e1c27ccdcdd23ab60e8f23bf4b90e6601561ca`  
		Last Modified: Fri, 13 Oct 2023 13:46:50 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c521b4cd3c137ddfcb1ab1f906429f8aea2bed45d67bdde5296e7a72ee9f01d`  
		Last Modified: Fri, 13 Oct 2023 13:46:51 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa40fb21e239590789c0e6fadcd2548304e2f064f6e5aa3b5c78f9219142f15d`  
		Last Modified: Fri, 13 Oct 2023 13:46:59 GMT  
		Size: 122.3 MB (122344492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.26` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5d5ad2dfd45b061f27ea0558a5eb0f4a816c8f86c8da0650f61b0d9a18a42fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293883247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5462747eeb929e9156eb13de1b271f40ef7af6d833e13680e79d25e63385ec6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:26:07 GMT
COPY dir:b4903e9e1c2782550c5bca9cb7b0f840b4fdb810848e07ca44af328ac9dd84f6 in /opt/java/openjdk 
# Fri, 13 Oct 2023 08:26:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 08:26:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 08:26:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 08:26:11 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 08:26:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:26:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:26:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 08:26:22 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 08:26:22 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 08:26:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 08:26:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe38f36b0480d7264c9d22fe6161aee59046ea148d7c5db5adf031ed382ecb6`  
		Last Modified: Fri, 13 Oct 2023 08:29:47 GMT  
		Size: 141.6 MB (141570598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaff1cdcfe3b58763da7f31369ab7c96d454f7b2b2740ce964ddd8ea51b8b24`  
		Last Modified: Fri, 13 Oct 2023 08:29:38 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e31d3044d23f3bb51298d832eb53e2b10beb5951961b79c277d291aea5402`  
		Last Modified: Fri, 13 Oct 2023 08:29:38 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212b787f731cce2ddbd26f5bf8867d522a844473bed7810d4adcaebdb275c235`  
		Last Modified: Fri, 13 Oct 2023 08:29:44 GMT  
		Size: 122.2 MB (122235378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.26-community`

```console
$ docker pull neo4j@sha256:ced59c30cdf4421b67c43d5ce746a96c649aaa2db6e5b34b5c12eca9afb906b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.26-community` - linux; amd64

```console
$ docker pull neo4j@sha256:f72f3ce6b7e8d04269830fc3ecb7ee78b9e23c11039ea630b93f7cced0076e9d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298601690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98afcb7700029c7db8038a508605c87fff8c28fc601cbb227ba184bbba5b4660`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:45:36 GMT
COPY dir:2526dfaf6aedccef54b8de2f87890e86c6d3fe8431985d8e74dcfc29195b01ed in /opt/java/openjdk 
# Fri, 13 Oct 2023 13:43:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 13:43:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 13:43:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 13:43:10 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 13:43:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 13:43:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 13:43:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 13:43:22 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 13:43:22 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 13:43:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 13:43:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119a53a4a8795e7699b47fa3480b38b8b13e889bb26254f2a28ca9e57185096c`  
		Last Modified: Fri, 13 Oct 2023 13:05:54 GMT  
		Size: 144.8 MB (144826181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b5ff6ee817eac19b8e8c36c8e1c27ccdcdd23ab60e8f23bf4b90e6601561ca`  
		Last Modified: Fri, 13 Oct 2023 13:46:50 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c521b4cd3c137ddfcb1ab1f906429f8aea2bed45d67bdde5296e7a72ee9f01d`  
		Last Modified: Fri, 13 Oct 2023 13:46:51 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa40fb21e239590789c0e6fadcd2548304e2f064f6e5aa3b5c78f9219142f15d`  
		Last Modified: Fri, 13 Oct 2023 13:46:59 GMT  
		Size: 122.3 MB (122344492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.26-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5d5ad2dfd45b061f27ea0558a5eb0f4a816c8f86c8da0650f61b0d9a18a42fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293883247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5462747eeb929e9156eb13de1b271f40ef7af6d833e13680e79d25e63385ec6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:26:07 GMT
COPY dir:b4903e9e1c2782550c5bca9cb7b0f840b4fdb810848e07ca44af328ac9dd84f6 in /opt/java/openjdk 
# Fri, 13 Oct 2023 08:26:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8c547187bdd00bdb735d4fcf4036e158b54071499608c1262d3108f5550155f7 NEO4J_TARBALL=neo4j-community-4.4.26-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 08:26:11 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 08:26:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 08:26:11 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 08:26:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:26:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:26:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 08:26:22 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 08:26:22 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 08:26:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 08:26:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe38f36b0480d7264c9d22fe6161aee59046ea148d7c5db5adf031ed382ecb6`  
		Last Modified: Fri, 13 Oct 2023 08:29:47 GMT  
		Size: 141.6 MB (141570598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aaff1cdcfe3b58763da7f31369ab7c96d454f7b2b2740ce964ddd8ea51b8b24`  
		Last Modified: Fri, 13 Oct 2023 08:29:38 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655e31d3044d23f3bb51298d832eb53e2b10beb5951961b79c277d291aea5402`  
		Last Modified: Fri, 13 Oct 2023 08:29:38 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212b787f731cce2ddbd26f5bf8867d522a844473bed7810d4adcaebdb275c235`  
		Last Modified: Fri, 13 Oct 2023 08:29:44 GMT  
		Size: 122.2 MB (122235378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.26-enterprise`

```console
$ docker pull neo4j@sha256:6147e91d4dc90b65253a9f60092b2508fac2cdb61c66c96bae05c80e4ce5551a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.26-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:4cc26a2f7847cc0ab279c33f01b6b9bb57b128500cc5eab705b8c0ecefca0848
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.3 MB (405291263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9292a52ecc91db3335d3ddfb8ab02191cc77504bd2c4c81547856250a8831bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:45:36 GMT
COPY dir:2526dfaf6aedccef54b8de2f87890e86c6d3fe8431985d8e74dcfc29195b01ed in /opt/java/openjdk 
# Fri, 13 Oct 2023 13:43:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5059157293dee431cd78ad350b077792a481526b3994f5f043529d7145005914 NEO4J_TARBALL=neo4j-enterprise-4.4.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 13:43:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 13:43:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 13:43:27 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 13:43:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 13:43:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 13:43:42 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 13:43:43 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 13:43:43 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 13:43:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 13:43:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:119a53a4a8795e7699b47fa3480b38b8b13e889bb26254f2a28ca9e57185096c`  
		Last Modified: Fri, 13 Oct 2023 13:05:54 GMT  
		Size: 144.8 MB (144826181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879bff131a52e6f6fe041ccae2f6b6363f074de9a8340979c34a183240617919`  
		Last Modified: Fri, 13 Oct 2023 13:47:12 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339562b07247bbeb492052b9877ab8fb52fa5c7a9c94a5c9878a9f1b98b044b1`  
		Last Modified: Fri, 13 Oct 2023 13:47:12 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bb57e5d768f666ca28089c15885ad98ca2754286f9e37814b32bbd735901c0`  
		Last Modified: Fri, 13 Oct 2023 13:47:26 GMT  
		Size: 229.0 MB (229034064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.26-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:600df6dbb641c766b4cbf42ce7cdc44b6969ac8b8c297a5fa0a6149c2a1f7df4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.6 MB (400575896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16caeec53c3955f09ba7c901709b0ae755e35547ca77bea8072057bcb6542a10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:26:07 GMT
COPY dir:b4903e9e1c2782550c5bca9cb7b0f840b4fdb810848e07ca44af328ac9dd84f6 in /opt/java/openjdk 
# Fri, 13 Oct 2023 08:26:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5059157293dee431cd78ad350b077792a481526b3994f5f043529d7145005914 NEO4J_TARBALL=neo4j-enterprise-4.4.26-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 08:26:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
# Fri, 13 Oct 2023 08:26:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 08:26:25 GMT
COPY multi:a23c335136a31744c3da3fe5cd721fb899707ce1efde466c13bf9deefb000b04 in /startup/ 
# Fri, 13 Oct 2023 08:26:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.26-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:26:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:26:40 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 08:26:40 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 08:26:40 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 08:26:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 08:26:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe38f36b0480d7264c9d22fe6161aee59046ea148d7c5db5adf031ed382ecb6`  
		Last Modified: Fri, 13 Oct 2023 08:29:47 GMT  
		Size: 141.6 MB (141570598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf60a8179df5b04adb75a47ade0e633be738c0d12a2b4e13a060a99e38fcd06`  
		Last Modified: Fri, 13 Oct 2023 08:30:00 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0b4fc685734505c60b5449d25af64df03810f2a9eead56509d9477f2cfa315`  
		Last Modified: Fri, 13 Oct 2023 08:30:00 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df589bb5fc9125efa3513ee531abe64f013d9d41bf7b95ed9d1c4e2e49948b21`  
		Last Modified: Fri, 13 Oct 2023 08:30:17 GMT  
		Size: 228.9 MB (228928030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:d3fd3a1d732ada9e3f6e5ee90eb60dd9478cc27c2a0584c2bfb0e40c1dfd8358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1f56089ea971bb031f282d02a7f47d00477ad61f63dfe2366168868b8210a7e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303186836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4062ae5b326ca01c8276df7b0514e325adfeb8d4989dfc37240874ed11e5c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:43 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:17:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:17:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:17:47 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:17:47 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:17:47 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:17:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:17:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4875fc5aa36db66fd60ac4c33ee24d7b78781cc7057b39a3c5dd333da45e67`  
		Last Modified: Sat, 28 Oct 2023 00:18:44 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad3aa2bf436a8074e531c63db0335c886a5affdc5442c7eff91b5971b78f899`  
		Last Modified: Sat, 28 Oct 2023 00:18:51 GMT  
		Size: 112.6 MB (112571459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e7b055d5dcdbaa909a7f860df30f24df15a47e57c0af7baebeff32233d40e5f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300330311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88063685d54688ed8fe0aab7d9cf1d6f8857ef8567eca4912929d52760ed6309`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:16 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:20 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:20 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37588613c0a442109a8b5e96b11783494630003e0f2014aefbc5320ee021b4f`  
		Last Modified: Sat, 28 Oct 2023 00:15:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72541dc1b2cb797f225e442a285d2bf567ceb4380b4422945e0b0597f709880`  
		Last Modified: Sat, 28 Oct 2023 00:15:37 GMT  
		Size: 112.6 MB (112571508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:9c29deebf02269b232b604b61f6eec3053eed7e8579de30d6c2a44678438c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b6513dac2f7e41b64028ae956cce6e509c52e517505f5de548f5d5af9d07a6e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563995553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48038f7ec803b404a2a0753ab2582ce40d46013d0bb5545fa0d8c876f259fd0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:23:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:23:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:23:15 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:23:15 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:23:15 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:23:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:23:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a518f4ff3384d7b1f95bec6f8eb7a4dc4f6c85520848e3c38426831ef4d84497`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0cd134c9a52a1b12e63a3bc14b082b077624c7f899c8f0aa73bbc86b7daaf`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27793a1ea7ba2a5df6c01269f10c45fbec89545158296942f53de40a667521f6`  
		Last Modified: Mon, 23 Oct 2023 23:25:21 GMT  
		Size: 387.8 MB (387788702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f1a2c0887c31845afcc20af6f3287b3ae3cc577a547879b7c625bcab0d656f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561301164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13a85349ee14b832ba65e428feb6596712508a6ab24bbdef83af3aa95e32929`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:38 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:56 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:56 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:56 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444acc2d512154a3a12a506b5fff4b5ad22dccd3dbb69d2af0f39740da4f4156`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aad7f31e1121b612569b871348d076aa978053bf06e1399bdf50cad48ef11ac`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b133d9350effbb278967b5da69cdffa0ec5d1211265622859cf55cfa2ce413`  
		Last Modified: Mon, 23 Oct 2023 23:42:56 GMT  
		Size: 387.7 MB (387680242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:9c29deebf02269b232b604b61f6eec3053eed7e8579de30d6c2a44678438c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b6513dac2f7e41b64028ae956cce6e509c52e517505f5de548f5d5af9d07a6e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563995553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48038f7ec803b404a2a0753ab2582ce40d46013d0bb5545fa0d8c876f259fd0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:23:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:23:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:23:15 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:23:15 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:23:15 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:23:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:23:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a518f4ff3384d7b1f95bec6f8eb7a4dc4f6c85520848e3c38426831ef4d84497`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0cd134c9a52a1b12e63a3bc14b082b077624c7f899c8f0aa73bbc86b7daaf`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27793a1ea7ba2a5df6c01269f10c45fbec89545158296942f53de40a667521f6`  
		Last Modified: Mon, 23 Oct 2023 23:25:21 GMT  
		Size: 387.8 MB (387788702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f1a2c0887c31845afcc20af6f3287b3ae3cc577a547879b7c625bcab0d656f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561301164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13a85349ee14b832ba65e428feb6596712508a6ab24bbdef83af3aa95e32929`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:38 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:56 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:56 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:56 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444acc2d512154a3a12a506b5fff4b5ad22dccd3dbb69d2af0f39740da4f4156`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aad7f31e1121b612569b871348d076aa978053bf06e1399bdf50cad48ef11ac`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b133d9350effbb278967b5da69cdffa0ec5d1211265622859cf55cfa2ce413`  
		Last Modified: Mon, 23 Oct 2023 23:42:56 GMT  
		Size: 387.7 MB (387680242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:7d5f7dbdfdb84dd97ae2ad07ff4a0fb97aa4bab41793e571dcb8eb0293dfc91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:d4514bb63647e7f0447be693786c7ab08362c79fb9d87143534a0fbede046255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574593546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de4f639c2925bd781e18ac495901f8c2a0e7966efd4ddb7d6517464cccb6c7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:18:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:18:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:18:03 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:18:03 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:18:03 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:18:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:18:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7244962af5d6c6ed5c0762b6739fbfc3777703b8cb7029137c6f7482ff9aaeca`  
		Last Modified: Sat, 28 Oct 2023 00:19:16 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a5fe57ea88dd7b2fe994a3e2168f48c22edcb7cea6c9f6c9864c9f19439313`  
		Last Modified: Sat, 28 Oct 2023 00:19:38 GMT  
		Size: 384.0 MB (383978174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f3b0d3d8a9e95b302f1355dd82eb59fb543b147edb272b20d77f1e6fd9928fdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.7 MB (571737042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232507afaa7634477d97d7659298f31afcb11d154938ac59b77e7ba096b46181`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:45 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:45 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:45 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8078e596f3c5b454a1bd939257da61addfd31bda31435c63edc74bb4fb8c93`  
		Last Modified: Sat, 28 Oct 2023 00:15:59 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3275542ef69cfa23700723a87f7893123df9f6d8898fdc3d717d865700dd814a`  
		Last Modified: Sat, 28 Oct 2023 00:16:19 GMT  
		Size: 384.0 MB (383978242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:d3fd3a1d732ada9e3f6e5ee90eb60dd9478cc27c2a0584c2bfb0e40c1dfd8358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1f56089ea971bb031f282d02a7f47d00477ad61f63dfe2366168868b8210a7e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303186836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4062ae5b326ca01c8276df7b0514e325adfeb8d4989dfc37240874ed11e5c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:43 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:17:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:17:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:17:47 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:17:47 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:17:47 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:17:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:17:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4875fc5aa36db66fd60ac4c33ee24d7b78781cc7057b39a3c5dd333da45e67`  
		Last Modified: Sat, 28 Oct 2023 00:18:44 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad3aa2bf436a8074e531c63db0335c886a5affdc5442c7eff91b5971b78f899`  
		Last Modified: Sat, 28 Oct 2023 00:18:51 GMT  
		Size: 112.6 MB (112571459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e7b055d5dcdbaa909a7f860df30f24df15a47e57c0af7baebeff32233d40e5f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300330311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88063685d54688ed8fe0aab7d9cf1d6f8857ef8567eca4912929d52760ed6309`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:16 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:20 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:20 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37588613c0a442109a8b5e96b11783494630003e0f2014aefbc5320ee021b4f`  
		Last Modified: Sat, 28 Oct 2023 00:15:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72541dc1b2cb797f225e442a285d2bf567ceb4380b4422945e0b0597f709880`  
		Last Modified: Sat, 28 Oct 2023 00:15:37 GMT  
		Size: 112.6 MB (112571508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-bullseye`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-community`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-community` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-community-bullseye`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-community-ubi8`

```console
$ docker pull neo4j@sha256:d3fd3a1d732ada9e3f6e5ee90eb60dd9478cc27c2a0584c2bfb0e40c1dfd8358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1f56089ea971bb031f282d02a7f47d00477ad61f63dfe2366168868b8210a7e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303186836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4062ae5b326ca01c8276df7b0514e325adfeb8d4989dfc37240874ed11e5c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:43 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:17:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:17:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:17:47 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:17:47 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:17:47 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:17:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:17:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4875fc5aa36db66fd60ac4c33ee24d7b78781cc7057b39a3c5dd333da45e67`  
		Last Modified: Sat, 28 Oct 2023 00:18:44 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad3aa2bf436a8074e531c63db0335c886a5affdc5442c7eff91b5971b78f899`  
		Last Modified: Sat, 28 Oct 2023 00:18:51 GMT  
		Size: 112.6 MB (112571459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e7b055d5dcdbaa909a7f860df30f24df15a47e57c0af7baebeff32233d40e5f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300330311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88063685d54688ed8fe0aab7d9cf1d6f8857ef8567eca4912929d52760ed6309`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:16 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:20 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:20 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37588613c0a442109a8b5e96b11783494630003e0f2014aefbc5320ee021b4f`  
		Last Modified: Sat, 28 Oct 2023 00:15:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72541dc1b2cb797f225e442a285d2bf567ceb4380b4422945e0b0597f709880`  
		Last Modified: Sat, 28 Oct 2023 00:15:37 GMT  
		Size: 112.6 MB (112571508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-enterprise`

```console
$ docker pull neo4j@sha256:9c29deebf02269b232b604b61f6eec3053eed7e8579de30d6c2a44678438c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b6513dac2f7e41b64028ae956cce6e509c52e517505f5de548f5d5af9d07a6e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563995553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48038f7ec803b404a2a0753ab2582ce40d46013d0bb5545fa0d8c876f259fd0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:23:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:23:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:23:15 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:23:15 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:23:15 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:23:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:23:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a518f4ff3384d7b1f95bec6f8eb7a4dc4f6c85520848e3c38426831ef4d84497`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0cd134c9a52a1b12e63a3bc14b082b077624c7f899c8f0aa73bbc86b7daaf`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27793a1ea7ba2a5df6c01269f10c45fbec89545158296942f53de40a667521f6`  
		Last Modified: Mon, 23 Oct 2023 23:25:21 GMT  
		Size: 387.8 MB (387788702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f1a2c0887c31845afcc20af6f3287b3ae3cc577a547879b7c625bcab0d656f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561301164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13a85349ee14b832ba65e428feb6596712508a6ab24bbdef83af3aa95e32929`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:38 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:56 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:56 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:56 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444acc2d512154a3a12a506b5fff4b5ad22dccd3dbb69d2af0f39740da4f4156`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aad7f31e1121b612569b871348d076aa978053bf06e1399bdf50cad48ef11ac`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b133d9350effbb278967b5da69cdffa0ec5d1211265622859cf55cfa2ce413`  
		Last Modified: Mon, 23 Oct 2023 23:42:56 GMT  
		Size: 387.7 MB (387680242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:9c29deebf02269b232b604b61f6eec3053eed7e8579de30d6c2a44678438c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b6513dac2f7e41b64028ae956cce6e509c52e517505f5de548f5d5af9d07a6e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563995553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48038f7ec803b404a2a0753ab2582ce40d46013d0bb5545fa0d8c876f259fd0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:23:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:23:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:23:15 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:23:15 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:23:15 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:23:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:23:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a518f4ff3384d7b1f95bec6f8eb7a4dc4f6c85520848e3c38426831ef4d84497`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0cd134c9a52a1b12e63a3bc14b082b077624c7f899c8f0aa73bbc86b7daaf`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27793a1ea7ba2a5df6c01269f10c45fbec89545158296942f53de40a667521f6`  
		Last Modified: Mon, 23 Oct 2023 23:25:21 GMT  
		Size: 387.8 MB (387788702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f1a2c0887c31845afcc20af6f3287b3ae3cc577a547879b7c625bcab0d656f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561301164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13a85349ee14b832ba65e428feb6596712508a6ab24bbdef83af3aa95e32929`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:38 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:56 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:56 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:56 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444acc2d512154a3a12a506b5fff4b5ad22dccd3dbb69d2af0f39740da4f4156`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aad7f31e1121b612569b871348d076aa978053bf06e1399bdf50cad48ef11ac`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b133d9350effbb278967b5da69cdffa0ec5d1211265622859cf55cfa2ce413`  
		Last Modified: Mon, 23 Oct 2023 23:42:56 GMT  
		Size: 387.7 MB (387680242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:7d5f7dbdfdb84dd97ae2ad07ff4a0fb97aa4bab41793e571dcb8eb0293dfc91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:d4514bb63647e7f0447be693786c7ab08362c79fb9d87143534a0fbede046255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574593546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de4f639c2925bd781e18ac495901f8c2a0e7966efd4ddb7d6517464cccb6c7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:18:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:18:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:18:03 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:18:03 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:18:03 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:18:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:18:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7244962af5d6c6ed5c0762b6739fbfc3777703b8cb7029137c6f7482ff9aaeca`  
		Last Modified: Sat, 28 Oct 2023 00:19:16 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a5fe57ea88dd7b2fe994a3e2168f48c22edcb7cea6c9f6c9864c9f19439313`  
		Last Modified: Sat, 28 Oct 2023 00:19:38 GMT  
		Size: 384.0 MB (383978174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f3b0d3d8a9e95b302f1355dd82eb59fb543b147edb272b20d77f1e6fd9928fdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.7 MB (571737042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232507afaa7634477d97d7659298f31afcb11d154938ac59b77e7ba096b46181`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:45 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:45 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:45 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8078e596f3c5b454a1bd939257da61addfd31bda31435c63edc74bb4fb8c93`  
		Last Modified: Sat, 28 Oct 2023 00:15:59 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3275542ef69cfa23700723a87f7893123df9f6d8898fdc3d717d865700dd814a`  
		Last Modified: Sat, 28 Oct 2023 00:16:19 GMT  
		Size: 384.0 MB (383978242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13-ubi8`

```console
$ docker pull neo4j@sha256:d3fd3a1d732ada9e3f6e5ee90eb60dd9478cc27c2a0584c2bfb0e40c1dfd8358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1f56089ea971bb031f282d02a7f47d00477ad61f63dfe2366168868b8210a7e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303186836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4062ae5b326ca01c8276df7b0514e325adfeb8d4989dfc37240874ed11e5c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:43 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:17:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:17:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:17:47 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:17:47 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:17:47 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:17:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:17:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4875fc5aa36db66fd60ac4c33ee24d7b78781cc7057b39a3c5dd333da45e67`  
		Last Modified: Sat, 28 Oct 2023 00:18:44 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad3aa2bf436a8074e531c63db0335c886a5affdc5442c7eff91b5971b78f899`  
		Last Modified: Sat, 28 Oct 2023 00:18:51 GMT  
		Size: 112.6 MB (112571459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e7b055d5dcdbaa909a7f860df30f24df15a47e57c0af7baebeff32233d40e5f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300330311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88063685d54688ed8fe0aab7d9cf1d6f8857ef8567eca4912929d52760ed6309`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:16 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:20 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:20 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37588613c0a442109a8b5e96b11783494630003e0f2014aefbc5320ee021b4f`  
		Last Modified: Sat, 28 Oct 2023 00:15:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72541dc1b2cb797f225e442a285d2bf567ceb4380b4422945e0b0597f709880`  
		Last Modified: Sat, 28 Oct 2023 00:15:37 GMT  
		Size: 112.6 MB (112571508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-bullseye`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-community`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-community-bullseye`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-community-ubi8`

```console
$ docker pull neo4j@sha256:d3fd3a1d732ada9e3f6e5ee90eb60dd9478cc27c2a0584c2bfb0e40c1dfd8358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1f56089ea971bb031f282d02a7f47d00477ad61f63dfe2366168868b8210a7e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303186836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4062ae5b326ca01c8276df7b0514e325adfeb8d4989dfc37240874ed11e5c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:43 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:17:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:17:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:17:47 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:17:47 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:17:47 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:17:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:17:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4875fc5aa36db66fd60ac4c33ee24d7b78781cc7057b39a3c5dd333da45e67`  
		Last Modified: Sat, 28 Oct 2023 00:18:44 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad3aa2bf436a8074e531c63db0335c886a5affdc5442c7eff91b5971b78f899`  
		Last Modified: Sat, 28 Oct 2023 00:18:51 GMT  
		Size: 112.6 MB (112571459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e7b055d5dcdbaa909a7f860df30f24df15a47e57c0af7baebeff32233d40e5f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300330311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88063685d54688ed8fe0aab7d9cf1d6f8857ef8567eca4912929d52760ed6309`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:16 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:20 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:20 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37588613c0a442109a8b5e96b11783494630003e0f2014aefbc5320ee021b4f`  
		Last Modified: Sat, 28 Oct 2023 00:15:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72541dc1b2cb797f225e442a285d2bf567ceb4380b4422945e0b0597f709880`  
		Last Modified: Sat, 28 Oct 2023 00:15:37 GMT  
		Size: 112.6 MB (112571508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-enterprise`

```console
$ docker pull neo4j@sha256:9c29deebf02269b232b604b61f6eec3053eed7e8579de30d6c2a44678438c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b6513dac2f7e41b64028ae956cce6e509c52e517505f5de548f5d5af9d07a6e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563995553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48038f7ec803b404a2a0753ab2582ce40d46013d0bb5545fa0d8c876f259fd0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:23:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:23:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:23:15 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:23:15 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:23:15 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:23:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:23:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a518f4ff3384d7b1f95bec6f8eb7a4dc4f6c85520848e3c38426831ef4d84497`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0cd134c9a52a1b12e63a3bc14b082b077624c7f899c8f0aa73bbc86b7daaf`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27793a1ea7ba2a5df6c01269f10c45fbec89545158296942f53de40a667521f6`  
		Last Modified: Mon, 23 Oct 2023 23:25:21 GMT  
		Size: 387.8 MB (387788702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f1a2c0887c31845afcc20af6f3287b3ae3cc577a547879b7c625bcab0d656f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561301164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13a85349ee14b832ba65e428feb6596712508a6ab24bbdef83af3aa95e32929`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:38 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:56 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:56 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:56 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444acc2d512154a3a12a506b5fff4b5ad22dccd3dbb69d2af0f39740da4f4156`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aad7f31e1121b612569b871348d076aa978053bf06e1399bdf50cad48ef11ac`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b133d9350effbb278967b5da69cdffa0ec5d1211265622859cf55cfa2ce413`  
		Last Modified: Mon, 23 Oct 2023 23:42:56 GMT  
		Size: 387.7 MB (387680242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:9c29deebf02269b232b604b61f6eec3053eed7e8579de30d6c2a44678438c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b6513dac2f7e41b64028ae956cce6e509c52e517505f5de548f5d5af9d07a6e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563995553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48038f7ec803b404a2a0753ab2582ce40d46013d0bb5545fa0d8c876f259fd0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:23:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:23:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:23:15 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:23:15 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:23:15 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:23:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:23:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a518f4ff3384d7b1f95bec6f8eb7a4dc4f6c85520848e3c38426831ef4d84497`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0cd134c9a52a1b12e63a3bc14b082b077624c7f899c8f0aa73bbc86b7daaf`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27793a1ea7ba2a5df6c01269f10c45fbec89545158296942f53de40a667521f6`  
		Last Modified: Mon, 23 Oct 2023 23:25:21 GMT  
		Size: 387.8 MB (387788702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f1a2c0887c31845afcc20af6f3287b3ae3cc577a547879b7c625bcab0d656f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561301164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13a85349ee14b832ba65e428feb6596712508a6ab24bbdef83af3aa95e32929`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:38 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:56 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:56 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:56 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444acc2d512154a3a12a506b5fff4b5ad22dccd3dbb69d2af0f39740da4f4156`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aad7f31e1121b612569b871348d076aa978053bf06e1399bdf50cad48ef11ac`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b133d9350effbb278967b5da69cdffa0ec5d1211265622859cf55cfa2ce413`  
		Last Modified: Mon, 23 Oct 2023 23:42:56 GMT  
		Size: 387.7 MB (387680242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:7d5f7dbdfdb84dd97ae2ad07ff4a0fb97aa4bab41793e571dcb8eb0293dfc91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:d4514bb63647e7f0447be693786c7ab08362c79fb9d87143534a0fbede046255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574593546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de4f639c2925bd781e18ac495901f8c2a0e7966efd4ddb7d6517464cccb6c7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:18:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:18:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:18:03 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:18:03 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:18:03 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:18:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:18:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7244962af5d6c6ed5c0762b6739fbfc3777703b8cb7029137c6f7482ff9aaeca`  
		Last Modified: Sat, 28 Oct 2023 00:19:16 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a5fe57ea88dd7b2fe994a3e2168f48c22edcb7cea6c9f6c9864c9f19439313`  
		Last Modified: Sat, 28 Oct 2023 00:19:38 GMT  
		Size: 384.0 MB (383978174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f3b0d3d8a9e95b302f1355dd82eb59fb543b147edb272b20d77f1e6fd9928fdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.7 MB (571737042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232507afaa7634477d97d7659298f31afcb11d154938ac59b77e7ba096b46181`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:45 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:45 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:45 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8078e596f3c5b454a1bd939257da61addfd31bda31435c63edc74bb4fb8c93`  
		Last Modified: Sat, 28 Oct 2023 00:15:59 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3275542ef69cfa23700723a87f7893123df9f6d8898fdc3d717d865700dd814a`  
		Last Modified: Sat, 28 Oct 2023 00:16:19 GMT  
		Size: 384.0 MB (383978242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.13.0-ubi8`

```console
$ docker pull neo4j@sha256:d3fd3a1d732ada9e3f6e5ee90eb60dd9478cc27c2a0584c2bfb0e40c1dfd8358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.13.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1f56089ea971bb031f282d02a7f47d00477ad61f63dfe2366168868b8210a7e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303186836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4062ae5b326ca01c8276df7b0514e325adfeb8d4989dfc37240874ed11e5c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:43 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:17:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:17:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:17:47 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:17:47 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:17:47 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:17:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:17:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4875fc5aa36db66fd60ac4c33ee24d7b78781cc7057b39a3c5dd333da45e67`  
		Last Modified: Sat, 28 Oct 2023 00:18:44 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad3aa2bf436a8074e531c63db0335c886a5affdc5442c7eff91b5971b78f899`  
		Last Modified: Sat, 28 Oct 2023 00:18:51 GMT  
		Size: 112.6 MB (112571459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.13.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e7b055d5dcdbaa909a7f860df30f24df15a47e57c0af7baebeff32233d40e5f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300330311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88063685d54688ed8fe0aab7d9cf1d6f8857ef8567eca4912929d52760ed6309`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:16 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:20 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:20 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37588613c0a442109a8b5e96b11783494630003e0f2014aefbc5320ee021b4f`  
		Last Modified: Sat, 28 Oct 2023 00:15:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72541dc1b2cb797f225e442a285d2bf567ceb4380b4422945e0b0597f709880`  
		Last Modified: Sat, 28 Oct 2023 00:15:37 GMT  
		Size: 112.6 MB (112571508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:d3fd3a1d732ada9e3f6e5ee90eb60dd9478cc27c2a0584c2bfb0e40c1dfd8358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1f56089ea971bb031f282d02a7f47d00477ad61f63dfe2366168868b8210a7e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303186836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4062ae5b326ca01c8276df7b0514e325adfeb8d4989dfc37240874ed11e5c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:43 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:17:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:17:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:17:47 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:17:47 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:17:47 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:17:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:17:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4875fc5aa36db66fd60ac4c33ee24d7b78781cc7057b39a3c5dd333da45e67`  
		Last Modified: Sat, 28 Oct 2023 00:18:44 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad3aa2bf436a8074e531c63db0335c886a5affdc5442c7eff91b5971b78f899`  
		Last Modified: Sat, 28 Oct 2023 00:18:51 GMT  
		Size: 112.6 MB (112571459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e7b055d5dcdbaa909a7f860df30f24df15a47e57c0af7baebeff32233d40e5f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300330311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88063685d54688ed8fe0aab7d9cf1d6f8857ef8567eca4912929d52760ed6309`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:16 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:20 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:20 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37588613c0a442109a8b5e96b11783494630003e0f2014aefbc5320ee021b4f`  
		Last Modified: Sat, 28 Oct 2023 00:15:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72541dc1b2cb797f225e442a285d2bf567ceb4380b4422945e0b0597f709880`  
		Last Modified: Sat, 28 Oct 2023 00:15:37 GMT  
		Size: 112.6 MB (112571508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:9c29deebf02269b232b604b61f6eec3053eed7e8579de30d6c2a44678438c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b6513dac2f7e41b64028ae956cce6e509c52e517505f5de548f5d5af9d07a6e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563995553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48038f7ec803b404a2a0753ab2582ce40d46013d0bb5545fa0d8c876f259fd0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:23:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:23:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:23:15 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:23:15 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:23:15 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:23:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:23:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a518f4ff3384d7b1f95bec6f8eb7a4dc4f6c85520848e3c38426831ef4d84497`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0cd134c9a52a1b12e63a3bc14b082b077624c7f899c8f0aa73bbc86b7daaf`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27793a1ea7ba2a5df6c01269f10c45fbec89545158296942f53de40a667521f6`  
		Last Modified: Mon, 23 Oct 2023 23:25:21 GMT  
		Size: 387.8 MB (387788702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f1a2c0887c31845afcc20af6f3287b3ae3cc577a547879b7c625bcab0d656f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561301164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13a85349ee14b832ba65e428feb6596712508a6ab24bbdef83af3aa95e32929`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:38 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:56 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:56 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:56 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444acc2d512154a3a12a506b5fff4b5ad22dccd3dbb69d2af0f39740da4f4156`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aad7f31e1121b612569b871348d076aa978053bf06e1399bdf50cad48ef11ac`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b133d9350effbb278967b5da69cdffa0ec5d1211265622859cf55cfa2ce413`  
		Last Modified: Mon, 23 Oct 2023 23:42:56 GMT  
		Size: 387.7 MB (387680242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:9c29deebf02269b232b604b61f6eec3053eed7e8579de30d6c2a44678438c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b6513dac2f7e41b64028ae956cce6e509c52e517505f5de548f5d5af9d07a6e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.0 MB (563995553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48038f7ec803b404a2a0753ab2582ce40d46013d0bb5545fa0d8c876f259fd0d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:45 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:23:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:23:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:23:15 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:23:15 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:23:15 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:23:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:23:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a518f4ff3384d7b1f95bec6f8eb7a4dc4f6c85520848e3c38426831ef4d84497`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe0cd134c9a52a1b12e63a3bc14b082b077624c7f899c8f0aa73bbc86b7daaf`  
		Last Modified: Mon, 23 Oct 2023 23:25:04 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27793a1ea7ba2a5df6c01269f10c45fbec89545158296942f53de40a667521f6`  
		Last Modified: Mon, 23 Oct 2023 23:25:21 GMT  
		Size: 387.8 MB (387788702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f1a2c0887c31845afcc20af6f3287b3ae3cc577a547879b7c625bcab0d656f7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.3 MB (561301164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13a85349ee14b832ba65e428feb6596712508a6ab24bbdef83af3aa95e32929`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:38 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:38 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:56 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:56 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:56 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444acc2d512154a3a12a506b5fff4b5ad22dccd3dbb69d2af0f39740da4f4156`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 3.9 KB (3892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aad7f31e1121b612569b871348d076aa978053bf06e1399bdf50cad48ef11ac`  
		Last Modified: Mon, 23 Oct 2023 23:42:36 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b133d9350effbb278967b5da69cdffa0ec5d1211265622859cf55cfa2ce413`  
		Last Modified: Mon, 23 Oct 2023 23:42:56 GMT  
		Size: 387.7 MB (387680242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:7d5f7dbdfdb84dd97ae2ad07ff4a0fb97aa4bab41793e571dcb8eb0293dfc91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:d4514bb63647e7f0447be693786c7ab08362c79fb9d87143534a0fbede046255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.6 MB (574593546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34de4f639c2925bd781e18ac495901f8c2a0e7966efd4ddb7d6517464cccb6c7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:52 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:18:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:18:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:18:03 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:18:03 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:18:03 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:18:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:18:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7244962af5d6c6ed5c0762b6739fbfc3777703b8cb7029137c6f7482ff9aaeca`  
		Last Modified: Sat, 28 Oct 2023 00:19:16 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a5fe57ea88dd7b2fe994a3e2168f48c22edcb7cea6c9f6c9864c9f19439313`  
		Last Modified: Sat, 28 Oct 2023 00:19:38 GMT  
		Size: 384.0 MB (383978174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f3b0d3d8a9e95b302f1355dd82eb59fb543b147edb272b20d77f1e6fd9928fdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **571.7 MB (571737042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232507afaa7634477d97d7659298f31afcb11d154938ac59b77e7ba096b46181`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ddb9a8a703e097fe7cb4bb1f13787d38488f61f417397781b020bee71160fb6b NEO4J_TARBALL=neo4j-enterprise-5.13.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:22 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:45 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:45 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:45 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:45 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:45 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8078e596f3c5b454a1bd939257da61addfd31bda31435c63edc74bb4fb8c93`  
		Last Modified: Sat, 28 Oct 2023 00:15:59 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3275542ef69cfa23700723a87f7893123df9f6d8898fdc3d717d865700dd814a`  
		Last Modified: Sat, 28 Oct 2023 00:16:19 GMT  
		Size: 384.0 MB (383978242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:5ba8a00a38444cc07623f3de1dd72d0f8cc3dcd64a198c8d87af5a64f65c8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:300897737da9ffb89cc972aa188285ab6221a31bca36e1af80a0a123cabee7cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292588697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab5625f5cf9cf484d658644348e2e4a35b3bb37ce7c3e9b63a502b4bd8f8c3a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 12:53:47 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:22:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:22:28 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:22:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:22:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:22:40 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:22:40 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:22:40 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:22:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b1c1358482f5ddb86ae83588f9a6573202aa945dfa8279bd498c975380cddc`  
		Last Modified: Fri, 13 Oct 2023 13:11:05 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b6b211c73ba8343e784f253b1688bae2e882d0bb5cc09f169066188083947f`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e2689a8ef1630bf5443133f04596b90090666d82da8cd90c8ca544328fcb0e`  
		Last Modified: Mon, 23 Oct 2023 23:24:19 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4d0c91596c6ef00df61214be5007e36469791ec1c2be5997e0080c6be4eccc`  
		Last Modified: Mon, 23 Oct 2023 23:24:25 GMT  
		Size: 116.4 MB (116381843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3e9e732c52b07396516a3d143faab7f44740541d7f5f7afdd8be2560fefe4b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b37b9396d95c28b5f3190b1d816e80c05eb3bb9a68a844a4de00cda63dcdd12`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:24:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Mon, 23 Oct 2023 23:40:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 23 Oct 2023 23:40:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Mon, 23 Oct 2023 23:40:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 23 Oct 2023 23:40:22 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Mon, 23 Oct 2023 23:40:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 Oct 2023 23:40:33 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Oct 2023 23:40:33 GMT
WORKDIR /var/lib/neo4j
# Mon, 23 Oct 2023 23:40:33 GMT
VOLUME [/data /logs]
# Mon, 23 Oct 2023 23:40:33 GMT
EXPOSE 7473 7474 7687
# Mon, 23 Oct 2023 23:40:33 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 23 Oct 2023 23:40:33 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50995bd10c2e2c63e742f532bc7575787ab439e67f61962f5966d8d4cca120`  
		Last Modified: Fri, 13 Oct 2023 08:27:21 GMT  
		Size: 143.5 MB (143543521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bd04e2b624696c16df47eda6289a4b7e3a09107e83b5f6edf3320af7b69538`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a573f2fef6c500ffb7e4c61de932a5e41eacc3f623c54c8d9a3cf63501a317a`  
		Last Modified: Mon, 23 Oct 2023 23:41:54 GMT  
		Size: 9.4 KB (9423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf2a385e8d6e766e3b79ef49f1ca35f11c654171c55701424c062d55b4a7269`  
		Last Modified: Mon, 23 Oct 2023 23:42:01 GMT  
		Size: 116.3 MB (116275151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:d3fd3a1d732ada9e3f6e5ee90eb60dd9478cc27c2a0584c2bfb0e40c1dfd8358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:1f56089ea971bb031f282d02a7f47d00477ad61f63dfe2366168868b8210a7e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303186836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4062ae5b326ca01c8276df7b0514e325adfeb8d4989dfc37240874ed11e5c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:5c3db83b000dbd7f5ac652deca0885f748fc3927831292ee77f730ba2f248f5c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:5e368d6e32137dc736d21dd012bd92b380bff4b32507604f02cc3380ed1f27fc in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:9fbad41b814186dd0da1dae5e6ea38418efba78dbf999da629bbf906da226243 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:55 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:57 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:17:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:17:34 GMT
COPY dir:8fa632b88aeba77c454a49e03e46f325d18f1d0b88154566aabd27ca9aa05ac5 in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:17:43 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:17:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:17:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:17:43 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:17:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:17:47 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:17:47 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:17:47 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:17:47 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:17:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:17:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dc35b837139a95d1b9f7f7b0435a024a74ab972416bdc248f3f608c9f917a753`  
		Last Modified: Wed, 18 Oct 2023 21:53:00 GMT  
		Size: 39.3 MB (39307955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265c4c087c2b3171751cf0c87ab6ca1b345d3abeea69f0e27c59cf455f674cb8`  
		Last Modified: Sat, 28 Oct 2023 00:18:56 GMT  
		Size: 144.8 MB (144775710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066a38b4c409c71d08ac1083faaf19d192d8b848a48b4196e5aaa63132052005`  
		Last Modified: Sat, 28 Oct 2023 00:18:46 GMT  
		Size: 6.5 MB (6522288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4875fc5aa36db66fd60ac4c33ee24d7b78781cc7057b39a3c5dd333da45e67`  
		Last Modified: Sat, 28 Oct 2023 00:18:44 GMT  
		Size: 9.4 KB (9424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad3aa2bf436a8074e531c63db0335c886a5affdc5442c7eff91b5971b78f899`  
		Last Modified: Sat, 28 Oct 2023 00:18:51 GMT  
		Size: 112.6 MB (112571459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e7b055d5dcdbaa909a7f860df30f24df15a47e57c0af7baebeff32233d40e5f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300330311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88063685d54688ed8fe0aab7d9cf1d6f8857ef8567eca4912929d52760ed6309`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 18 Oct 2023 12:49:52 GMT
ADD file:bb957a9ad1c49f868a6ddca1fc0d1a6d046a4ac78579016c86513ae2697c800c in / 
# Wed, 18 Oct 2023 12:49:53 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 18 Oct 2023 12:49:53 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 18 Oct 2023 12:49:53 GMT
ADD multi:02c4aafe003795d7be1bd5a3b6d53d7e91c3b729faa5c8f64c2cc816e6915a18 in /etc/yum.repos.d/ 
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.8"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.expose-services=""
# Wed, 18 Oct 2023 12:49:53 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 18 Oct 2023 12:49:53 GMT
ENV container oci
# Wed, 18 Oct 2023 12:49:53 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Oct 2023 12:49:53 GMT
CMD ["/bin/bash"]
# Wed, 18 Oct 2023 12:49:54 GMT
RUN rm -rf /var/log/*
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:c3a7e153dd0c17454a58c2ee7b0344bb6c541bad125e5fd6aafe5502594445c7 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.8-1072.1697626218.json 
# Wed, 18 Oct 2023 12:49:54 GMT
ADD file:09b2a520966e606ac4a7e397becf400ecaebbb4f919dc1153b799e5c5e11e832 in /root/buildinfo/Dockerfile-ubi8-minimal-8.8-1072.1697626218 
# Wed, 18 Oct 2023 12:49:54 GMT
LABEL "release"="1072.1697626218" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2023-10-18T11:46:11" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dee8029ddcc7ecbfbebb0905d2b15e134338616c" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.8-1072.1697626218"
# Wed, 18 Oct 2023 12:49:56 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2460229-2a53b.repo' '/etc/yum.repos.d/gitweb-f6bee.repo'
# Wed, 18 Oct 2023 12:49:57 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 18 Oct 2023 12:49:59 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Sat, 28 Oct 2023 00:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 28 Oct 2023 00:14:05 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Sat, 28 Oct 2023 00:14:15 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-amd64";             gosusha="3a4e1fc7430f9e7dd7b0cbbe0bfde26bf4a250702e84cf48a1eb2b631c64cf13";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             gosuurl="https://github.com/tianon/gosu/releases/download/1.16/gosu-arm64";             gosusha="23fa49907d5246d2e257de3bf883f57fba47fe1f559f7e732ff16c0f23d2b6a6";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y         findutils         gzip         hostname         jq         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     wget -q ${gosuurl} -O /usr/sbin/gosu;     wget -q  ${gosuurl}.asc -O gosu.asc;     echo "${gosusha}" /usr/sbin/gosu | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     chmod a+x /usr/sbin/gosu;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     gpg --batch --verify gosu.asc /usr/sbin/gosu;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc gosu.asc;     microdnf clean all
# Sat, 28 Oct 2023 00:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c5b1834ae4493af9c623c7d4d68783de1f87d73adea34cd973d9daa3c2ea056c NEO4J_TARBALL=neo4j-community-5.13.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 28 Oct 2023 00:14:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
# Sat, 28 Oct 2023 00:14:16 GMT
COPY multi:b19c74ad2a70cdf4417b1421915c955c79ff7fa1bdf35404eadb22915ea27a8b in /startup/ 
# Sat, 28 Oct 2023 00:14:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.13.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report
# Sat, 28 Oct 2023 00:14:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Oct 2023 00:14:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 28 Oct 2023 00:14:20 GMT
VOLUME [/data /logs]
# Sat, 28 Oct 2023 00:14:20 GMT
EXPOSE 7473 7474 7687
# Sat, 28 Oct 2023 00:14:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 28 Oct 2023 00:14:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4da493486a8e6bed896d94989fd40199cacab25cef2022dc5b72dc9b0be61387`  
		Last Modified: Thu, 19 Oct 2023 07:47:22 GMT  
		Size: 37.7 MB (37689299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145173f563b0089369efa95145ccfd70eece7d62e67374f9488cd12f8b57242d`  
		Last Modified: Sat, 28 Oct 2023 00:15:39 GMT  
		Size: 143.5 MB (143543463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feac9315f3684eb77d25f2d04892858824fd00d93d22e11caf55a9b8ba9cd72a`  
		Last Modified: Sat, 28 Oct 2023 00:15:31 GMT  
		Size: 6.5 MB (6516624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37588613c0a442109a8b5e96b11783494630003e0f2014aefbc5320ee021b4f`  
		Last Modified: Sat, 28 Oct 2023 00:15:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72541dc1b2cb797f225e442a285d2bf567ceb4380b4422945e0b0597f709880`  
		Last Modified: Sat, 28 Oct 2023 00:15:37 GMT  
		Size: 112.6 MB (112571508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
