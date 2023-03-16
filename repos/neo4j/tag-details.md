<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.18`](#neo4j4418)
-	[`neo4j:4.4.18-community`](#neo4j4418-community)
-	[`neo4j:4.4.18-enterprise`](#neo4j4418-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.5`](#neo4j55)
-	[`neo4j:5.5-enterprise`](#neo4j55-enterprise)
-	[`neo4j:5.5.0`](#neo4j550)
-	[`neo4j:5.5.0-community`](#neo4j550-community)
-	[`neo4j:5.5.0-enterprise`](#neo4j550-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:f4cedc2ec96c92efaf9c20724077b3c3f4c90a1c7f7b5c0859e2dc9e6b6a339f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:a2c7e4389c7ae5f728679d8fcb313c239dc2f50e31573426c3c5bf7c6879cd6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366801810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567b03d340d9ec5bd28ebda3ab0444868d87913da04442c4356f80d85c4df5f2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:09:28 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 07:09:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:30 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 07:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:09:42 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:09:42 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:09:42 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cdbfa885c40f74f375de05f596451f2eb302e89adeb4e35299b8e7ca9c4ed`  
		Last Modified: Thu, 16 Mar 2023 07:11:39 GMT  
		Size: 198.5 MB (198475989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9938df98b0c1d7f82713df12407bd4359239d297bfcd3f85cf712f0a0755355`  
		Last Modified: Thu, 16 Mar 2023 07:11:25 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aefe826533e5d715c0ebfdca8cc449ff4df19c31ed291e9217933a7535cd97a`  
		Last Modified: Thu, 16 Mar 2023 07:11:25 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d4b582c7fcc3d54829ced68d008521894b420f4408ffb4334200a84f9f433`  
		Last Modified: Thu, 16 Mar 2023 07:11:32 GMT  
		Size: 136.9 MB (136902128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb0b73ca840cb389341a6a8b9a5a8d1003a54bef77cba3d36a3fb109f1c0971c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362075787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f035a628b41c928ac888a6e46e1dfac83b2ad5c03c81095ac181aba29a627a4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:50:13 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:12:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:12:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 06:12:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:12:10 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 06:12:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:25 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:25 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849668ad76f372948228ac47245422eeb38d27a3c72428341214ee297da1d92d`  
		Last Modified: Thu, 16 Mar 2023 05:04:48 GMT  
		Size: 195.2 MB (195242533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef42568794418609d2f84f8257f12e19cb042dbc1ee3d02d4d83d9e8f6dd848c`  
		Last Modified: Thu, 16 Mar 2023 06:13:52 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2534248e2dbbfe4374eeb72816ad0e59f046ec793011f412291da9412e6801`  
		Last Modified: Thu, 16 Mar 2023 06:13:52 GMT  
		Size: 8.4 KB (8426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55dea049fd02a97c84d7338b2d0c05acfa3c846ed53d81aa6fd9014a13d211b`  
		Last Modified: Thu, 16 Mar 2023 06:13:58 GMT  
		Size: 136.8 MB (136758126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:f4cedc2ec96c92efaf9c20724077b3c3f4c90a1c7f7b5c0859e2dc9e6b6a339f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a2c7e4389c7ae5f728679d8fcb313c239dc2f50e31573426c3c5bf7c6879cd6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366801810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567b03d340d9ec5bd28ebda3ab0444868d87913da04442c4356f80d85c4df5f2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:09:28 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 07:09:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:30 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 07:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:09:42 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:09:42 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:09:42 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cdbfa885c40f74f375de05f596451f2eb302e89adeb4e35299b8e7ca9c4ed`  
		Last Modified: Thu, 16 Mar 2023 07:11:39 GMT  
		Size: 198.5 MB (198475989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9938df98b0c1d7f82713df12407bd4359239d297bfcd3f85cf712f0a0755355`  
		Last Modified: Thu, 16 Mar 2023 07:11:25 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aefe826533e5d715c0ebfdca8cc449ff4df19c31ed291e9217933a7535cd97a`  
		Last Modified: Thu, 16 Mar 2023 07:11:25 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d4b582c7fcc3d54829ced68d008521894b420f4408ffb4334200a84f9f433`  
		Last Modified: Thu, 16 Mar 2023 07:11:32 GMT  
		Size: 136.9 MB (136902128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb0b73ca840cb389341a6a8b9a5a8d1003a54bef77cba3d36a3fb109f1c0971c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362075787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f035a628b41c928ac888a6e46e1dfac83b2ad5c03c81095ac181aba29a627a4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:50:13 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:12:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:12:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 06:12:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:12:10 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 06:12:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:25 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:25 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849668ad76f372948228ac47245422eeb38d27a3c72428341214ee297da1d92d`  
		Last Modified: Thu, 16 Mar 2023 05:04:48 GMT  
		Size: 195.2 MB (195242533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef42568794418609d2f84f8257f12e19cb042dbc1ee3d02d4d83d9e8f6dd848c`  
		Last Modified: Thu, 16 Mar 2023 06:13:52 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2534248e2dbbfe4374eeb72816ad0e59f046ec793011f412291da9412e6801`  
		Last Modified: Thu, 16 Mar 2023 06:13:52 GMT  
		Size: 8.4 KB (8426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55dea049fd02a97c84d7338b2d0c05acfa3c846ed53d81aa6fd9014a13d211b`  
		Last Modified: Thu, 16 Mar 2023 06:13:58 GMT  
		Size: 136.8 MB (136758126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:fab801a2ec6a88d1ecf2f103ead76c2be123383b91000e51f75b718f73c7e1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:a5c630bdf0a792f2957eba59ab46b0a1ad3221663399a80e742c7358208e6578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.2 MB (463205386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eddb7576a4decb046eb642333eac99f75bac948bd72a2b587a1132c38967647`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:09:28 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79d7283199af9e4830dbf79ff36b98d8851b342724edd741785b91bad33f7d73 NEO4J_TARBALL=neo4j-enterprise-4.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 07:09:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:49 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 07:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:10:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:10:03 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:10:03 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:10:03 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cdbfa885c40f74f375de05f596451f2eb302e89adeb4e35299b8e7ca9c4ed`  
		Last Modified: Thu, 16 Mar 2023 07:11:39 GMT  
		Size: 198.5 MB (198475989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c6a017da58e31f23b2b5533ba126600cc2dc59d99ec83f967e61e178d46907`  
		Last Modified: Thu, 16 Mar 2023 07:11:51 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b24bb5867a0c2cd07294507bcc79f9d5a471409dbef07747c23fc9be32da47`  
		Last Modified: Thu, 16 Mar 2023 07:11:51 GMT  
		Size: 8.4 KB (8426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bacb656612684e64003f420fe3b0622c4318a5ecf15845c180bb0e5224fe2a`  
		Last Modified: Thu, 16 Mar 2023 07:12:02 GMT  
		Size: 233.3 MB (233305708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1217ece5a6f6ca3c6a144653873c31197ed308a48f237328d2c02c1c16cf2fa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.5 MB (458481619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaba0e5a70f350db609a362ef9f32f7ed40b855041a9914cd7c514f1dd6da6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:50:13 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:12:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79d7283199af9e4830dbf79ff36b98d8851b342724edd741785b91bad33f7d73 NEO4J_TARBALL=neo4j-enterprise-4.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:12:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 06:12:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:12:30 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 06:12:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:43 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:44 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:44 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849668ad76f372948228ac47245422eeb38d27a3c72428341214ee297da1d92d`  
		Last Modified: Thu, 16 Mar 2023 05:04:48 GMT  
		Size: 195.2 MB (195242533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fd4923d2bbd76b27c8dffad7e304369264163d19b85e9ee52158e51698fcb9`  
		Last Modified: Thu, 16 Mar 2023 06:14:11 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418ab8174f12a4788a7ae7f81e5bd4e2b66ab371a185d6795286d6c075c5cc7a`  
		Last Modified: Thu, 16 Mar 2023 06:14:11 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef7fc4d0a700eb7ab9cde7f73b1e38118fa4014857953b0b267861df8980da7`  
		Last Modified: Thu, 16 Mar 2023 06:14:20 GMT  
		Size: 233.2 MB (233163962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.18`

```console
$ docker pull neo4j@sha256:f4cedc2ec96c92efaf9c20724077b3c3f4c90a1c7f7b5c0859e2dc9e6b6a339f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.18` - linux; amd64

```console
$ docker pull neo4j@sha256:a2c7e4389c7ae5f728679d8fcb313c239dc2f50e31573426c3c5bf7c6879cd6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366801810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567b03d340d9ec5bd28ebda3ab0444868d87913da04442c4356f80d85c4df5f2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:09:28 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 07:09:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:30 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 07:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:09:42 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:09:42 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:09:42 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cdbfa885c40f74f375de05f596451f2eb302e89adeb4e35299b8e7ca9c4ed`  
		Last Modified: Thu, 16 Mar 2023 07:11:39 GMT  
		Size: 198.5 MB (198475989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9938df98b0c1d7f82713df12407bd4359239d297bfcd3f85cf712f0a0755355`  
		Last Modified: Thu, 16 Mar 2023 07:11:25 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aefe826533e5d715c0ebfdca8cc449ff4df19c31ed291e9217933a7535cd97a`  
		Last Modified: Thu, 16 Mar 2023 07:11:25 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d4b582c7fcc3d54829ced68d008521894b420f4408ffb4334200a84f9f433`  
		Last Modified: Thu, 16 Mar 2023 07:11:32 GMT  
		Size: 136.9 MB (136902128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.18` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb0b73ca840cb389341a6a8b9a5a8d1003a54bef77cba3d36a3fb109f1c0971c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362075787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f035a628b41c928ac888a6e46e1dfac83b2ad5c03c81095ac181aba29a627a4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:50:13 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:12:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:12:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 06:12:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:12:10 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 06:12:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:25 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:25 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849668ad76f372948228ac47245422eeb38d27a3c72428341214ee297da1d92d`  
		Last Modified: Thu, 16 Mar 2023 05:04:48 GMT  
		Size: 195.2 MB (195242533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef42568794418609d2f84f8257f12e19cb042dbc1ee3d02d4d83d9e8f6dd848c`  
		Last Modified: Thu, 16 Mar 2023 06:13:52 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2534248e2dbbfe4374eeb72816ad0e59f046ec793011f412291da9412e6801`  
		Last Modified: Thu, 16 Mar 2023 06:13:52 GMT  
		Size: 8.4 KB (8426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55dea049fd02a97c84d7338b2d0c05acfa3c846ed53d81aa6fd9014a13d211b`  
		Last Modified: Thu, 16 Mar 2023 06:13:58 GMT  
		Size: 136.8 MB (136758126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.18-community`

```console
$ docker pull neo4j@sha256:f4cedc2ec96c92efaf9c20724077b3c3f4c90a1c7f7b5c0859e2dc9e6b6a339f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.18-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a2c7e4389c7ae5f728679d8fcb313c239dc2f50e31573426c3c5bf7c6879cd6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366801810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567b03d340d9ec5bd28ebda3ab0444868d87913da04442c4356f80d85c4df5f2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:09:28 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:29 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 07:09:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:30 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 07:09:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:09:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:09:42 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:09:42 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:09:42 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:09:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:09:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cdbfa885c40f74f375de05f596451f2eb302e89adeb4e35299b8e7ca9c4ed`  
		Last Modified: Thu, 16 Mar 2023 07:11:39 GMT  
		Size: 198.5 MB (198475989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9938df98b0c1d7f82713df12407bd4359239d297bfcd3f85cf712f0a0755355`  
		Last Modified: Thu, 16 Mar 2023 07:11:25 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aefe826533e5d715c0ebfdca8cc449ff4df19c31ed291e9217933a7535cd97a`  
		Last Modified: Thu, 16 Mar 2023 07:11:25 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45d4b582c7fcc3d54829ced68d008521894b420f4408ffb4334200a84f9f433`  
		Last Modified: Thu, 16 Mar 2023 07:11:32 GMT  
		Size: 136.9 MB (136902128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.18-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb0b73ca840cb389341a6a8b9a5a8d1003a54bef77cba3d36a3fb109f1c0971c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362075787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f035a628b41c928ac888a6e46e1dfac83b2ad5c03c81095ac181aba29a627a4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:50:13 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:12:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:12:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 06:12:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:12:10 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 06:12:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:25 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:25 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:25 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849668ad76f372948228ac47245422eeb38d27a3c72428341214ee297da1d92d`  
		Last Modified: Thu, 16 Mar 2023 05:04:48 GMT  
		Size: 195.2 MB (195242533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef42568794418609d2f84f8257f12e19cb042dbc1ee3d02d4d83d9e8f6dd848c`  
		Last Modified: Thu, 16 Mar 2023 06:13:52 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2534248e2dbbfe4374eeb72816ad0e59f046ec793011f412291da9412e6801`  
		Last Modified: Thu, 16 Mar 2023 06:13:52 GMT  
		Size: 8.4 KB (8426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55dea049fd02a97c84d7338b2d0c05acfa3c846ed53d81aa6fd9014a13d211b`  
		Last Modified: Thu, 16 Mar 2023 06:13:58 GMT  
		Size: 136.8 MB (136758126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.18-enterprise`

```console
$ docker pull neo4j@sha256:fab801a2ec6a88d1ecf2f103ead76c2be123383b91000e51f75b718f73c7e1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.18-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:a5c630bdf0a792f2957eba59ab46b0a1ad3221663399a80e742c7358208e6578
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.2 MB (463205386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eddb7576a4decb046eb642333eac99f75bac948bd72a2b587a1132c38967647`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:09:28 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79d7283199af9e4830dbf79ff36b98d8851b342724edd741785b91bad33f7d73 NEO4J_TARBALL=neo4j-enterprise-4.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 07:09:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:49 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 07:10:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:10:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:10:03 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:10:03 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:10:03 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:10:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:10:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9cdbfa885c40f74f375de05f596451f2eb302e89adeb4e35299b8e7ca9c4ed`  
		Last Modified: Thu, 16 Mar 2023 07:11:39 GMT  
		Size: 198.5 MB (198475989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c6a017da58e31f23b2b5533ba126600cc2dc59d99ec83f967e61e178d46907`  
		Last Modified: Thu, 16 Mar 2023 07:11:51 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b24bb5867a0c2cd07294507bcc79f9d5a471409dbef07747c23fc9be32da47`  
		Last Modified: Thu, 16 Mar 2023 07:11:51 GMT  
		Size: 8.4 KB (8426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bacb656612684e64003f420fe3b0622c4318a5ecf15845c180bb0e5224fe2a`  
		Last Modified: Thu, 16 Mar 2023 07:12:02 GMT  
		Size: 233.3 MB (233305708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.18-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1217ece5a6f6ca3c6a144653873c31197ed308a48f237328d2c02c1c16cf2fa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.5 MB (458481619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaba0e5a70f350db609a362ef9f32f7ed40b855041a9914cd7c514f1dd6da6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:50:13 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:12:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79d7283199af9e4830dbf79ff36b98d8851b342724edd741785b91bad33f7d73 NEO4J_TARBALL=neo4j-enterprise-4.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:12:30 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
# Thu, 16 Mar 2023 06:12:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:12:30 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 16 Mar 2023 06:12:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:43 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:44 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:44 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849668ad76f372948228ac47245422eeb38d27a3c72428341214ee297da1d92d`  
		Last Modified: Thu, 16 Mar 2023 05:04:48 GMT  
		Size: 195.2 MB (195242533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fd4923d2bbd76b27c8dffad7e304369264163d19b85e9ee52158e51698fcb9`  
		Last Modified: Thu, 16 Mar 2023 06:14:11 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418ab8174f12a4788a7ae7f81e5bd4e2b66ab371a185d6795286d6c075c5cc7a`  
		Last Modified: Thu, 16 Mar 2023 06:14:11 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef7fc4d0a700eb7ab9cde7f73b1e38118fa4014857953b0b267861df8980da7`  
		Last Modified: Thu, 16 Mar 2023 06:14:20 GMT  
		Size: 233.2 MB (233163962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:986e76ae57e8b107a132997cce59705141b0954afb9e2ebfed3026b5cc412b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:fa9ed6ececd003c4ea80104b4b200150141f34303cff74ee1289988a57e8f30d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f75bff79bbe533a724921207f5c0febacdeae83841e95e8b8ac5830b80e66`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:08:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:08:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:08:41 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:08:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:08:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:08:57 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:08:57 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:08:57 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:08:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:08:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e001ddc63a4f7b55f811d3d54e0f5bebb86d5485219d94c03d9916f4d5617bfe`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c518db23e44a7853b593eec4a067cb1dac9637d76493e511e5f563c9e2b085`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dc49f41a37e67e5f40aeccfb78ee248cefb4943e39cca13d1eb7ddaceab6c`  
		Last Modified: Thu, 16 Mar 2023 07:10:30 GMT  
		Size: 115.2 MB (115196191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0f9405cb24ed3de1a3554f40bb61a37cc0f84a7e2d4e40e0fc2104b5f08d0618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b031cfcc8c1af3547b11f3c4745fd2fed41dd3683b1b15c4149df19e44b6a2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:22 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:11:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:11:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:11:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:11:38 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:11:38 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:11:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:11:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86bd7229f0f47a2be61b3635fcec180a6a1d3dfd604789c381c1fcf5d06f37`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eed4276cd4040efbb08862d97c0ffb49001d8f027aa9bb6783e07db5564e07e`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d0f080131c26aec7aa1c262b3cd21724f8ab31da55b978a6ef058aa483133c`  
		Last Modified: Thu, 16 Mar 2023 06:13:10 GMT  
		Size: 115.1 MB (115051235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:986e76ae57e8b107a132997cce59705141b0954afb9e2ebfed3026b5cc412b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa9ed6ececd003c4ea80104b4b200150141f34303cff74ee1289988a57e8f30d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f75bff79bbe533a724921207f5c0febacdeae83841e95e8b8ac5830b80e66`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:08:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:08:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:08:41 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:08:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:08:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:08:57 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:08:57 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:08:57 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:08:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:08:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e001ddc63a4f7b55f811d3d54e0f5bebb86d5485219d94c03d9916f4d5617bfe`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c518db23e44a7853b593eec4a067cb1dac9637d76493e511e5f563c9e2b085`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dc49f41a37e67e5f40aeccfb78ee248cefb4943e39cca13d1eb7ddaceab6c`  
		Last Modified: Thu, 16 Mar 2023 07:10:30 GMT  
		Size: 115.2 MB (115196191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0f9405cb24ed3de1a3554f40bb61a37cc0f84a7e2d4e40e0fc2104b5f08d0618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b031cfcc8c1af3547b11f3c4745fd2fed41dd3683b1b15c4149df19e44b6a2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:22 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:11:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:11:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:11:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:11:38 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:11:38 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:11:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:11:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86bd7229f0f47a2be61b3635fcec180a6a1d3dfd604789c381c1fcf5d06f37`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eed4276cd4040efbb08862d97c0ffb49001d8f027aa9bb6783e07db5564e07e`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d0f080131c26aec7aa1c262b3cd21724f8ab31da55b978a6ef058aa483133c`  
		Last Modified: Thu, 16 Mar 2023 06:13:10 GMT  
		Size: 115.1 MB (115051235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:22eaf8585a13f194a98fb0c3c2f72c768ecfa407f64b66eecffdd13d6f8f29bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b750d556c7fe46bf7dfe565932b45cedaca08d5dda3b3a3e595b4f8bfd487fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.0 MB (543986295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b70e78aaa852faa9322df16912659d74ca3250c737ebde9ecab3b47a4a19386`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:09:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:04 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:09:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:09:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:09:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:09:20 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:09:21 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:09:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:09:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7faf1cbaba3044a9068d65a3c0498e7c0d66c9bc7e077f1fcbec60e1e7c503c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6cbd2a8118028bb60557929266606feb4ec4e9f26a1fb4ac99cce58c4a366c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e24e0d4bf82b601ff7f0b08e4b72740d466a4d5708817c835aa05195c099e`  
		Last Modified: Thu, 16 Mar 2023 07:11:11 GMT  
		Size: 320.1 MB (320124347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5b9642a46beda383b5c4b2e0cd2e1287ea9d382a1a66348cdc348669d8071bdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.3 MB (541317554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87106aebfd70f8607a883d41014e4acf1a38e41e880c7950669d12c4f06dc044`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:42 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:12:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:05 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:05 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debdc6e583e4d9de905be35df35f7f4e359b68b391bcb09f5996693245fe1276`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884476f2fa28819c14f1cbcecb95388dc5302248c67f2c2b56bb5bc50586bfed`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 8.4 KB (8420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2503db9ba63adcd504c01a50e7dfbe87d3e1822cbbd258e8a631d43ed2c6d908`  
		Last Modified: Thu, 16 Mar 2023 06:13:40 GMT  
		Size: 320.0 MB (319982031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5`

```console
$ docker pull neo4j@sha256:986e76ae57e8b107a132997cce59705141b0954afb9e2ebfed3026b5cc412b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5` - linux; amd64

```console
$ docker pull neo4j@sha256:fa9ed6ececd003c4ea80104b4b200150141f34303cff74ee1289988a57e8f30d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f75bff79bbe533a724921207f5c0febacdeae83841e95e8b8ac5830b80e66`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:08:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:08:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:08:41 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:08:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:08:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:08:57 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:08:57 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:08:57 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:08:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:08:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e001ddc63a4f7b55f811d3d54e0f5bebb86d5485219d94c03d9916f4d5617bfe`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c518db23e44a7853b593eec4a067cb1dac9637d76493e511e5f563c9e2b085`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dc49f41a37e67e5f40aeccfb78ee248cefb4943e39cca13d1eb7ddaceab6c`  
		Last Modified: Thu, 16 Mar 2023 07:10:30 GMT  
		Size: 115.2 MB (115196191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0f9405cb24ed3de1a3554f40bb61a37cc0f84a7e2d4e40e0fc2104b5f08d0618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b031cfcc8c1af3547b11f3c4745fd2fed41dd3683b1b15c4149df19e44b6a2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:22 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:11:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:11:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:11:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:11:38 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:11:38 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:11:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:11:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86bd7229f0f47a2be61b3635fcec180a6a1d3dfd604789c381c1fcf5d06f37`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eed4276cd4040efbb08862d97c0ffb49001d8f027aa9bb6783e07db5564e07e`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d0f080131c26aec7aa1c262b3cd21724f8ab31da55b978a6ef058aa483133c`  
		Last Modified: Thu, 16 Mar 2023 06:13:10 GMT  
		Size: 115.1 MB (115051235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5-enterprise`

```console
$ docker pull neo4j@sha256:22eaf8585a13f194a98fb0c3c2f72c768ecfa407f64b66eecffdd13d6f8f29bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b750d556c7fe46bf7dfe565932b45cedaca08d5dda3b3a3e595b4f8bfd487fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.0 MB (543986295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b70e78aaa852faa9322df16912659d74ca3250c737ebde9ecab3b47a4a19386`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:09:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:04 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:09:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:09:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:09:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:09:20 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:09:21 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:09:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:09:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7faf1cbaba3044a9068d65a3c0498e7c0d66c9bc7e077f1fcbec60e1e7c503c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6cbd2a8118028bb60557929266606feb4ec4e9f26a1fb4ac99cce58c4a366c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e24e0d4bf82b601ff7f0b08e4b72740d466a4d5708817c835aa05195c099e`  
		Last Modified: Thu, 16 Mar 2023 07:11:11 GMT  
		Size: 320.1 MB (320124347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5b9642a46beda383b5c4b2e0cd2e1287ea9d382a1a66348cdc348669d8071bdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.3 MB (541317554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87106aebfd70f8607a883d41014e4acf1a38e41e880c7950669d12c4f06dc044`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:42 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:12:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:05 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:05 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debdc6e583e4d9de905be35df35f7f4e359b68b391bcb09f5996693245fe1276`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884476f2fa28819c14f1cbcecb95388dc5302248c67f2c2b56bb5bc50586bfed`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 8.4 KB (8420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2503db9ba63adcd504c01a50e7dfbe87d3e1822cbbd258e8a631d43ed2c6d908`  
		Last Modified: Thu, 16 Mar 2023 06:13:40 GMT  
		Size: 320.0 MB (319982031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5.0`

```console
$ docker pull neo4j@sha256:986e76ae57e8b107a132997cce59705141b0954afb9e2ebfed3026b5cc412b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5.0` - linux; amd64

```console
$ docker pull neo4j@sha256:fa9ed6ececd003c4ea80104b4b200150141f34303cff74ee1289988a57e8f30d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f75bff79bbe533a724921207f5c0febacdeae83841e95e8b8ac5830b80e66`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:08:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:08:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:08:41 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:08:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:08:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:08:57 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:08:57 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:08:57 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:08:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:08:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e001ddc63a4f7b55f811d3d54e0f5bebb86d5485219d94c03d9916f4d5617bfe`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c518db23e44a7853b593eec4a067cb1dac9637d76493e511e5f563c9e2b085`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dc49f41a37e67e5f40aeccfb78ee248cefb4943e39cca13d1eb7ddaceab6c`  
		Last Modified: Thu, 16 Mar 2023 07:10:30 GMT  
		Size: 115.2 MB (115196191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0f9405cb24ed3de1a3554f40bb61a37cc0f84a7e2d4e40e0fc2104b5f08d0618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b031cfcc8c1af3547b11f3c4745fd2fed41dd3683b1b15c4149df19e44b6a2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:22 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:11:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:11:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:11:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:11:38 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:11:38 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:11:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:11:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86bd7229f0f47a2be61b3635fcec180a6a1d3dfd604789c381c1fcf5d06f37`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eed4276cd4040efbb08862d97c0ffb49001d8f027aa9bb6783e07db5564e07e`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d0f080131c26aec7aa1c262b3cd21724f8ab31da55b978a6ef058aa483133c`  
		Last Modified: Thu, 16 Mar 2023 06:13:10 GMT  
		Size: 115.1 MB (115051235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5.0-community`

```console
$ docker pull neo4j@sha256:986e76ae57e8b107a132997cce59705141b0954afb9e2ebfed3026b5cc412b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa9ed6ececd003c4ea80104b4b200150141f34303cff74ee1289988a57e8f30d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f75bff79bbe533a724921207f5c0febacdeae83841e95e8b8ac5830b80e66`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:08:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:08:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:08:41 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:08:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:08:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:08:57 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:08:57 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:08:57 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:08:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:08:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e001ddc63a4f7b55f811d3d54e0f5bebb86d5485219d94c03d9916f4d5617bfe`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c518db23e44a7853b593eec4a067cb1dac9637d76493e511e5f563c9e2b085`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dc49f41a37e67e5f40aeccfb78ee248cefb4943e39cca13d1eb7ddaceab6c`  
		Last Modified: Thu, 16 Mar 2023 07:10:30 GMT  
		Size: 115.2 MB (115196191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0f9405cb24ed3de1a3554f40bb61a37cc0f84a7e2d4e40e0fc2104b5f08d0618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b031cfcc8c1af3547b11f3c4745fd2fed41dd3683b1b15c4149df19e44b6a2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:22 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:11:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:11:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:11:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:11:38 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:11:38 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:11:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:11:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86bd7229f0f47a2be61b3635fcec180a6a1d3dfd604789c381c1fcf5d06f37`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eed4276cd4040efbb08862d97c0ffb49001d8f027aa9bb6783e07db5564e07e`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d0f080131c26aec7aa1c262b3cd21724f8ab31da55b978a6ef058aa483133c`  
		Last Modified: Thu, 16 Mar 2023 06:13:10 GMT  
		Size: 115.1 MB (115051235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5.0-enterprise`

```console
$ docker pull neo4j@sha256:22eaf8585a13f194a98fb0c3c2f72c768ecfa407f64b66eecffdd13d6f8f29bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b750d556c7fe46bf7dfe565932b45cedaca08d5dda3b3a3e595b4f8bfd487fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.0 MB (543986295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b70e78aaa852faa9322df16912659d74ca3250c737ebde9ecab3b47a4a19386`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:09:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:04 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:09:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:09:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:09:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:09:20 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:09:21 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:09:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:09:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7faf1cbaba3044a9068d65a3c0498e7c0d66c9bc7e077f1fcbec60e1e7c503c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6cbd2a8118028bb60557929266606feb4ec4e9f26a1fb4ac99cce58c4a366c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e24e0d4bf82b601ff7f0b08e4b72740d466a4d5708817c835aa05195c099e`  
		Last Modified: Thu, 16 Mar 2023 07:11:11 GMT  
		Size: 320.1 MB (320124347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5b9642a46beda383b5c4b2e0cd2e1287ea9d382a1a66348cdc348669d8071bdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.3 MB (541317554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87106aebfd70f8607a883d41014e4acf1a38e41e880c7950669d12c4f06dc044`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:42 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:12:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:05 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:05 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debdc6e583e4d9de905be35df35f7f4e359b68b391bcb09f5996693245fe1276`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884476f2fa28819c14f1cbcecb95388dc5302248c67f2c2b56bb5bc50586bfed`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 8.4 KB (8420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2503db9ba63adcd504c01a50e7dfbe87d3e1822cbbd258e8a631d43ed2c6d908`  
		Last Modified: Thu, 16 Mar 2023 06:13:40 GMT  
		Size: 320.0 MB (319982031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:986e76ae57e8b107a132997cce59705141b0954afb9e2ebfed3026b5cc412b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:fa9ed6ececd003c4ea80104b4b200150141f34303cff74ee1289988a57e8f30d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f75bff79bbe533a724921207f5c0febacdeae83841e95e8b8ac5830b80e66`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:08:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:08:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:08:41 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:08:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:08:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:08:57 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:08:57 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:08:57 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:08:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:08:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e001ddc63a4f7b55f811d3d54e0f5bebb86d5485219d94c03d9916f4d5617bfe`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c518db23e44a7853b593eec4a067cb1dac9637d76493e511e5f563c9e2b085`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dc49f41a37e67e5f40aeccfb78ee248cefb4943e39cca13d1eb7ddaceab6c`  
		Last Modified: Thu, 16 Mar 2023 07:10:30 GMT  
		Size: 115.2 MB (115196191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0f9405cb24ed3de1a3554f40bb61a37cc0f84a7e2d4e40e0fc2104b5f08d0618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b031cfcc8c1af3547b11f3c4745fd2fed41dd3683b1b15c4149df19e44b6a2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:22 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:11:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:11:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:11:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:11:38 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:11:38 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:11:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:11:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86bd7229f0f47a2be61b3635fcec180a6a1d3dfd604789c381c1fcf5d06f37`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eed4276cd4040efbb08862d97c0ffb49001d8f027aa9bb6783e07db5564e07e`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d0f080131c26aec7aa1c262b3cd21724f8ab31da55b978a6ef058aa483133c`  
		Last Modified: Thu, 16 Mar 2023 06:13:10 GMT  
		Size: 115.1 MB (115051235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:22eaf8585a13f194a98fb0c3c2f72c768ecfa407f64b66eecffdd13d6f8f29bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b750d556c7fe46bf7dfe565932b45cedaca08d5dda3b3a3e595b4f8bfd487fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.0 MB (543986295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b70e78aaa852faa9322df16912659d74ca3250c737ebde9ecab3b47a4a19386`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:09:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:09:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:09:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:09:04 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:09:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:09:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:09:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:09:20 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:09:21 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:09:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:09:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7faf1cbaba3044a9068d65a3c0498e7c0d66c9bc7e077f1fcbec60e1e7c503c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6cbd2a8118028bb60557929266606feb4ec4e9f26a1fb4ac99cce58c4a366c`  
		Last Modified: Thu, 16 Mar 2023 07:10:58 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e24e0d4bf82b601ff7f0b08e4b72740d466a4d5708817c835aa05195c099e`  
		Last Modified: Thu, 16 Mar 2023 07:11:11 GMT  
		Size: 320.1 MB (320124347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5b9642a46beda383b5c4b2e0cd2e1287ea9d382a1a66348cdc348669d8071bdf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.3 MB (541317554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87106aebfd70f8607a883d41014e4acf1a38e41e880c7950669d12c4f06dc044`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:42 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:12:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:12:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:12:05 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:12:05 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:12:05 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:12:06 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:12:06 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debdc6e583e4d9de905be35df35f7f4e359b68b391bcb09f5996693245fe1276`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884476f2fa28819c14f1cbcecb95388dc5302248c67f2c2b56bb5bc50586bfed`  
		Last Modified: Thu, 16 Mar 2023 06:13:29 GMT  
		Size: 8.4 KB (8420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2503db9ba63adcd504c01a50e7dfbe87d3e1822cbbd258e8a631d43ed2c6d908`  
		Last Modified: Thu, 16 Mar 2023 06:13:40 GMT  
		Size: 320.0 MB (319982031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:986e76ae57e8b107a132997cce59705141b0954afb9e2ebfed3026b5cc412b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:fa9ed6ececd003c4ea80104b4b200150141f34303cff74ee1289988a57e8f30d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81f75bff79bbe533a724921207f5c0febacdeae83841e95e8b8ac5830b80e66`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:08:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 07:08:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 07:08:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 07:08:41 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 07:08:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 07:08:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:08:57 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 07:08:57 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 07:08:57 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 07:08:57 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 07:08:57 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6987daa2231f63e24673f500cc33290b31087d360a4da1759adea5436c5f3100`  
		Last Modified: Thu, 16 Mar 2023 07:10:38 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e001ddc63a4f7b55f811d3d54e0f5bebb86d5485219d94c03d9916f4d5617bfe`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c518db23e44a7853b593eec4a067cb1dac9637d76493e511e5f563c9e2b085`  
		Last Modified: Thu, 16 Mar 2023 07:10:24 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28dc49f41a37e67e5f40aeccfb78ee248cefb4943e39cca13d1eb7ddaceab6c`  
		Last Modified: Thu, 16 Mar 2023 07:10:30 GMT  
		Size: 115.2 MB (115196191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0f9405cb24ed3de1a3554f40bb61a37cc0f84a7e2d4e40e0fc2104b5f08d0618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b031cfcc8c1af3547b11f3c4745fd2fed41dd3683b1b15c4149df19e44b6a2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 06:11:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 16 Mar 2023 06:11:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 16 Mar 2023 06:11:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 16 Mar 2023 06:11:22 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 16 Mar 2023 06:11:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 06:11:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 06:11:38 GMT
WORKDIR /var/lib/neo4j
# Thu, 16 Mar 2023 06:11:38 GMT
VOLUME [/data /logs]
# Thu, 16 Mar 2023 06:11:38 GMT
EXPOSE 7473 7474 7687
# Thu, 16 Mar 2023 06:11:38 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:11:38 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86bd7229f0f47a2be61b3635fcec180a6a1d3dfd604789c381c1fcf5d06f37`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eed4276cd4040efbb08862d97c0ffb49001d8f027aa9bb6783e07db5564e07e`  
		Last Modified: Thu, 16 Mar 2023 06:13:05 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d0f080131c26aec7aa1c262b3cd21724f8ab31da55b978a6ef058aa483133c`  
		Last Modified: Thu, 16 Mar 2023 06:13:10 GMT  
		Size: 115.1 MB (115051235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
