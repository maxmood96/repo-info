<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.3`](#neo4j43)
-	[`neo4j:4.3-community`](#neo4j43-community)
-	[`neo4j:4.3-enterprise`](#neo4j43-enterprise)
-	[`neo4j:4.3.22`](#neo4j4322)
-	[`neo4j:4.3.22-community`](#neo4j4322-community)
-	[`neo4j:4.3.22-enterprise`](#neo4j4322-enterprise)
-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.15`](#neo4j4415)
-	[`neo4j:4.4.15-community`](#neo4j4415-community)
-	[`neo4j:4.4.15-enterprise`](#neo4j4415-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.2`](#neo4j52)
-	[`neo4j:5.2-enterprise`](#neo4j52-enterprise)
-	[`neo4j:5.2.0`](#neo4j520)
-	[`neo4j:5.2.0-community`](#neo4j520-community)
-	[`neo4j:5.2.0-enterprise`](#neo4j520-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.3`

```console
$ docker pull neo4j@sha256:c2189ceea793016f43cd3b4f1a18c4b07894c2645cccb617afd4cdedb6e82571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3` - linux; amd64

```console
$ docker pull neo4j@sha256:babb5075999a705f0b221e015dedf8c178417bd275b779b9f5c8ffb188d5ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360414193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c5f30d79f1125ff8690fc32b85424dfdef0b0a44afcdf2bfada05d83ade807`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb4f97266d8057fbf15012235106a7241c66cc27475187eb6a6d3cdc9298e534 NEO4J_TARBALL=neo4j-community-4.3.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
# Fri, 25 Nov 2022 21:28:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:56 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 25 Nov 2022 21:29:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:29:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:29:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:29:12 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:29:13 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:29:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:29:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d71a3fe1def6b75de7f7ff1130ea7e74c95a2dfd24e595cef6717257cdbc74`  
		Last Modified: Fri, 25 Nov 2022 21:30:43 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5722c2c1f68c2b937dc4d40aec3002a78b8d9e98b2db9cd48845c066948bb465`  
		Last Modified: Fri, 25 Nov 2022 21:30:43 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129c8e4a104aa54f7b2e162de66b907339b4f814dcd75cbdac5b9865bc70cfb9`  
		Last Modified: Fri, 25 Nov 2022 21:30:50 GMT  
		Size: 130.5 MB (130534265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-community`

```console
$ docker pull neo4j@sha256:c2189ceea793016f43cd3b4f1a18c4b07894c2645cccb617afd4cdedb6e82571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-community` - linux; amd64

```console
$ docker pull neo4j@sha256:babb5075999a705f0b221e015dedf8c178417bd275b779b9f5c8ffb188d5ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360414193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c5f30d79f1125ff8690fc32b85424dfdef0b0a44afcdf2bfada05d83ade807`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb4f97266d8057fbf15012235106a7241c66cc27475187eb6a6d3cdc9298e534 NEO4J_TARBALL=neo4j-community-4.3.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
# Fri, 25 Nov 2022 21:28:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:56 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 25 Nov 2022 21:29:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:29:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:29:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:29:12 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:29:13 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:29:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:29:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d71a3fe1def6b75de7f7ff1130ea7e74c95a2dfd24e595cef6717257cdbc74`  
		Last Modified: Fri, 25 Nov 2022 21:30:43 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5722c2c1f68c2b937dc4d40aec3002a78b8d9e98b2db9cd48845c066948bb465`  
		Last Modified: Fri, 25 Nov 2022 21:30:43 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129c8e4a104aa54f7b2e162de66b907339b4f814dcd75cbdac5b9865bc70cfb9`  
		Last Modified: Fri, 25 Nov 2022 21:30:50 GMT  
		Size: 130.5 MB (130534265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-enterprise`

```console
$ docker pull neo4j@sha256:5fe83ab550348243b26a485e186215623286434e9e14bff17fe241255a481ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:051098e3c43d4793a06ed129022ff04b29dce7b8f27c8108755e76e4e5231f83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 MB (390917072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc03bf7c50b1f701639be4050df90adbaa1c788ee008bad49c83e05576c26af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:29:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=eac8dab9669ad128ae65fabfac982087eaebb6b3bc011e688d33eb379ed92629 NEO4J_TARBALL=neo4j-enterprise-4.3.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:29:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
# Fri, 25 Nov 2022 21:29:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:29:17 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 25 Nov 2022 21:29:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:29:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:29:35 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:29:35 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:29:35 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:29:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:29:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950cb0c40c990ed0bc5702893f640fe0946d52fcb92c4360967910171beb5e`  
		Last Modified: Fri, 25 Nov 2022 21:31:02 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cfe0b7f886b6d1ce69e8b10819158b2e3a94de64215aebcc33499e69b016e4`  
		Last Modified: Fri, 25 Nov 2022 21:31:02 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b536c03580c1c21dcc7cd1ea82d6fb4f8830c7767742afb06fedf147ce4f2c5`  
		Last Modified: Fri, 25 Nov 2022 21:31:10 GMT  
		Size: 161.0 MB (161037149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.22`

```console
$ docker pull neo4j@sha256:c2189ceea793016f43cd3b4f1a18c4b07894c2645cccb617afd4cdedb6e82571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.22` - linux; amd64

```console
$ docker pull neo4j@sha256:babb5075999a705f0b221e015dedf8c178417bd275b779b9f5c8ffb188d5ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360414193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c5f30d79f1125ff8690fc32b85424dfdef0b0a44afcdf2bfada05d83ade807`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb4f97266d8057fbf15012235106a7241c66cc27475187eb6a6d3cdc9298e534 NEO4J_TARBALL=neo4j-community-4.3.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
# Fri, 25 Nov 2022 21:28:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:56 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 25 Nov 2022 21:29:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:29:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:29:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:29:12 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:29:13 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:29:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:29:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d71a3fe1def6b75de7f7ff1130ea7e74c95a2dfd24e595cef6717257cdbc74`  
		Last Modified: Fri, 25 Nov 2022 21:30:43 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5722c2c1f68c2b937dc4d40aec3002a78b8d9e98b2db9cd48845c066948bb465`  
		Last Modified: Fri, 25 Nov 2022 21:30:43 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129c8e4a104aa54f7b2e162de66b907339b4f814dcd75cbdac5b9865bc70cfb9`  
		Last Modified: Fri, 25 Nov 2022 21:30:50 GMT  
		Size: 130.5 MB (130534265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.22-community`

```console
$ docker pull neo4j@sha256:c2189ceea793016f43cd3b4f1a18c4b07894c2645cccb617afd4cdedb6e82571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.22-community` - linux; amd64

```console
$ docker pull neo4j@sha256:babb5075999a705f0b221e015dedf8c178417bd275b779b9f5c8ffb188d5ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.4 MB (360414193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c5f30d79f1125ff8690fc32b85424dfdef0b0a44afcdf2bfada05d83ade807`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb4f97266d8057fbf15012235106a7241c66cc27475187eb6a6d3cdc9298e534 NEO4J_TARBALL=neo4j-community-4.3.22-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
# Fri, 25 Nov 2022 21:28:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:56 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 25 Nov 2022 21:29:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:29:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:29:12 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:29:12 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:29:13 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:29:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:29:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d71a3fe1def6b75de7f7ff1130ea7e74c95a2dfd24e595cef6717257cdbc74`  
		Last Modified: Fri, 25 Nov 2022 21:30:43 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5722c2c1f68c2b937dc4d40aec3002a78b8d9e98b2db9cd48845c066948bb465`  
		Last Modified: Fri, 25 Nov 2022 21:30:43 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129c8e4a104aa54f7b2e162de66b907339b4f814dcd75cbdac5b9865bc70cfb9`  
		Last Modified: Fri, 25 Nov 2022 21:30:50 GMT  
		Size: 130.5 MB (130534265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.22-enterprise`

```console
$ docker pull neo4j@sha256:5fe83ab550348243b26a485e186215623286434e9e14bff17fe241255a481ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.22-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:051098e3c43d4793a06ed129022ff04b29dce7b8f27c8108755e76e4e5231f83
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 MB (390917072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc03bf7c50b1f701639be4050df90adbaa1c788ee008bad49c83e05576c26af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:29:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=eac8dab9669ad128ae65fabfac982087eaebb6b3bc011e688d33eb379ed92629 NEO4J_TARBALL=neo4j-enterprise-4.3.22-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:29:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
# Fri, 25 Nov 2022 21:29:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:29:17 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Fri, 25 Nov 2022 21:29:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.22-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:29:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:29:35 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:29:35 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:29:35 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:29:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:29:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f950cb0c40c990ed0bc5702893f640fe0946d52fcb92c4360967910171beb5e`  
		Last Modified: Fri, 25 Nov 2022 21:31:02 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cfe0b7f886b6d1ce69e8b10819158b2e3a94de64215aebcc33499e69b016e4`  
		Last Modified: Fri, 25 Nov 2022 21:31:02 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b536c03580c1c21dcc7cd1ea82d6fb4f8830c7767742afb06fedf147ce4f2c5`  
		Last Modified: Fri, 25 Nov 2022 21:31:10 GMT  
		Size: 161.0 MB (161037149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:b680bf25e672202b3cccb17eb8d3a6de5a8c910d7dfdb5bd2b22cbec4633a370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:acf0ba298d912f3dc1649e482866368a816a3a38b21b59c68834c6da39493497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365299767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f402700ef4ad66dc80d3c8e998d05ccd47f42e1067bf61480180602d7389d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Fri, 25 Nov 2022 21:28:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:04 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 25 Nov 2022 21:28:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:28:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:28:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:28:22 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:28:22 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:28:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:28:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9fbf4fe053d5a41c521f707006954ad4acc0ed7adde532074ff8f462b22550`  
		Last Modified: Fri, 25 Nov 2022 21:30:05 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e9093383d554306f9eb8969c4aa5cb9e979c4d95254e532df9e75334e9820d`  
		Last Modified: Fri, 25 Nov 2022 21:30:05 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c58500421fd5dfe1e4fcd8fc8173e79d0839865a3b7fcbad3716d76c652be38`  
		Last Modified: Fri, 25 Nov 2022 21:30:12 GMT  
		Size: 135.4 MB (135419292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2159eb4c32fae86fdf5402b1341b821dfa2a6a17f0fdc432119fc992f14f8fe1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360549739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c8e49e3514d02cb87a1dda5f07015e483bbe25905fccfe1de40f6c4ae772bc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:20:18 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Tue, 06 Dec 2022 04:03:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:31 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Tue, 06 Dec 2022 04:03:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:41 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:41 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:41 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ee26ba69cd8afd37462741fda4929d6658730baa6af64ace9a30c2c6aa3b9`  
		Last Modified: Tue, 06 Dec 2022 02:31:55 GMT  
		Size: 195.2 MB (195201090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4042457744bdde95e750dc0d8f91830b05b4c95038df0151efa294ba35254dcd`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587f7be3c0a9780eff9e088fe5d7d294eb86e8ff738a7fdf45fbbe5747b975a`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee2e042e18cac7238ab144afea4d47952fa020013706e8891b94ce1b97ec7cb`  
		Last Modified: Tue, 06 Dec 2022 04:05:23 GMT  
		Size: 135.3 MB (135276275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:b680bf25e672202b3cccb17eb8d3a6de5a8c910d7dfdb5bd2b22cbec4633a370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:acf0ba298d912f3dc1649e482866368a816a3a38b21b59c68834c6da39493497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365299767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f402700ef4ad66dc80d3c8e998d05ccd47f42e1067bf61480180602d7389d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Fri, 25 Nov 2022 21:28:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:04 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 25 Nov 2022 21:28:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:28:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:28:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:28:22 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:28:22 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:28:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:28:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9fbf4fe053d5a41c521f707006954ad4acc0ed7adde532074ff8f462b22550`  
		Last Modified: Fri, 25 Nov 2022 21:30:05 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e9093383d554306f9eb8969c4aa5cb9e979c4d95254e532df9e75334e9820d`  
		Last Modified: Fri, 25 Nov 2022 21:30:05 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c58500421fd5dfe1e4fcd8fc8173e79d0839865a3b7fcbad3716d76c652be38`  
		Last Modified: Fri, 25 Nov 2022 21:30:12 GMT  
		Size: 135.4 MB (135419292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2159eb4c32fae86fdf5402b1341b821dfa2a6a17f0fdc432119fc992f14f8fe1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360549739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c8e49e3514d02cb87a1dda5f07015e483bbe25905fccfe1de40f6c4ae772bc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:20:18 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Tue, 06 Dec 2022 04:03:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:31 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Tue, 06 Dec 2022 04:03:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:41 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:41 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:41 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ee26ba69cd8afd37462741fda4929d6658730baa6af64ace9a30c2c6aa3b9`  
		Last Modified: Tue, 06 Dec 2022 02:31:55 GMT  
		Size: 195.2 MB (195201090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4042457744bdde95e750dc0d8f91830b05b4c95038df0151efa294ba35254dcd`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587f7be3c0a9780eff9e088fe5d7d294eb86e8ff738a7fdf45fbbe5747b975a`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee2e042e18cac7238ab144afea4d47952fa020013706e8891b94ce1b97ec7cb`  
		Last Modified: Tue, 06 Dec 2022 04:05:23 GMT  
		Size: 135.3 MB (135276275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:d726dafa9f2489766b7b1b8e372ffb54ea6ba719394feb53b6e398b559e286c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5bd52f1ed041278ec140811b4eb858827892041e9f05a939b058f21dbff1b2fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 MB (460486940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625a15633a01e678aa7708b2773f6036538bc6d994a05e526a28bd68bebfc83`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54531e7d1a7c381138fa527e1f5f22482d1687c04f237532b24fe42a1ef57491 NEO4J_TARBALL=neo4j-enterprise-4.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
# Fri, 25 Nov 2022 21:28:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:28 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 25 Nov 2022 21:28:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:28:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:28:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:28:50 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:28:50 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:28:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:28:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10dc1b50282c2a94c646b0ffe4960639bccce034cae8a428b4b6fe150127128`  
		Last Modified: Fri, 25 Nov 2022 21:30:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa0970df9e0057850b3364b765790a30cfea58056e880945bf796044524f37c`  
		Last Modified: Fri, 25 Nov 2022 21:30:24 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367851c3c4c158892279f6467bc4d3224ad4044ebcf7c9262d2cc342d6a08268`  
		Last Modified: Fri, 25 Nov 2022 21:30:35 GMT  
		Size: 230.6 MB (230606468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9399e811aa63764b3da7feb1ec77fe3be0c6ab720f4303fb8f4be7b0d7c5e8a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455737771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765db737bde4fc4121c228d2a56e4f778aaf93a7dd6673e55cf46c1fa21bea51`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:20:18 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54531e7d1a7c381138fa527e1f5f22482d1687c04f237532b24fe42a1ef57491 NEO4J_TARBALL=neo4j-enterprise-4.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
# Tue, 06 Dec 2022 04:03:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:45 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Tue, 06 Dec 2022 04:04:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:04:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:04:09 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:04:09 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:04:09 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:04:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ee26ba69cd8afd37462741fda4929d6658730baa6af64ace9a30c2c6aa3b9`  
		Last Modified: Tue, 06 Dec 2022 02:31:55 GMT  
		Size: 195.2 MB (195201090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975cf6d96b74e1c8512287aaf486fa2d7c6c955ecdd49165ce5f11769edf1078`  
		Last Modified: Tue, 06 Dec 2022 04:05:35 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a44601ca9f1668a6998d79aaa901495c04b32809c9b7f8e2bcf0193edc34df`  
		Last Modified: Tue, 06 Dec 2022 04:05:35 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16a015aa3588c3cf4c28b0b9b91fbb70d81bbcf59a9454849445c429b3923e0`  
		Last Modified: Tue, 06 Dec 2022 04:05:44 GMT  
		Size: 230.5 MB (230464308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.15`

```console
$ docker pull neo4j@sha256:b680bf25e672202b3cccb17eb8d3a6de5a8c910d7dfdb5bd2b22cbec4633a370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.15` - linux; amd64

```console
$ docker pull neo4j@sha256:acf0ba298d912f3dc1649e482866368a816a3a38b21b59c68834c6da39493497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365299767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f402700ef4ad66dc80d3c8e998d05ccd47f42e1067bf61480180602d7389d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Fri, 25 Nov 2022 21:28:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:04 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 25 Nov 2022 21:28:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:28:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:28:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:28:22 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:28:22 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:28:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:28:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9fbf4fe053d5a41c521f707006954ad4acc0ed7adde532074ff8f462b22550`  
		Last Modified: Fri, 25 Nov 2022 21:30:05 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e9093383d554306f9eb8969c4aa5cb9e979c4d95254e532df9e75334e9820d`  
		Last Modified: Fri, 25 Nov 2022 21:30:05 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c58500421fd5dfe1e4fcd8fc8173e79d0839865a3b7fcbad3716d76c652be38`  
		Last Modified: Fri, 25 Nov 2022 21:30:12 GMT  
		Size: 135.4 MB (135419292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.15` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2159eb4c32fae86fdf5402b1341b821dfa2a6a17f0fdc432119fc992f14f8fe1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360549739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c8e49e3514d02cb87a1dda5f07015e483bbe25905fccfe1de40f6c4ae772bc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:20:18 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Tue, 06 Dec 2022 04:03:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:31 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Tue, 06 Dec 2022 04:03:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:41 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:41 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:41 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ee26ba69cd8afd37462741fda4929d6658730baa6af64ace9a30c2c6aa3b9`  
		Last Modified: Tue, 06 Dec 2022 02:31:55 GMT  
		Size: 195.2 MB (195201090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4042457744bdde95e750dc0d8f91830b05b4c95038df0151efa294ba35254dcd`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587f7be3c0a9780eff9e088fe5d7d294eb86e8ff738a7fdf45fbbe5747b975a`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee2e042e18cac7238ab144afea4d47952fa020013706e8891b94ce1b97ec7cb`  
		Last Modified: Tue, 06 Dec 2022 04:05:23 GMT  
		Size: 135.3 MB (135276275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.15-community`

```console
$ docker pull neo4j@sha256:b680bf25e672202b3cccb17eb8d3a6de5a8c910d7dfdb5bd2b22cbec4633a370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.15-community` - linux; amd64

```console
$ docker pull neo4j@sha256:acf0ba298d912f3dc1649e482866368a816a3a38b21b59c68834c6da39493497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365299767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f402700ef4ad66dc80d3c8e998d05ccd47f42e1067bf61480180602d7389d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Fri, 25 Nov 2022 21:28:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:04 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 25 Nov 2022 21:28:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:28:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:28:22 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:28:22 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:28:22 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:28:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:28:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9fbf4fe053d5a41c521f707006954ad4acc0ed7adde532074ff8f462b22550`  
		Last Modified: Fri, 25 Nov 2022 21:30:05 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e9093383d554306f9eb8969c4aa5cb9e979c4d95254e532df9e75334e9820d`  
		Last Modified: Fri, 25 Nov 2022 21:30:05 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c58500421fd5dfe1e4fcd8fc8173e79d0839865a3b7fcbad3716d76c652be38`  
		Last Modified: Fri, 25 Nov 2022 21:30:12 GMT  
		Size: 135.4 MB (135419292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.15-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2159eb4c32fae86fdf5402b1341b821dfa2a6a17f0fdc432119fc992f14f8fe1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360549739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c8e49e3514d02cb87a1dda5f07015e483bbe25905fccfe1de40f6c4ae772bc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:20:18 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=310527e15a88fc6c874148e1807b9dbdf3c094c30bb27e7bba08655f1ea06352 NEO4J_TARBALL=neo4j-community-4.4.15-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
# Tue, 06 Dec 2022 04:03:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:31 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Tue, 06 Dec 2022 04:03:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:41 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:41 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:41 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ee26ba69cd8afd37462741fda4929d6658730baa6af64ace9a30c2c6aa3b9`  
		Last Modified: Tue, 06 Dec 2022 02:31:55 GMT  
		Size: 195.2 MB (195201090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4042457744bdde95e750dc0d8f91830b05b4c95038df0151efa294ba35254dcd`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f587f7be3c0a9780eff9e088fe5d7d294eb86e8ff738a7fdf45fbbe5747b975a`  
		Last Modified: Tue, 06 Dec 2022 04:05:16 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee2e042e18cac7238ab144afea4d47952fa020013706e8891b94ce1b97ec7cb`  
		Last Modified: Tue, 06 Dec 2022 04:05:23 GMT  
		Size: 135.3 MB (135276275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.15-enterprise`

```console
$ docker pull neo4j@sha256:d726dafa9f2489766b7b1b8e372ffb54ea6ba719394feb53b6e398b559e286c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.15-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5bd52f1ed041278ec140811b4eb858827892041e9f05a939b058f21dbff1b2fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.5 MB (460486940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3625a15633a01e678aa7708b2773f6036538bc6d994a05e526a28bd68bebfc83`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Fri, 25 Nov 2022 21:28:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54531e7d1a7c381138fa527e1f5f22482d1687c04f237532b24fe42a1ef57491 NEO4J_TARBALL=neo4j-enterprise-4.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 25 Nov 2022 21:28:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
# Fri, 25 Nov 2022 21:28:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 25 Nov 2022 21:28:28 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Fri, 25 Nov 2022 21:28:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Nov 2022 21:28:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Nov 2022 21:28:50 GMT
WORKDIR /var/lib/neo4j
# Fri, 25 Nov 2022 21:28:50 GMT
VOLUME [/data /logs]
# Fri, 25 Nov 2022 21:28:50 GMT
EXPOSE 7473 7474 7687
# Fri, 25 Nov 2022 21:28:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 25 Nov 2022 21:28:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b10dc1b50282c2a94c646b0ffe4960639bccce034cae8a428b4b6fe150127128`  
		Last Modified: Fri, 25 Nov 2022 21:30:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa0970df9e0057850b3364b765790a30cfea58056e880945bf796044524f37c`  
		Last Modified: Fri, 25 Nov 2022 21:30:24 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367851c3c4c158892279f6467bc4d3224ad4044ebcf7c9262d2cc342d6a08268`  
		Last Modified: Fri, 25 Nov 2022 21:30:35 GMT  
		Size: 230.6 MB (230606468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.15-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9399e811aa63764b3da7feb1ec77fe3be0c6ab720f4303fb8f4be7b0d7c5e8a0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.7 MB (455737771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765db737bde4fc4121c228d2a56e4f778aaf93a7dd6673e55cf46c1fa21bea51`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:20:18 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=54531e7d1a7c381138fa527e1f5f22482d1687c04f237532b24fe42a1ef57491 NEO4J_TARBALL=neo4j-enterprise-4.4.15-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:44 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
# Tue, 06 Dec 2022 04:03:45 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:45 GMT
COPY multi:d79a5b7ba73da37dcfa9335950c203f23710473d4bdc3c12de4d0b0c62fbd733 in /startup/ 
# Tue, 06 Dec 2022 04:04:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.15-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:04:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:04:09 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:04:09 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:04:09 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:04:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:04:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ee26ba69cd8afd37462741fda4929d6658730baa6af64ace9a30c2c6aa3b9`  
		Last Modified: Tue, 06 Dec 2022 02:31:55 GMT  
		Size: 195.2 MB (195201090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975cf6d96b74e1c8512287aaf486fa2d7c6c955ecdd49165ce5f11769edf1078`  
		Last Modified: Tue, 06 Dec 2022 04:05:35 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a44601ca9f1668a6998d79aaa901495c04b32809c9b7f8e2bcf0193edc34df`  
		Last Modified: Tue, 06 Dec 2022 04:05:35 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16a015aa3588c3cf4c28b0b9b91fbb70d81bbcf59a9454849445c429b3923e0`  
		Last Modified: Tue, 06 Dec 2022 04:05:44 GMT  
		Size: 230.5 MB (230464308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:b3dc4e466b1f7768f36eab9830229ae53547a748fdc4efef096657ce36b1be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:00d19bb846618f4a014868c6ed1e9c16bb37b3cd08cabb60a16348d8fed6a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336774481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee0b833f524df181bc1cdb33a65c9d7d40ba34452e1bd2b7a7323c751659023`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:27 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:27 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:27 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398f7542920d6bd98a9af713e2d7e2ebbaface91042b0e3a29e211ade0a827a3`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacdd549a219adcf7daa416dea38438cd91e610c033800425bb922605d8d85a`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d107c6cefe664bd054035614d7cfacaab9910ea18031f603011c1591b60c0`  
		Last Modified: Mon, 21 Nov 2022 19:26:37 GMT  
		Size: 112.9 MB (112918550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f135a1fc3a3158e5f9bdf7cc79ba0ecb7b0ce04847937ab7b37e4988e33bcff4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b75b9bfe32a255333142a7fc1e1e23e2c95efa0e6c5f0696a17b4ca650952e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:02:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:02:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:10 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:10 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25298c694c11fad6a5841954aa4df84c3e180cae5a5d8d1b9eab087d9e61e342`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc321b6cef4d7cb780374ed4c536dcbe4d470df0273b4373ce57953ad5676707`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b20ee9a4e14fd3beb4832ab9f332c72abed7ac15e7a1bded3b43bd738e592`  
		Last Modified: Tue, 06 Dec 2022 04:04:37 GMT  
		Size: 112.8 MB (112775730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:b3dc4e466b1f7768f36eab9830229ae53547a748fdc4efef096657ce36b1be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:00d19bb846618f4a014868c6ed1e9c16bb37b3cd08cabb60a16348d8fed6a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336774481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee0b833f524df181bc1cdb33a65c9d7d40ba34452e1bd2b7a7323c751659023`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:27 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:27 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:27 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398f7542920d6bd98a9af713e2d7e2ebbaface91042b0e3a29e211ade0a827a3`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacdd549a219adcf7daa416dea38438cd91e610c033800425bb922605d8d85a`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d107c6cefe664bd054035614d7cfacaab9910ea18031f603011c1591b60c0`  
		Last Modified: Mon, 21 Nov 2022 19:26:37 GMT  
		Size: 112.9 MB (112918550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f135a1fc3a3158e5f9bdf7cc79ba0ecb7b0ce04847937ab7b37e4988e33bcff4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b75b9bfe32a255333142a7fc1e1e23e2c95efa0e6c5f0696a17b4ca650952e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:02:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:02:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:10 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:10 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25298c694c11fad6a5841954aa4df84c3e180cae5a5d8d1b9eab087d9e61e342`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc321b6cef4d7cb780374ed4c536dcbe4d470df0273b4373ce57953ad5676707`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b20ee9a4e14fd3beb4832ab9f332c72abed7ac15e7a1bded3b43bd738e592`  
		Last Modified: Tue, 06 Dec 2022 04:04:37 GMT  
		Size: 112.8 MB (112775730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:598479babc48baf43a51463780781034d95c8861de69de6384119984a66800fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b43013f0cd7d74e1e4497d3756cdb7ccb1b8b219bad3407c58956e215ef3a56f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432869622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f110c02412218cfb5462456b109fbccc713f6be834eb4eff160dcc02a1037b63`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:32 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:52 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:53 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3472f19c8a5a24c108dc649a7497094ed5be4db2d33246bb3b0405224ac6bfc2`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4e10d12e10c3659084ea62f78809a048ce5b0e3607f6cfff686434d0332bcd`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f71541831b0253791f32bf49c5dd3d9c3a0794bf23ea63b8584caa7fbe2bcf7`  
		Last Modified: Mon, 21 Nov 2022 19:27:06 GMT  
		Size: 209.0 MB (209013694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:90f8871f5adcc5ed41020731e3b7cd55e9dfcd9de2b31439ba4fc7e379f1af12
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430158153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05a45fbc4c5d91679ccfcca0f863645d1317c21c76c08137670f66a74a685e2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:03:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:27 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:27 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:27 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1128db2f4b08bc6f628623eac1f80cc5279c0cdcd21f45b8739eb59a680c34c`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0951e28fc5d1a0ac9065b81777666b227d565470fa92e3004b8cc1094beb4701`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b160227ed7d13a3c1655a1fac0ee736792ee4d20a71884670c1dcd791b10c`  
		Last Modified: Tue, 06 Dec 2022 04:05:04 GMT  
		Size: 208.9 MB (208870552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.2`

```console
$ docker pull neo4j@sha256:b3dc4e466b1f7768f36eab9830229ae53547a748fdc4efef096657ce36b1be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2` - linux; amd64

```console
$ docker pull neo4j@sha256:00d19bb846618f4a014868c6ed1e9c16bb37b3cd08cabb60a16348d8fed6a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336774481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee0b833f524df181bc1cdb33a65c9d7d40ba34452e1bd2b7a7323c751659023`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:27 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:27 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:27 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398f7542920d6bd98a9af713e2d7e2ebbaface91042b0e3a29e211ade0a827a3`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacdd549a219adcf7daa416dea38438cd91e610c033800425bb922605d8d85a`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d107c6cefe664bd054035614d7cfacaab9910ea18031f603011c1591b60c0`  
		Last Modified: Mon, 21 Nov 2022 19:26:37 GMT  
		Size: 112.9 MB (112918550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f135a1fc3a3158e5f9bdf7cc79ba0ecb7b0ce04847937ab7b37e4988e33bcff4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b75b9bfe32a255333142a7fc1e1e23e2c95efa0e6c5f0696a17b4ca650952e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:02:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:02:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:10 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:10 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25298c694c11fad6a5841954aa4df84c3e180cae5a5d8d1b9eab087d9e61e342`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc321b6cef4d7cb780374ed4c536dcbe4d470df0273b4373ce57953ad5676707`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b20ee9a4e14fd3beb4832ab9f332c72abed7ac15e7a1bded3b43bd738e592`  
		Last Modified: Tue, 06 Dec 2022 04:04:37 GMT  
		Size: 112.8 MB (112775730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.2-enterprise`

```console
$ docker pull neo4j@sha256:598479babc48baf43a51463780781034d95c8861de69de6384119984a66800fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b43013f0cd7d74e1e4497d3756cdb7ccb1b8b219bad3407c58956e215ef3a56f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432869622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f110c02412218cfb5462456b109fbccc713f6be834eb4eff160dcc02a1037b63`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:32 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:52 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:53 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3472f19c8a5a24c108dc649a7497094ed5be4db2d33246bb3b0405224ac6bfc2`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4e10d12e10c3659084ea62f78809a048ce5b0e3607f6cfff686434d0332bcd`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f71541831b0253791f32bf49c5dd3d9c3a0794bf23ea63b8584caa7fbe2bcf7`  
		Last Modified: Mon, 21 Nov 2022 19:27:06 GMT  
		Size: 209.0 MB (209013694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:90f8871f5adcc5ed41020731e3b7cd55e9dfcd9de2b31439ba4fc7e379f1af12
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430158153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05a45fbc4c5d91679ccfcca0f863645d1317c21c76c08137670f66a74a685e2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:03:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:27 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:27 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:27 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1128db2f4b08bc6f628623eac1f80cc5279c0cdcd21f45b8739eb59a680c34c`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0951e28fc5d1a0ac9065b81777666b227d565470fa92e3004b8cc1094beb4701`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b160227ed7d13a3c1655a1fac0ee736792ee4d20a71884670c1dcd791b10c`  
		Last Modified: Tue, 06 Dec 2022 04:05:04 GMT  
		Size: 208.9 MB (208870552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.2.0`

```console
$ docker pull neo4j@sha256:b3dc4e466b1f7768f36eab9830229ae53547a748fdc4efef096657ce36b1be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2.0` - linux; amd64

```console
$ docker pull neo4j@sha256:00d19bb846618f4a014868c6ed1e9c16bb37b3cd08cabb60a16348d8fed6a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336774481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee0b833f524df181bc1cdb33a65c9d7d40ba34452e1bd2b7a7323c751659023`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:27 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:27 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:27 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398f7542920d6bd98a9af713e2d7e2ebbaface91042b0e3a29e211ade0a827a3`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacdd549a219adcf7daa416dea38438cd91e610c033800425bb922605d8d85a`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d107c6cefe664bd054035614d7cfacaab9910ea18031f603011c1591b60c0`  
		Last Modified: Mon, 21 Nov 2022 19:26:37 GMT  
		Size: 112.9 MB (112918550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f135a1fc3a3158e5f9bdf7cc79ba0ecb7b0ce04847937ab7b37e4988e33bcff4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b75b9bfe32a255333142a7fc1e1e23e2c95efa0e6c5f0696a17b4ca650952e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:02:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:02:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:10 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:10 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25298c694c11fad6a5841954aa4df84c3e180cae5a5d8d1b9eab087d9e61e342`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc321b6cef4d7cb780374ed4c536dcbe4d470df0273b4373ce57953ad5676707`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b20ee9a4e14fd3beb4832ab9f332c72abed7ac15e7a1bded3b43bd738e592`  
		Last Modified: Tue, 06 Dec 2022 04:04:37 GMT  
		Size: 112.8 MB (112775730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.2.0-community`

```console
$ docker pull neo4j@sha256:b3dc4e466b1f7768f36eab9830229ae53547a748fdc4efef096657ce36b1be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:00d19bb846618f4a014868c6ed1e9c16bb37b3cd08cabb60a16348d8fed6a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336774481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee0b833f524df181bc1cdb33a65c9d7d40ba34452e1bd2b7a7323c751659023`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:27 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:27 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:27 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398f7542920d6bd98a9af713e2d7e2ebbaface91042b0e3a29e211ade0a827a3`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacdd549a219adcf7daa416dea38438cd91e610c033800425bb922605d8d85a`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d107c6cefe664bd054035614d7cfacaab9910ea18031f603011c1591b60c0`  
		Last Modified: Mon, 21 Nov 2022 19:26:37 GMT  
		Size: 112.9 MB (112918550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f135a1fc3a3158e5f9bdf7cc79ba0ecb7b0ce04847937ab7b37e4988e33bcff4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b75b9bfe32a255333142a7fc1e1e23e2c95efa0e6c5f0696a17b4ca650952e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:02:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:02:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:10 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:10 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25298c694c11fad6a5841954aa4df84c3e180cae5a5d8d1b9eab087d9e61e342`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc321b6cef4d7cb780374ed4c536dcbe4d470df0273b4373ce57953ad5676707`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b20ee9a4e14fd3beb4832ab9f332c72abed7ac15e7a1bded3b43bd738e592`  
		Last Modified: Tue, 06 Dec 2022 04:04:37 GMT  
		Size: 112.8 MB (112775730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.2.0-enterprise`

```console
$ docker pull neo4j@sha256:598479babc48baf43a51463780781034d95c8861de69de6384119984a66800fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.2.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b43013f0cd7d74e1e4497d3756cdb7ccb1b8b219bad3407c58956e215ef3a56f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432869622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f110c02412218cfb5462456b109fbccc713f6be834eb4eff160dcc02a1037b63`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:32 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:52 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:53 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3472f19c8a5a24c108dc649a7497094ed5be4db2d33246bb3b0405224ac6bfc2`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4e10d12e10c3659084ea62f78809a048ce5b0e3607f6cfff686434d0332bcd`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f71541831b0253791f32bf49c5dd3d9c3a0794bf23ea63b8584caa7fbe2bcf7`  
		Last Modified: Mon, 21 Nov 2022 19:27:06 GMT  
		Size: 209.0 MB (209013694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.2.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:90f8871f5adcc5ed41020731e3b7cd55e9dfcd9de2b31439ba4fc7e379f1af12
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430158153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05a45fbc4c5d91679ccfcca0f863645d1317c21c76c08137670f66a74a685e2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:03:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:27 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:27 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:27 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1128db2f4b08bc6f628623eac1f80cc5279c0cdcd21f45b8739eb59a680c34c`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0951e28fc5d1a0ac9065b81777666b227d565470fa92e3004b8cc1094beb4701`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b160227ed7d13a3c1655a1fac0ee736792ee4d20a71884670c1dcd791b10c`  
		Last Modified: Tue, 06 Dec 2022 04:05:04 GMT  
		Size: 208.9 MB (208870552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:b3dc4e466b1f7768f36eab9830229ae53547a748fdc4efef096657ce36b1be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:00d19bb846618f4a014868c6ed1e9c16bb37b3cd08cabb60a16348d8fed6a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336774481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee0b833f524df181bc1cdb33a65c9d7d40ba34452e1bd2b7a7323c751659023`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:27 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:27 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:27 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398f7542920d6bd98a9af713e2d7e2ebbaface91042b0e3a29e211ade0a827a3`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacdd549a219adcf7daa416dea38438cd91e610c033800425bb922605d8d85a`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d107c6cefe664bd054035614d7cfacaab9910ea18031f603011c1591b60c0`  
		Last Modified: Mon, 21 Nov 2022 19:26:37 GMT  
		Size: 112.9 MB (112918550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f135a1fc3a3158e5f9bdf7cc79ba0ecb7b0ce04847937ab7b37e4988e33bcff4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b75b9bfe32a255333142a7fc1e1e23e2c95efa0e6c5f0696a17b4ca650952e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:02:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:02:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:10 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:10 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25298c694c11fad6a5841954aa4df84c3e180cae5a5d8d1b9eab087d9e61e342`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc321b6cef4d7cb780374ed4c536dcbe4d470df0273b4373ce57953ad5676707`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b20ee9a4e14fd3beb4832ab9f332c72abed7ac15e7a1bded3b43bd738e592`  
		Last Modified: Tue, 06 Dec 2022 04:04:37 GMT  
		Size: 112.8 MB (112775730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:598479babc48baf43a51463780781034d95c8861de69de6384119984a66800fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b43013f0cd7d74e1e4497d3756cdb7ccb1b8b219bad3407c58956e215ef3a56f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432869622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f110c02412218cfb5462456b109fbccc713f6be834eb4eff160dcc02a1037b63`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:32 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:52 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:53 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3472f19c8a5a24c108dc649a7497094ed5be4db2d33246bb3b0405224ac6bfc2`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4e10d12e10c3659084ea62f78809a048ce5b0e3607f6cfff686434d0332bcd`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f71541831b0253791f32bf49c5dd3d9c3a0794bf23ea63b8584caa7fbe2bcf7`  
		Last Modified: Mon, 21 Nov 2022 19:27:06 GMT  
		Size: 209.0 MB (209013694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:90f8871f5adcc5ed41020731e3b7cd55e9dfcd9de2b31439ba4fc7e379f1af12
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430158153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05a45fbc4c5d91679ccfcca0f863645d1317c21c76c08137670f66a74a685e2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:03:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:27 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:27 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:27 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1128db2f4b08bc6f628623eac1f80cc5279c0cdcd21f45b8739eb59a680c34c`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0951e28fc5d1a0ac9065b81777666b227d565470fa92e3004b8cc1094beb4701`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b160227ed7d13a3c1655a1fac0ee736792ee4d20a71884670c1dcd791b10c`  
		Last Modified: Tue, 06 Dec 2022 04:05:04 GMT  
		Size: 208.9 MB (208870552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:b3dc4e466b1f7768f36eab9830229ae53547a748fdc4efef096657ce36b1be41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:00d19bb846618f4a014868c6ed1e9c16bb37b3cd08cabb60a16348d8fed6a978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336774481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee0b833f524df181bc1cdb33a65c9d7d40ba34452e1bd2b7a7323c751659023`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:13 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:27 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:27 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:27 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398f7542920d6bd98a9af713e2d7e2ebbaface91042b0e3a29e211ade0a827a3`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beacdd549a219adcf7daa416dea38438cd91e610c033800425bb922605d8d85a`  
		Last Modified: Mon, 21 Nov 2022 19:26:32 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d107c6cefe664bd054035614d7cfacaab9910ea18031f603011c1591b60c0`  
		Last Modified: Mon, 21 Nov 2022 19:26:37 GMT  
		Size: 112.9 MB (112918550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f135a1fc3a3158e5f9bdf7cc79ba0ecb7b0ce04847937ab7b37e4988e33bcff4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334063333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b75b9bfe32a255333142a7fc1e1e23e2c95efa0e6c5f0696a17b4ca650952e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:02:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5fe22a0ff4cb11152b40b7ba0228f0e9af6a0b899006c413adf498314fd4b4f9 NEO4J_TARBALL=neo4j-community-5.2.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:02:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:02:59 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:10 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:10 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:10 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25298c694c11fad6a5841954aa4df84c3e180cae5a5d8d1b9eab087d9e61e342`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc321b6cef4d7cb780374ed4c536dcbe4d470df0273b4373ce57953ad5676707`  
		Last Modified: Tue, 06 Dec 2022 04:04:32 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b20ee9a4e14fd3beb4832ab9f332c72abed7ac15e7a1bded3b43bd738e592`  
		Last Modified: Tue, 06 Dec 2022 04:04:37 GMT  
		Size: 112.8 MB (112775730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
