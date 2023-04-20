<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.19`](#neo4j4419)
-	[`neo4j:4.4.19-community`](#neo4j4419-community)
-	[`neo4j:4.4.19-enterprise`](#neo4j4419-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.7`](#neo4j57)
-	[`neo4j:5.7-community`](#neo4j57-community)
-	[`neo4j:5.7-enterprise`](#neo4j57-enterprise)
-	[`neo4j:5.7.0`](#neo4j570)
-	[`neo4j:5.7.0-community`](#neo4j570-community)
-	[`neo4j:5.7.0-enterprise`](#neo4j570-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:c2dfb91ebe161dd6b1674ec887f54243574e07f373480bd330980167a7bdbf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:233e40a451103a4eea525b9f05f1cf7e99c218498e29632f284d8556e4af3912
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349567274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3504dbdfa74967bf5945fdc1b24833d24b466fab830c949e6efc1ea59336ad3e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:14:00 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:28:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:28:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 08:28:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:28:13 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 08:28:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:28:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:28:24 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:28:24 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:28:24 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:28:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:28:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4791db44f1181a51939f7b21de0fda8d67e0a03b6a5393ac49f8d64eadc56`  
		Last Modified: Wed, 12 Apr 2023 08:23:18 GMT  
		Size: 198.5 MB (198475991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5b333302b9ab5809f19218cd380df91f9a27f10b5d28432c248accad3b2e0d`  
		Last Modified: Wed, 12 Apr 2023 08:29:44 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc619c949cadf2a283ec47987f96965d00f0b355e8dd1e3b91e3fd30b582577`  
		Last Modified: Wed, 12 Apr 2023 08:29:44 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306b912272817594d9ba4e4515ff2c94db58be29fb05f62248de4ef615b1db0`  
		Last Modified: Wed, 12 Apr 2023 08:29:49 GMT  
		Size: 119.7 MB (119660626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5cd4a30938ea03d4ccb7da402113e996faf548045ad441344c8c598d2eb5fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344836993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865938353751632763ef13e1ee47f440ee78564b9400c8a09e8f9d5246ff3bf6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:21:10 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:19:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:19:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 04:19:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:19:26 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 04:19:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:36 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:37 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:37 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2a925b22c34d676c0f7dfea6c5e40dae89a2cd334554f1387adb3b0d65cee9`  
		Last Modified: Wed, 12 Apr 2023 01:29:42 GMT  
		Size: 195.2 MB (195242534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f4f0923ceb9a6b28985a53c91321754176486b20e26dbc7de37a4ab5b0b5d6`  
		Last Modified: Wed, 12 Apr 2023 04:20:59 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d9a312c1147b08b3200688361c11243b3c745f4ac478a03bb5ba66dee4bb16`  
		Last Modified: Wed, 12 Apr 2023 04:20:59 GMT  
		Size: 8.6 KB (8564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4022f1ec6edafb91be2d6d1642fb2a29af80e257add97f68193884477bdec250`  
		Last Modified: Wed, 12 Apr 2023 04:21:04 GMT  
		Size: 119.5 MB (119518182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:c2dfb91ebe161dd6b1674ec887f54243574e07f373480bd330980167a7bdbf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:233e40a451103a4eea525b9f05f1cf7e99c218498e29632f284d8556e4af3912
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349567274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3504dbdfa74967bf5945fdc1b24833d24b466fab830c949e6efc1ea59336ad3e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:14:00 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:28:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:28:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 08:28:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:28:13 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 08:28:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:28:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:28:24 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:28:24 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:28:24 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:28:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:28:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4791db44f1181a51939f7b21de0fda8d67e0a03b6a5393ac49f8d64eadc56`  
		Last Modified: Wed, 12 Apr 2023 08:23:18 GMT  
		Size: 198.5 MB (198475991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5b333302b9ab5809f19218cd380df91f9a27f10b5d28432c248accad3b2e0d`  
		Last Modified: Wed, 12 Apr 2023 08:29:44 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc619c949cadf2a283ec47987f96965d00f0b355e8dd1e3b91e3fd30b582577`  
		Last Modified: Wed, 12 Apr 2023 08:29:44 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306b912272817594d9ba4e4515ff2c94db58be29fb05f62248de4ef615b1db0`  
		Last Modified: Wed, 12 Apr 2023 08:29:49 GMT  
		Size: 119.7 MB (119660626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5cd4a30938ea03d4ccb7da402113e996faf548045ad441344c8c598d2eb5fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344836993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865938353751632763ef13e1ee47f440ee78564b9400c8a09e8f9d5246ff3bf6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:21:10 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:19:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:19:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 04:19:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:19:26 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 04:19:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:36 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:37 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:37 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2a925b22c34d676c0f7dfea6c5e40dae89a2cd334554f1387adb3b0d65cee9`  
		Last Modified: Wed, 12 Apr 2023 01:29:42 GMT  
		Size: 195.2 MB (195242534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f4f0923ceb9a6b28985a53c91321754176486b20e26dbc7de37a4ab5b0b5d6`  
		Last Modified: Wed, 12 Apr 2023 04:20:59 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d9a312c1147b08b3200688361c11243b3c745f4ac478a03bb5ba66dee4bb16`  
		Last Modified: Wed, 12 Apr 2023 04:20:59 GMT  
		Size: 8.6 KB (8564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4022f1ec6edafb91be2d6d1642fb2a29af80e257add97f68193884477bdec250`  
		Last Modified: Wed, 12 Apr 2023 04:21:04 GMT  
		Size: 119.5 MB (119518182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:80123d1fce7761a99fa0109f6876c454c900209d33a7fb9373fec1fe0207a6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b22aba3f4da2780f2b8b4775060b2cabe54474bb04c9fe0642dfd762316c0fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.3 MB (446334882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212280b19a45fbb4d43dc735aa85d9d6c00887a343df1e380adc69a72f751d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:14:00 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9ecf2706abff535c4ac9e902ca36257ab23af96be3386ea54f0ec17dcb7cf8e NEO4J_TARBALL=neo4j-enterprise-4.4.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 08:28:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:28:29 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 08:28:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:28:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:28:43 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:28:43 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:28:43 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:28:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:28:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4791db44f1181a51939f7b21de0fda8d67e0a03b6a5393ac49f8d64eadc56`  
		Last Modified: Wed, 12 Apr 2023 08:23:18 GMT  
		Size: 198.5 MB (198475991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a1c32c48cc8b1243a4498a5c9f69ed7d8c7851d0beb170d8eb53724bf7c768`  
		Last Modified: Wed, 12 Apr 2023 08:30:01 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e988b2bb0eefe1fefdbb27f9df55ca19dafbd364a06a1fc4d2cabb69b6984b9a`  
		Last Modified: Wed, 12 Apr 2023 08:30:01 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8975ceb99e32eb8d44924a3d020d3a89c1cc42e17ff9f7c499c05d5e05709ed1`  
		Last Modified: Wed, 12 Apr 2023 08:30:10 GMT  
		Size: 216.4 MB (216428239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4f93208dbcfab14e87ec86def2918a858bc1862c1b56200188e258422f79d38c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.6 MB (441604971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e52bcf7f636a84cd72afb3311c7b6dac17c474687142adbfe0f165e22c0a2ed`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:21:10 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:19:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9ecf2706abff535c4ac9e902ca36257ab23af96be3386ea54f0ec17dcb7cf8e NEO4J_TARBALL=neo4j-enterprise-4.4.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:19:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 04:19:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:19:40 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 04:19:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:59 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:59 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:59 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2a925b22c34d676c0f7dfea6c5e40dae89a2cd334554f1387adb3b0d65cee9`  
		Last Modified: Wed, 12 Apr 2023 01:29:42 GMT  
		Size: 195.2 MB (195242534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bb05aa0bc57ddafcd0544e72a5249b71194450c0ed5c0313d53a5265289a5b`  
		Last Modified: Wed, 12 Apr 2023 04:21:15 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eaec0edabda472a78212330a9a1048a704a6f7ccf77cfdf70ddf1a3b5382d3`  
		Last Modified: Wed, 12 Apr 2023 04:21:15 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d9cb15aaf269aad791dbd64d8c69f932d284df8abf61e52f2f61167845275`  
		Last Modified: Wed, 12 Apr 2023 04:21:24 GMT  
		Size: 216.3 MB (216286159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.19`

```console
$ docker pull neo4j@sha256:c2dfb91ebe161dd6b1674ec887f54243574e07f373480bd330980167a7bdbf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.19` - linux; amd64

```console
$ docker pull neo4j@sha256:233e40a451103a4eea525b9f05f1cf7e99c218498e29632f284d8556e4af3912
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349567274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3504dbdfa74967bf5945fdc1b24833d24b466fab830c949e6efc1ea59336ad3e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:14:00 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:28:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:28:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 08:28:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:28:13 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 08:28:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:28:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:28:24 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:28:24 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:28:24 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:28:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:28:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4791db44f1181a51939f7b21de0fda8d67e0a03b6a5393ac49f8d64eadc56`  
		Last Modified: Wed, 12 Apr 2023 08:23:18 GMT  
		Size: 198.5 MB (198475991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5b333302b9ab5809f19218cd380df91f9a27f10b5d28432c248accad3b2e0d`  
		Last Modified: Wed, 12 Apr 2023 08:29:44 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc619c949cadf2a283ec47987f96965d00f0b355e8dd1e3b91e3fd30b582577`  
		Last Modified: Wed, 12 Apr 2023 08:29:44 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306b912272817594d9ba4e4515ff2c94db58be29fb05f62248de4ef615b1db0`  
		Last Modified: Wed, 12 Apr 2023 08:29:49 GMT  
		Size: 119.7 MB (119660626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.19` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5cd4a30938ea03d4ccb7da402113e996faf548045ad441344c8c598d2eb5fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344836993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865938353751632763ef13e1ee47f440ee78564b9400c8a09e8f9d5246ff3bf6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:21:10 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:19:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:19:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 04:19:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:19:26 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 04:19:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:36 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:37 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:37 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2a925b22c34d676c0f7dfea6c5e40dae89a2cd334554f1387adb3b0d65cee9`  
		Last Modified: Wed, 12 Apr 2023 01:29:42 GMT  
		Size: 195.2 MB (195242534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f4f0923ceb9a6b28985a53c91321754176486b20e26dbc7de37a4ab5b0b5d6`  
		Last Modified: Wed, 12 Apr 2023 04:20:59 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d9a312c1147b08b3200688361c11243b3c745f4ac478a03bb5ba66dee4bb16`  
		Last Modified: Wed, 12 Apr 2023 04:20:59 GMT  
		Size: 8.6 KB (8564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4022f1ec6edafb91be2d6d1642fb2a29af80e257add97f68193884477bdec250`  
		Last Modified: Wed, 12 Apr 2023 04:21:04 GMT  
		Size: 119.5 MB (119518182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.19-community`

```console
$ docker pull neo4j@sha256:c2dfb91ebe161dd6b1674ec887f54243574e07f373480bd330980167a7bdbf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.19-community` - linux; amd64

```console
$ docker pull neo4j@sha256:233e40a451103a4eea525b9f05f1cf7e99c218498e29632f284d8556e4af3912
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.6 MB (349567274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3504dbdfa74967bf5945fdc1b24833d24b466fab830c949e6efc1ea59336ad3e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:14:00 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:28:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:28:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 08:28:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:28:13 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 08:28:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:28:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:28:24 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:28:24 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:28:24 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:28:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:28:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4791db44f1181a51939f7b21de0fda8d67e0a03b6a5393ac49f8d64eadc56`  
		Last Modified: Wed, 12 Apr 2023 08:23:18 GMT  
		Size: 198.5 MB (198475991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5b333302b9ab5809f19218cd380df91f9a27f10b5d28432c248accad3b2e0d`  
		Last Modified: Wed, 12 Apr 2023 08:29:44 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc619c949cadf2a283ec47987f96965d00f0b355e8dd1e3b91e3fd30b582577`  
		Last Modified: Wed, 12 Apr 2023 08:29:44 GMT  
		Size: 8.6 KB (8571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b306b912272817594d9ba4e4515ff2c94db58be29fb05f62248de4ef615b1db0`  
		Last Modified: Wed, 12 Apr 2023 08:29:49 GMT  
		Size: 119.7 MB (119660626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.19-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5cd4a30938ea03d4ccb7da402113e996faf548045ad441344c8c598d2eb5fec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344836993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865938353751632763ef13e1ee47f440ee78564b9400c8a09e8f9d5246ff3bf6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:21:10 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:19:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e101ff8ad46b1244223fefb2508e4d83c40a717028e004aba66b9cc70945cecb NEO4J_TARBALL=neo4j-community-4.4.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:19:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 04:19:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:19:26 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 04:19:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:36 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:37 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:37 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2a925b22c34d676c0f7dfea6c5e40dae89a2cd334554f1387adb3b0d65cee9`  
		Last Modified: Wed, 12 Apr 2023 01:29:42 GMT  
		Size: 195.2 MB (195242534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f4f0923ceb9a6b28985a53c91321754176486b20e26dbc7de37a4ab5b0b5d6`  
		Last Modified: Wed, 12 Apr 2023 04:20:59 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d9a312c1147b08b3200688361c11243b3c745f4ac478a03bb5ba66dee4bb16`  
		Last Modified: Wed, 12 Apr 2023 04:20:59 GMT  
		Size: 8.6 KB (8564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4022f1ec6edafb91be2d6d1642fb2a29af80e257add97f68193884477bdec250`  
		Last Modified: Wed, 12 Apr 2023 04:21:04 GMT  
		Size: 119.5 MB (119518182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.19-enterprise`

```console
$ docker pull neo4j@sha256:80123d1fce7761a99fa0109f6876c454c900209d33a7fb9373fec1fe0207a6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.19-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8b22aba3f4da2780f2b8b4775060b2cabe54474bb04c9fe0642dfd762316c0fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.3 MB (446334882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d212280b19a45fbb4d43dc735aa85d9d6c00887a343df1e380adc69a72f751d7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:14:00 GMT
COPY dir:e649a995635d4b28f1458e8ccc09f5f71440b52479cfda5ea11e99ab14d0ce82 in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9ecf2706abff535c4ac9e902ca36257ab23af96be3386ea54f0ec17dcb7cf8e NEO4J_TARBALL=neo4j-enterprise-4.4.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 08:28:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:28:29 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 08:28:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:28:42 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:28:43 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:28:43 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:28:43 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:28:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:28:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa4791db44f1181a51939f7b21de0fda8d67e0a03b6a5393ac49f8d64eadc56`  
		Last Modified: Wed, 12 Apr 2023 08:23:18 GMT  
		Size: 198.5 MB (198475991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a1c32c48cc8b1243a4498a5c9f69ed7d8c7851d0beb170d8eb53724bf7c768`  
		Last Modified: Wed, 12 Apr 2023 08:30:01 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e988b2bb0eefe1fefdbb27f9df55ca19dafbd364a06a1fc4d2cabb69b6984b9a`  
		Last Modified: Wed, 12 Apr 2023 08:30:01 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8975ceb99e32eb8d44924a3d020d3a89c1cc42e17ff9f7c499c05d5e05709ed1`  
		Last Modified: Wed, 12 Apr 2023 08:30:10 GMT  
		Size: 216.4 MB (216428239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.19-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4f93208dbcfab14e87ec86def2918a858bc1862c1b56200188e258422f79d38c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.6 MB (441604971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e52bcf7f636a84cd72afb3311c7b6dac17c474687142adbfe0f165e22c0a2ed`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:21:10 GMT
COPY dir:d446509417048b798354227404c222c2c6031477a91cb1b64eded33f5e598adf in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:19:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=e9ecf2706abff535c4ac9e902ca36257ab23af96be3386ea54f0ec17dcb7cf8e NEO4J_TARBALL=neo4j-enterprise-4.4.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:19:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
# Wed, 12 Apr 2023 04:19:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:19:40 GMT
COPY multi:aaaef3312b424e9587435ac8f800bbbd3d3459429e38edf4429492cb6a753a4b in /startup/ 
# Wed, 12 Apr 2023 04:19:57 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:59 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:59 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:59 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:59 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:59 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2a925b22c34d676c0f7dfea6c5e40dae89a2cd334554f1387adb3b0d65cee9`  
		Last Modified: Wed, 12 Apr 2023 01:29:42 GMT  
		Size: 195.2 MB (195242534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bb05aa0bc57ddafcd0544e72a5249b71194450c0ed5c0313d53a5265289a5b`  
		Last Modified: Wed, 12 Apr 2023 04:21:15 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0eaec0edabda472a78212330a9a1048a704a6f7ccf77cfdf70ddf1a3b5382d3`  
		Last Modified: Wed, 12 Apr 2023 04:21:15 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33d9cb15aaf269aad791dbd64d8c69f932d284df8abf61e52f2f61167845275`  
		Last Modified: Wed, 12 Apr 2023 04:21:24 GMT  
		Size: 216.3 MB (216286159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:b817478d92e2bc20dba98742f40927c8988ec0a090be38cc096ba6222bd16041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:0a8ed3602875ffe0807e0e4046663763ec481a260e12ada91b3fcbd23dec0e89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339542637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2bbb766df78905a61eb61755bcadc15acb4ae15280029d78410afdc74acec8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:16:43 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:27:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:27:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 08:27:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:27:37 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 08:27:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:27:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:27:48 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:27:48 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:27:48 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:27:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:27:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddd9ea3ca0dd85f3af3e4aaaa2acdd08b9f289fab659372eedc7fd033de543c`  
		Last Modified: Wed, 12 Apr 2023 08:24:58 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2468aaaf0a78abc2d5737b5b48245f7d54294ae4dabd1b4e6e3bb3d5ee24a0a`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa783c941a481477b08af1f779e1909cdb32dda1fd6d257bb32e7157f8388963`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 8.6 KB (8627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081b9e3f57b27f4f7d7cd842c6abaf737f0ee52f50d3b2fda0c7097c70762436`  
		Last Modified: Wed, 12 Apr 2023 08:29:01 GMT  
		Size: 115.7 MB (115673660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b338729acc57a8b23e3f07dde6ee307fea7bc848c5c85c3ef35c7c03fa2a10ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336868264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a478ab5d3a4dd7a7b0bc781f8c3ef96e4b8799ade7c896bf2a003d2f589e44f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:23:36 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 04:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 04:19:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:05 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:05 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:05 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9701f65253cb8cdaa00fd933b855a5c7977f66e7e7b1e8cfa93ad00f587f6479`  
		Last Modified: Wed, 12 Apr 2023 01:31:17 GMT  
		Size: 191.3 MB (191260431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35efb11ab5fe742be81e3c2049cb3053ff82a73d15963bbd20c405948c1338e7`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701ed5e8b2fbc8c1b8d5c7b7b8a70d83a750d2e30b318198f675edccd62024a8`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 8.6 KB (8631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ca08505b7f879ec6594895fc709ae06d279848756db5c3ea85dc7ff90b6bf3`  
		Last Modified: Wed, 12 Apr 2023 04:20:18 GMT  
		Size: 115.5 MB (115531491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:b817478d92e2bc20dba98742f40927c8988ec0a090be38cc096ba6222bd16041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:0a8ed3602875ffe0807e0e4046663763ec481a260e12ada91b3fcbd23dec0e89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339542637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2bbb766df78905a61eb61755bcadc15acb4ae15280029d78410afdc74acec8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:16:43 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:27:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:27:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 08:27:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:27:37 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 08:27:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:27:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:27:48 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:27:48 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:27:48 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:27:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:27:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddd9ea3ca0dd85f3af3e4aaaa2acdd08b9f289fab659372eedc7fd033de543c`  
		Last Modified: Wed, 12 Apr 2023 08:24:58 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2468aaaf0a78abc2d5737b5b48245f7d54294ae4dabd1b4e6e3bb3d5ee24a0a`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa783c941a481477b08af1f779e1909cdb32dda1fd6d257bb32e7157f8388963`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 8.6 KB (8627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081b9e3f57b27f4f7d7cd842c6abaf737f0ee52f50d3b2fda0c7097c70762436`  
		Last Modified: Wed, 12 Apr 2023 08:29:01 GMT  
		Size: 115.7 MB (115673660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b338729acc57a8b23e3f07dde6ee307fea7bc848c5c85c3ef35c7c03fa2a10ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336868264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a478ab5d3a4dd7a7b0bc781f8c3ef96e4b8799ade7c896bf2a003d2f589e44f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:23:36 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 04:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 04:19:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:05 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:05 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:05 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9701f65253cb8cdaa00fd933b855a5c7977f66e7e7b1e8cfa93ad00f587f6479`  
		Last Modified: Wed, 12 Apr 2023 01:31:17 GMT  
		Size: 191.3 MB (191260431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35efb11ab5fe742be81e3c2049cb3053ff82a73d15963bbd20c405948c1338e7`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701ed5e8b2fbc8c1b8d5c7b7b8a70d83a750d2e30b318198f675edccd62024a8`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 8.6 KB (8631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ca08505b7f879ec6594895fc709ae06d279848756db5c3ea85dc7ff90b6bf3`  
		Last Modified: Wed, 12 Apr 2023 04:20:18 GMT  
		Size: 115.5 MB (115531491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:0b8f947ce651be74dc8613c5c9f4edbd1d04310fd7f737e20f38d9d0ae0426c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:08be0893e00d10b1eabd4b16e26280ab22a94b74e2fe266bfe726a10d67e2298
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.3 MB (545312341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7c741779fed4a86bf281b0aa6be5217dfbd1ea2c6d5533052d2ea821cb685f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:16:43 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:27:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=01eebdd9a24ea10ab3c863bb11d59faa4d732f84801ff755f1d2d5aad27fad9b NEO4J_TARBALL=neo4j-enterprise-5.6.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:27:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 08:27:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:27:53 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 08:28:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:28:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:28:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:28:09 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:28:09 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:28:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:28:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddd9ea3ca0dd85f3af3e4aaaa2acdd08b9f289fab659372eedc7fd033de543c`  
		Last Modified: Wed, 12 Apr 2023 08:24:58 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ba353dd33b417b16c9ee28d064180e5805672bb318ca7d2da4a36d63f76000`  
		Last Modified: Wed, 12 Apr 2023 08:29:19 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9330a93ec249c5ab808decad64a952117b0b08bf16679c331375321792c4f05f`  
		Last Modified: Wed, 12 Apr 2023 08:29:19 GMT  
		Size: 8.6 KB (8628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f962db00d3ffb908794955ffe7614da3b1b44d72be42c84f9b20b269a1508754`  
		Last Modified: Wed, 12 Apr 2023 08:29:32 GMT  
		Size: 321.4 MB (321443364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5fc0e1854168eb93f03b1a108da62763e90a05107e1dcc0bda28e0c48ba2ed8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542638994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a4a8b6f6b68d96d0f1b14c43828a528712e6481d69c4ab99d92496519262f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:23:36 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=01eebdd9a24ea10ab3c863bb11d59faa4d732f84801ff755f1d2d5aad27fad9b NEO4J_TARBALL=neo4j-enterprise-5.6.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:19:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 04:19:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:19:07 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 04:19:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:22 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:22 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:22 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9701f65253cb8cdaa00fd933b855a5c7977f66e7e7b1e8cfa93ad00f587f6479`  
		Last Modified: Wed, 12 Apr 2023 01:31:17 GMT  
		Size: 191.3 MB (191260431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de12bc1df98f159ab33d071b56655c86bfc8c8d9ede3ee85c1f195ff28b26e7e`  
		Last Modified: Wed, 12 Apr 2023 04:20:36 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db664e3750fbd8f01cdaf8ac577e9ea85b17e7624f8ddb845d674371c39187aa`  
		Last Modified: Wed, 12 Apr 2023 04:20:36 GMT  
		Size: 8.6 KB (8629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f68a226caa4b17658883e16605bc2a59ace1f6d4d64f1b55c5a257d8e78cce`  
		Last Modified: Wed, 12 Apr 2023 04:20:47 GMT  
		Size: 321.3 MB (321302226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.7`

**does not exist** (yet?)

## `neo4j:5.7-community`

**does not exist** (yet?)

## `neo4j:5.7-enterprise`

**does not exist** (yet?)

## `neo4j:5.7.0`

**does not exist** (yet?)

## `neo4j:5.7.0-community`

**does not exist** (yet?)

## `neo4j:5.7.0-enterprise`

**does not exist** (yet?)

## `neo4j:community`

```console
$ docker pull neo4j@sha256:b817478d92e2bc20dba98742f40927c8988ec0a090be38cc096ba6222bd16041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:0a8ed3602875ffe0807e0e4046663763ec481a260e12ada91b3fcbd23dec0e89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339542637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2bbb766df78905a61eb61755bcadc15acb4ae15280029d78410afdc74acec8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:16:43 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:27:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:27:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 08:27:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:27:37 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 08:27:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:27:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:27:48 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:27:48 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:27:48 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:27:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:27:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddd9ea3ca0dd85f3af3e4aaaa2acdd08b9f289fab659372eedc7fd033de543c`  
		Last Modified: Wed, 12 Apr 2023 08:24:58 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2468aaaf0a78abc2d5737b5b48245f7d54294ae4dabd1b4e6e3bb3d5ee24a0a`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa783c941a481477b08af1f779e1909cdb32dda1fd6d257bb32e7157f8388963`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 8.6 KB (8627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081b9e3f57b27f4f7d7cd842c6abaf737f0ee52f50d3b2fda0c7097c70762436`  
		Last Modified: Wed, 12 Apr 2023 08:29:01 GMT  
		Size: 115.7 MB (115673660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b338729acc57a8b23e3f07dde6ee307fea7bc848c5c85c3ef35c7c03fa2a10ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336868264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a478ab5d3a4dd7a7b0bc781f8c3ef96e4b8799ade7c896bf2a003d2f589e44f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:23:36 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 04:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 04:19:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:05 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:05 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:05 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9701f65253cb8cdaa00fd933b855a5c7977f66e7e7b1e8cfa93ad00f587f6479`  
		Last Modified: Wed, 12 Apr 2023 01:31:17 GMT  
		Size: 191.3 MB (191260431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35efb11ab5fe742be81e3c2049cb3053ff82a73d15963bbd20c405948c1338e7`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701ed5e8b2fbc8c1b8d5c7b7b8a70d83a750d2e30b318198f675edccd62024a8`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 8.6 KB (8631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ca08505b7f879ec6594895fc709ae06d279848756db5c3ea85dc7ff90b6bf3`  
		Last Modified: Wed, 12 Apr 2023 04:20:18 GMT  
		Size: 115.5 MB (115531491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:0b8f947ce651be74dc8613c5c9f4edbd1d04310fd7f737e20f38d9d0ae0426c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:08be0893e00d10b1eabd4b16e26280ab22a94b74e2fe266bfe726a10d67e2298
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **545.3 MB (545312341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7c741779fed4a86bf281b0aa6be5217dfbd1ea2c6d5533052d2ea821cb685f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:16:43 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:27:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=01eebdd9a24ea10ab3c863bb11d59faa4d732f84801ff755f1d2d5aad27fad9b NEO4J_TARBALL=neo4j-enterprise-5.6.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:27:52 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 08:27:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:27:53 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 08:28:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:28:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:28:09 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:28:09 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:28:09 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:28:09 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:28:09 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddd9ea3ca0dd85f3af3e4aaaa2acdd08b9f289fab659372eedc7fd033de543c`  
		Last Modified: Wed, 12 Apr 2023 08:24:58 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ba353dd33b417b16c9ee28d064180e5805672bb318ca7d2da4a36d63f76000`  
		Last Modified: Wed, 12 Apr 2023 08:29:19 GMT  
		Size: 3.9 KB (3857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9330a93ec249c5ab808decad64a952117b0b08bf16679c331375321792c4f05f`  
		Last Modified: Wed, 12 Apr 2023 08:29:19 GMT  
		Size: 8.6 KB (8628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f962db00d3ffb908794955ffe7614da3b1b44d72be42c84f9b20b269a1508754`  
		Last Modified: Wed, 12 Apr 2023 08:29:32 GMT  
		Size: 321.4 MB (321443364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5fc0e1854168eb93f03b1a108da62763e90a05107e1dcc0bda28e0c48ba2ed8d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.6 MB (542638994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a4a8b6f6b68d96d0f1b14c43828a528712e6481d69c4ab99d92496519262f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:23:36 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=01eebdd9a24ea10ab3c863bb11d59faa4d732f84801ff755f1d2d5aad27fad9b NEO4J_TARBALL=neo4j-enterprise-5.6.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:19:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 04:19:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:19:07 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 04:19:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:22 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:22 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:22 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:22 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:22 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:22 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9701f65253cb8cdaa00fd933b855a5c7977f66e7e7b1e8cfa93ad00f587f6479`  
		Last Modified: Wed, 12 Apr 2023 01:31:17 GMT  
		Size: 191.3 MB (191260431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de12bc1df98f159ab33d071b56655c86bfc8c8d9ede3ee85c1f195ff28b26e7e`  
		Last Modified: Wed, 12 Apr 2023 04:20:36 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db664e3750fbd8f01cdaf8ac577e9ea85b17e7624f8ddb845d674371c39187aa`  
		Last Modified: Wed, 12 Apr 2023 04:20:36 GMT  
		Size: 8.6 KB (8629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f68a226caa4b17658883e16605bc2a59ace1f6d4d64f1b55c5a257d8e78cce`  
		Last Modified: Wed, 12 Apr 2023 04:20:47 GMT  
		Size: 321.3 MB (321302226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:b817478d92e2bc20dba98742f40927c8988ec0a090be38cc096ba6222bd16041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:0a8ed3602875ffe0807e0e4046663763ec481a260e12ada91b3fcbd23dec0e89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339542637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2bbb766df78905a61eb61755bcadc15acb4ae15280029d78410afdc74acec8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 08:16:43 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Wed, 12 Apr 2023 08:27:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 08:27:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 08:27:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 08:27:37 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 08:27:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:27:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 08:27:48 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 08:27:48 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 08:27:48 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 08:27:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:27:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddd9ea3ca0dd85f3af3e4aaaa2acdd08b9f289fab659372eedc7fd033de543c`  
		Last Modified: Wed, 12 Apr 2023 08:24:58 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2468aaaf0a78abc2d5737b5b48245f7d54294ae4dabd1b4e6e3bb3d5ee24a0a`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa783c941a481477b08af1f779e1909cdb32dda1fd6d257bb32e7157f8388963`  
		Last Modified: Wed, 12 Apr 2023 08:28:56 GMT  
		Size: 8.6 KB (8627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081b9e3f57b27f4f7d7cd842c6abaf737f0ee52f50d3b2fda0c7097c70762436`  
		Last Modified: Wed, 12 Apr 2023 08:29:01 GMT  
		Size: 115.7 MB (115673660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b338729acc57a8b23e3f07dde6ee307fea7bc848c5c85c3ef35c7c03fa2a10ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336868264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a478ab5d3a4dd7a7b0bc781f8c3ef96e4b8799ade7c896bf2a003d2f589e44f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:23:36 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Wed, 12 Apr 2023 04:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=16cc236a08fd99acea9b08dc9b19c016dc693bb97fa4f4ca81c2c90cf9452292 NEO4J_TARBALL=neo4j-community-5.6.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
# Wed, 12 Apr 2023 04:18:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 12 Apr 2023 04:18:48 GMT
COPY multi:a0d7d5f1f7f5a76cb0c8925dfafbe8943f9d1b1a76afc1b0ac964f6eb93156be in /startup/ 
# Wed, 12 Apr 2023 04:19:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.6.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 04:19:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 04:19:05 GMT
WORKDIR /var/lib/neo4j
# Wed, 12 Apr 2023 04:19:05 GMT
VOLUME [/data /logs]
# Wed, 12 Apr 2023 04:19:05 GMT
EXPOSE 7473 7474 7687
# Wed, 12 Apr 2023 04:19:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 04:19:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9701f65253cb8cdaa00fd933b855a5c7977f66e7e7b1e8cfa93ad00f587f6479`  
		Last Modified: Wed, 12 Apr 2023 01:31:17 GMT  
		Size: 191.3 MB (191260431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35efb11ab5fe742be81e3c2049cb3053ff82a73d15963bbd20c405948c1338e7`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701ed5e8b2fbc8c1b8d5c7b7b8a70d83a750d2e30b318198f675edccd62024a8`  
		Last Modified: Wed, 12 Apr 2023 04:20:13 GMT  
		Size: 8.6 KB (8631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ca08505b7f879ec6594895fc709ae06d279848756db5c3ea85dc7ff90b6bf3`  
		Last Modified: Wed, 12 Apr 2023 04:20:18 GMT  
		Size: 115.5 MB (115531491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
