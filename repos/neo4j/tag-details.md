<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.3`](#neo4j43)
-	[`neo4j:4.3-community`](#neo4j43-community)
-	[`neo4j:4.3-enterprise`](#neo4j43-enterprise)
-	[`neo4j:4.3.19`](#neo4j4319)
-	[`neo4j:4.3.19-community`](#neo4j4319-community)
-	[`neo4j:4.3.19-enterprise`](#neo4j4319-enterprise)
-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.12`](#neo4j4412)
-	[`neo4j:4.4.12-community`](#neo4j4412-community)
-	[`neo4j:4.4.12-enterprise`](#neo4j4412-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.1.0`](#neo4j510)
-	[`neo4j:5.1.0-community`](#neo4j510-community)
-	[`neo4j:5.1.0-enterprise`](#neo4j510-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.3`

```console
$ docker pull neo4j@sha256:2df7930499a77ebdf904a5442bf453eeebf6c2e62e7135ff3beea1f1e721a91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3` - linux; amd64

```console
$ docker pull neo4j@sha256:f5ecb2bdce172235ebb2967c66c49aaf776b9cfc9366c17e80d7a0c02947fbc3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360165761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4069c7d1b752f5d8c5b6178796c6dc5a7992a6982a09465d68bc02e80cfceb76`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=55e4dec03a4424933d753387913a38ac2a6100dbfbb1cd976b3958fb8489e3a7 NEO4J_TARBALL=neo4j-community-4.3.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
# Sat, 05 Nov 2022 00:29:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:47 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Sat, 05 Nov 2022 00:30:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:30:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:30:04 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:30:04 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:30:04 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:30:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:30:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214d0fb02690545b41c6690a6e5022fc496cbf2048365b83d666775bb799f209`  
		Last Modified: Sat, 05 Nov 2022 00:31:52 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bccce9ff73601ba7a3ac4d370685ab3748553ee04e2597264668a7c9337cfa`  
		Last Modified: Sat, 05 Nov 2022 00:31:52 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b251d6fb5bbee09775152ca5b3bd4af0a7a0e2154bbdca7f2f24ccbc0c0ed046`  
		Last Modified: Sat, 05 Nov 2022 00:31:59 GMT  
		Size: 130.3 MB (130278394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-community`

```console
$ docker pull neo4j@sha256:2df7930499a77ebdf904a5442bf453eeebf6c2e62e7135ff3beea1f1e721a91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-community` - linux; amd64

```console
$ docker pull neo4j@sha256:f5ecb2bdce172235ebb2967c66c49aaf776b9cfc9366c17e80d7a0c02947fbc3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360165761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4069c7d1b752f5d8c5b6178796c6dc5a7992a6982a09465d68bc02e80cfceb76`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=55e4dec03a4424933d753387913a38ac2a6100dbfbb1cd976b3958fb8489e3a7 NEO4J_TARBALL=neo4j-community-4.3.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
# Sat, 05 Nov 2022 00:29:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:47 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Sat, 05 Nov 2022 00:30:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:30:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:30:04 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:30:04 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:30:04 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:30:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:30:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214d0fb02690545b41c6690a6e5022fc496cbf2048365b83d666775bb799f209`  
		Last Modified: Sat, 05 Nov 2022 00:31:52 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bccce9ff73601ba7a3ac4d370685ab3748553ee04e2597264668a7c9337cfa`  
		Last Modified: Sat, 05 Nov 2022 00:31:52 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b251d6fb5bbee09775152ca5b3bd4af0a7a0e2154bbdca7f2f24ccbc0c0ed046`  
		Last Modified: Sat, 05 Nov 2022 00:31:59 GMT  
		Size: 130.3 MB (130278394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-enterprise`

```console
$ docker pull neo4j@sha256:2786fa0d93b2b6a3e836c7b1e887143fa827e0af99428c7df85a618390d32696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7a70908c98e36908dc8562a9efbaad00ab587b876fd82d354f93e88a39a808f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 MB (390649617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e959e5b26cc1917857e751a3ee3a212340dc97c6b20910e1bfc474e119078d88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:30:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4f574dc264853263b865d9c696b389c6dd3e4c9bf7adb84d2f6ac87f907a561c NEO4J_TARBALL=neo4j-enterprise-4.3.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:30:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
# Sat, 05 Nov 2022 00:30:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:30:11 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Sat, 05 Nov 2022 00:30:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:30:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:30:29 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:30:30 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:30:30 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:30:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:30:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d79c5b827e4f8f481cf777bc74bef90d8dacbae1776d5d8a59e6b07d39a2717`  
		Last Modified: Sat, 05 Nov 2022 00:32:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f63dd1a4f6a20fc4f60a721e16caac18d1d7a45adabb550ce193f58c54c91d`  
		Last Modified: Sat, 05 Nov 2022 00:32:13 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc5e0e0b78e5f4eb82ea7ec6fbd500250b89bb99cae21f0a96e1db195095ab8`  
		Last Modified: Sat, 05 Nov 2022 00:32:21 GMT  
		Size: 160.8 MB (160762247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.19`

```console
$ docker pull neo4j@sha256:2df7930499a77ebdf904a5442bf453eeebf6c2e62e7135ff3beea1f1e721a91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.19` - linux; amd64

```console
$ docker pull neo4j@sha256:f5ecb2bdce172235ebb2967c66c49aaf776b9cfc9366c17e80d7a0c02947fbc3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360165761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4069c7d1b752f5d8c5b6178796c6dc5a7992a6982a09465d68bc02e80cfceb76`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=55e4dec03a4424933d753387913a38ac2a6100dbfbb1cd976b3958fb8489e3a7 NEO4J_TARBALL=neo4j-community-4.3.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
# Sat, 05 Nov 2022 00:29:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:47 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Sat, 05 Nov 2022 00:30:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:30:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:30:04 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:30:04 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:30:04 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:30:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:30:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214d0fb02690545b41c6690a6e5022fc496cbf2048365b83d666775bb799f209`  
		Last Modified: Sat, 05 Nov 2022 00:31:52 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bccce9ff73601ba7a3ac4d370685ab3748553ee04e2597264668a7c9337cfa`  
		Last Modified: Sat, 05 Nov 2022 00:31:52 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b251d6fb5bbee09775152ca5b3bd4af0a7a0e2154bbdca7f2f24ccbc0c0ed046`  
		Last Modified: Sat, 05 Nov 2022 00:31:59 GMT  
		Size: 130.3 MB (130278394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.19-community`

```console
$ docker pull neo4j@sha256:2df7930499a77ebdf904a5442bf453eeebf6c2e62e7135ff3beea1f1e721a91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.19-community` - linux; amd64

```console
$ docker pull neo4j@sha256:f5ecb2bdce172235ebb2967c66c49aaf776b9cfc9366c17e80d7a0c02947fbc3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.2 MB (360165761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4069c7d1b752f5d8c5b6178796c6dc5a7992a6982a09465d68bc02e80cfceb76`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=55e4dec03a4424933d753387913a38ac2a6100dbfbb1cd976b3958fb8489e3a7 NEO4J_TARBALL=neo4j-community-4.3.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
# Sat, 05 Nov 2022 00:29:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:47 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Sat, 05 Nov 2022 00:30:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:30:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:30:04 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:30:04 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:30:04 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:30:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:30:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214d0fb02690545b41c6690a6e5022fc496cbf2048365b83d666775bb799f209`  
		Last Modified: Sat, 05 Nov 2022 00:31:52 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bccce9ff73601ba7a3ac4d370685ab3748553ee04e2597264668a7c9337cfa`  
		Last Modified: Sat, 05 Nov 2022 00:31:52 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b251d6fb5bbee09775152ca5b3bd4af0a7a0e2154bbdca7f2f24ccbc0c0ed046`  
		Last Modified: Sat, 05 Nov 2022 00:31:59 GMT  
		Size: 130.3 MB (130278394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.19-enterprise`

```console
$ docker pull neo4j@sha256:2786fa0d93b2b6a3e836c7b1e887143fa827e0af99428c7df85a618390d32696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.19-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7a70908c98e36908dc8562a9efbaad00ab587b876fd82d354f93e88a39a808f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 MB (390649617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e959e5b26cc1917857e751a3ee3a212340dc97c6b20910e1bfc474e119078d88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:30:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4f574dc264853263b865d9c696b389c6dd3e4c9bf7adb84d2f6ac87f907a561c NEO4J_TARBALL=neo4j-enterprise-4.3.19-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:30:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
# Sat, 05 Nov 2022 00:30:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:30:11 GMT
COPY multi:3b4704be041416e3fa83bc67a4b7f99c008afd7bda5553bae3b5e35844061a0a in /startup/ 
# Sat, 05 Nov 2022 00:30:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.19-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:30:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:30:29 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:30:30 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:30:30 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:30:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:30:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d79c5b827e4f8f481cf777bc74bef90d8dacbae1776d5d8a59e6b07d39a2717`  
		Last Modified: Sat, 05 Nov 2022 00:32:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f63dd1a4f6a20fc4f60a721e16caac18d1d7a45adabb550ce193f58c54c91d`  
		Last Modified: Sat, 05 Nov 2022 00:32:13 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc5e0e0b78e5f4eb82ea7ec6fbd500250b89bb99cae21f0a96e1db195095ab8`  
		Last Modified: Sat, 05 Nov 2022 00:32:21 GMT  
		Size: 160.8 MB (160762247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:bf3663e426274ab4a7c9df85208683aa8d57e527aef426ba59c5e95db7334ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:2dc174bb2f7d231ba332d83e8a92d805009f8d4d956a6f3fd7d5adfbb74ae6e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.0 MB (365033761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6836fda89e932c5b2bb82d9189c3c613244cc65332d598dd318ac899792f4f4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:29:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:08 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:29:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:29:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:29:21 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:29:21 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:29:21 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:29:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:29:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90050ec34ac0011d80656d8be239105a2b3ecb3bad879ee21850eb8680c404d7`  
		Last Modified: Sat, 05 Nov 2022 00:31:01 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a40fb45dc90f9b7d53ac018f9694e4cc68644d8226056d4f7c6cff44827dce`  
		Last Modified: Sat, 05 Nov 2022 00:31:01 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584ccb6f6ca3f9eae474080c63992c142a9e4e46e754d737235f18054ab6da2b`  
		Last Modified: Sat, 05 Nov 2022 00:31:08 GMT  
		Size: 135.1 MB (135146406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2cffca40f23efc2ec52409559f7541adb0b7cd118c7cc4453e681548f99e5fa8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360280836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb597751f143cae7120d19deaaf0b38d84adec376fa0b6af1490740866e49a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:21:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:21:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:21:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:21:49 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:22:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:22:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:22:05 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:22:05 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:22:05 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:22:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:22:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a68633cb697b6c1b8ed77d6dbafd3f42712fe46e35d42049b8dbeb6e8ee5a9`  
		Last Modified: Sat, 05 Nov 2022 00:22:55 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcebb94154f7acf8c17539ddd712579de1285aafa21bcba39223b53170b519c0`  
		Last Modified: Sat, 05 Nov 2022 00:22:55 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103006b9193a4939adc0b2b9e9bc03a58b651b4e599aeee34624f483d8aa8125`  
		Last Modified: Sat, 05 Nov 2022 00:23:01 GMT  
		Size: 135.0 MB (135004338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:bf3663e426274ab4a7c9df85208683aa8d57e527aef426ba59c5e95db7334ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2dc174bb2f7d231ba332d83e8a92d805009f8d4d956a6f3fd7d5adfbb74ae6e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.0 MB (365033761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6836fda89e932c5b2bb82d9189c3c613244cc65332d598dd318ac899792f4f4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:29:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:08 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:29:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:29:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:29:21 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:29:21 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:29:21 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:29:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:29:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90050ec34ac0011d80656d8be239105a2b3ecb3bad879ee21850eb8680c404d7`  
		Last Modified: Sat, 05 Nov 2022 00:31:01 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a40fb45dc90f9b7d53ac018f9694e4cc68644d8226056d4f7c6cff44827dce`  
		Last Modified: Sat, 05 Nov 2022 00:31:01 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584ccb6f6ca3f9eae474080c63992c142a9e4e46e754d737235f18054ab6da2b`  
		Last Modified: Sat, 05 Nov 2022 00:31:08 GMT  
		Size: 135.1 MB (135146406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2cffca40f23efc2ec52409559f7541adb0b7cd118c7cc4453e681548f99e5fa8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360280836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb597751f143cae7120d19deaaf0b38d84adec376fa0b6af1490740866e49a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:21:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:21:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:21:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:21:49 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:22:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:22:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:22:05 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:22:05 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:22:05 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:22:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:22:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a68633cb697b6c1b8ed77d6dbafd3f42712fe46e35d42049b8dbeb6e8ee5a9`  
		Last Modified: Sat, 05 Nov 2022 00:22:55 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcebb94154f7acf8c17539ddd712579de1285aafa21bcba39223b53170b519c0`  
		Last Modified: Sat, 05 Nov 2022 00:22:55 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103006b9193a4939adc0b2b9e9bc03a58b651b4e599aeee34624f483d8aa8125`  
		Last Modified: Sat, 05 Nov 2022 00:23:01 GMT  
		Size: 135.0 MB (135004338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:ca0510ebc3af07b18633b85bcc2d8a5cdad54592c14e7da347733b0b033ba8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:16fc86ead987666437a52d5ffb21f757a9f680d66e9496ff2e67a3218e942dcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.9 MB (459884805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01716941f8149943a6ce4563587908e157294a3674482e9ea0ae61b09bcd98cb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f0eff8c70ec5666169803d3d29363b770cd767f5737c8495e2daa3808c87836f NEO4J_TARBALL=neo4j-enterprise-4.4.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:29:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:27 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:29:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:29:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:29:43 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:29:43 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:29:43 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:29:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:29:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca125a22b302cd343cacee168d5b903cb67454dbad4b9beb6a7fde88a20cc92`  
		Last Modified: Sat, 05 Nov 2022 00:31:31 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b6c396b59f997c6b58b716b3814847b7fd6a41bbf646fec9e0173103373be0`  
		Last Modified: Sat, 05 Nov 2022 00:31:30 GMT  
		Size: 7.6 KB (7610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02e3d6b828702563630ce089fa03b891021ce77040cb4a2745478ba0f7589ac`  
		Last Modified: Sat, 05 Nov 2022 00:31:41 GMT  
		Size: 230.0 MB (229997453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e137a7f9d8cf422932698bb5d44723a44627c1c9d0af6854536a237110c62917
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.1 MB (455133028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f185e413be73f173613fe65609ddd771a53842c87bb6266114a3555310b86508`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:22:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f0eff8c70ec5666169803d3d29363b770cd767f5737c8495e2daa3808c87836f NEO4J_TARBALL=neo4j-enterprise-4.4.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:22:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:22:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:22:09 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:22:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:22:29 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:22:29 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:22:29 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:22:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:22:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7141fd2ada856cec9eae5212941823d2ecb2f574da39e94940089ac75774917`  
		Last Modified: Sat, 05 Nov 2022 00:23:15 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425e5909cf8762efa2d05ed7ccab5605cb28ddae559dbfa265f314ce1d98f99c`  
		Last Modified: Sat, 05 Nov 2022 00:23:15 GMT  
		Size: 7.6 KB (7610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2647528e7dcf5b08962b6f763c0550d88f8e7c455c73ff9814e7973ef8519cbd`  
		Last Modified: Sat, 05 Nov 2022 00:23:25 GMT  
		Size: 229.9 MB (229856535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.12`

```console
$ docker pull neo4j@sha256:bf3663e426274ab4a7c9df85208683aa8d57e527aef426ba59c5e95db7334ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.12` - linux; amd64

```console
$ docker pull neo4j@sha256:2dc174bb2f7d231ba332d83e8a92d805009f8d4d956a6f3fd7d5adfbb74ae6e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.0 MB (365033761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6836fda89e932c5b2bb82d9189c3c613244cc65332d598dd318ac899792f4f4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:29:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:08 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:29:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:29:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:29:21 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:29:21 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:29:21 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:29:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:29:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90050ec34ac0011d80656d8be239105a2b3ecb3bad879ee21850eb8680c404d7`  
		Last Modified: Sat, 05 Nov 2022 00:31:01 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a40fb45dc90f9b7d53ac018f9694e4cc68644d8226056d4f7c6cff44827dce`  
		Last Modified: Sat, 05 Nov 2022 00:31:01 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584ccb6f6ca3f9eae474080c63992c142a9e4e46e754d737235f18054ab6da2b`  
		Last Modified: Sat, 05 Nov 2022 00:31:08 GMT  
		Size: 135.1 MB (135146406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.12` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2cffca40f23efc2ec52409559f7541adb0b7cd118c7cc4453e681548f99e5fa8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360280836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb597751f143cae7120d19deaaf0b38d84adec376fa0b6af1490740866e49a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:21:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:21:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:21:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:21:49 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:22:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:22:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:22:05 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:22:05 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:22:05 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:22:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:22:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a68633cb697b6c1b8ed77d6dbafd3f42712fe46e35d42049b8dbeb6e8ee5a9`  
		Last Modified: Sat, 05 Nov 2022 00:22:55 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcebb94154f7acf8c17539ddd712579de1285aafa21bcba39223b53170b519c0`  
		Last Modified: Sat, 05 Nov 2022 00:22:55 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103006b9193a4939adc0b2b9e9bc03a58b651b4e599aeee34624f483d8aa8125`  
		Last Modified: Sat, 05 Nov 2022 00:23:01 GMT  
		Size: 135.0 MB (135004338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.12-community`

```console
$ docker pull neo4j@sha256:bf3663e426274ab4a7c9df85208683aa8d57e527aef426ba59c5e95db7334ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.12-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2dc174bb2f7d231ba332d83e8a92d805009f8d4d956a6f3fd7d5adfbb74ae6e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.0 MB (365033761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6836fda89e932c5b2bb82d9189c3c613244cc65332d598dd318ac899792f4f4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:29:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:08 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:29:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:29:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:29:21 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:29:21 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:29:21 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:29:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:29:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90050ec34ac0011d80656d8be239105a2b3ecb3bad879ee21850eb8680c404d7`  
		Last Modified: Sat, 05 Nov 2022 00:31:01 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a40fb45dc90f9b7d53ac018f9694e4cc68644d8226056d4f7c6cff44827dce`  
		Last Modified: Sat, 05 Nov 2022 00:31:01 GMT  
		Size: 7.6 KB (7613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584ccb6f6ca3f9eae474080c63992c142a9e4e46e754d737235f18054ab6da2b`  
		Last Modified: Sat, 05 Nov 2022 00:31:08 GMT  
		Size: 135.1 MB (135146406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.12-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2cffca40f23efc2ec52409559f7541adb0b7cd118c7cc4453e681548f99e5fa8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360280836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb597751f143cae7120d19deaaf0b38d84adec376fa0b6af1490740866e49a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:21:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=58f2ab847b1898c3f33731dc247784459223185307a4c89757f43ea94eb2a491 NEO4J_TARBALL=neo4j-community-4.4.12-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:21:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:21:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:21:49 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:22:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:22:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:22:05 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:22:05 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:22:05 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:22:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:22:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a68633cb697b6c1b8ed77d6dbafd3f42712fe46e35d42049b8dbeb6e8ee5a9`  
		Last Modified: Sat, 05 Nov 2022 00:22:55 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcebb94154f7acf8c17539ddd712579de1285aafa21bcba39223b53170b519c0`  
		Last Modified: Sat, 05 Nov 2022 00:22:55 GMT  
		Size: 7.6 KB (7612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103006b9193a4939adc0b2b9e9bc03a58b651b4e599aeee34624f483d8aa8125`  
		Last Modified: Sat, 05 Nov 2022 00:23:01 GMT  
		Size: 135.0 MB (135004338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.12-enterprise`

```console
$ docker pull neo4j@sha256:ca0510ebc3af07b18633b85bcc2d8a5cdad54592c14e7da347733b0b033ba8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.12-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:16fc86ead987666437a52d5ffb21f757a9f680d66e9496ff2e67a3218e942dcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.9 MB (459884805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01716941f8149943a6ce4563587908e157294a3674482e9ea0ae61b09bcd98cb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:29:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f0eff8c70ec5666169803d3d29363b770cd767f5737c8495e2daa3808c87836f NEO4J_TARBALL=neo4j-enterprise-4.4.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:29:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:29:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:29:27 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:29:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:29:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:29:43 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:29:43 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:29:43 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:29:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:29:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca125a22b302cd343cacee168d5b903cb67454dbad4b9beb6a7fde88a20cc92`  
		Last Modified: Sat, 05 Nov 2022 00:31:31 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b6c396b59f997c6b58b716b3814847b7fd6a41bbf646fec9e0173103373be0`  
		Last Modified: Sat, 05 Nov 2022 00:31:30 GMT  
		Size: 7.6 KB (7610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02e3d6b828702563630ce089fa03b891021ce77040cb4a2745478ba0f7589ac`  
		Last Modified: Sat, 05 Nov 2022 00:31:41 GMT  
		Size: 230.0 MB (229997453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.12-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e137a7f9d8cf422932698bb5d44723a44627c1c9d0af6854536a237110c62917
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.1 MB (455133028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f185e413be73f173613fe65609ddd771a53842c87bb6266114a3555310b86508`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Sat, 05 Nov 2022 00:22:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f0eff8c70ec5666169803d3d29363b770cd767f5737c8495e2daa3808c87836f NEO4J_TARBALL=neo4j-enterprise-4.4.12-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sat, 05 Nov 2022 00:22:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
# Sat, 05 Nov 2022 00:22:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sat, 05 Nov 2022 00:22:09 GMT
COPY multi:8d06e2159cef389ad848accdd078d2b91b147b7708e8ebf82c3f2530c0cabbdf in /startup/ 
# Sat, 05 Nov 2022 00:22:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.12-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sat, 05 Nov 2022 00:22:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:22:29 GMT
WORKDIR /var/lib/neo4j
# Sat, 05 Nov 2022 00:22:29 GMT
VOLUME [/data /logs]
# Sat, 05 Nov 2022 00:22:29 GMT
EXPOSE 7473 7474 7687
# Sat, 05 Nov 2022 00:22:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:22:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7141fd2ada856cec9eae5212941823d2ecb2f574da39e94940089ac75774917`  
		Last Modified: Sat, 05 Nov 2022 00:23:15 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425e5909cf8762efa2d05ed7ccab5605cb28ddae559dbfa265f314ce1d98f99c`  
		Last Modified: Sat, 05 Nov 2022 00:23:15 GMT  
		Size: 7.6 KB (7610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2647528e7dcf5b08962b6f763c0550d88f8e7c455c73ff9814e7973ef8519cbd`  
		Last Modified: Sat, 05 Nov 2022 00:23:25 GMT  
		Size: 229.9 MB (229856535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:fc99f5721a0badff3376526670a25a71f524dabb48f19ca383c1d2ff5db3c9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:b780c8381e7f1ab5ca8fe737276dbefbe7525bbd31cdc009b5d3810938dcba26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334277794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b92f0b7f95023408457dd46c1832f690f17828af1ec34a4a2b5328f2f2e0ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:53:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 20:53:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 20:53:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 20:53:41 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 20:53:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:53:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:53:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 20:53:55 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 20:53:55 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 20:53:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:53:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3112b4ae6e1a6961c3b59de4b733095baef2a2ac136c1fad7d9c2ae6c42492d`  
		Last Modified: Wed, 02 Nov 2022 20:56:11 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c89cfb52d22682f78babb4c91e0091ab16e91e38a29acbcc8a924c6e0a2059`  
		Last Modified: Wed, 02 Nov 2022 20:56:12 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129efcacc87bccae32585727944036d41362d927953efc157220609baa63f6ec`  
		Last Modified: Wed, 02 Nov 2022 20:56:18 GMT  
		Size: 110.7 MB (110708707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:26c2bac6ae0667ebbae325805848a20b6037c7ed6d450190d97db28091be20b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331545745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86073f4afd276e313eac90b043f954f932c77e8eb1a843a26bfdc24206cbcb9b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 21:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 21:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 21:26:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:26:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:26:29 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 21:26:29 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 21:26:30 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 21:26:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 21:26:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449edc3d08e467ce37d14ad7fa99aac6b03a0517ba1199eff5c63e54cf7add1c`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b0f871a10e6921abeb9ee66ec6092c30fca9379c1f7f428047eb46ff850cf`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c44bbd671eb7f05a3596c9a2ed39098a38c3b7ec17520fcd09550a3cec5fd`  
		Last Modified: Wed, 02 Nov 2022 21:27:47 GMT  
		Size: 110.6 MB (110566224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:fc99f5721a0badff3376526670a25a71f524dabb48f19ca383c1d2ff5db3c9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b780c8381e7f1ab5ca8fe737276dbefbe7525bbd31cdc009b5d3810938dcba26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334277794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b92f0b7f95023408457dd46c1832f690f17828af1ec34a4a2b5328f2f2e0ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:53:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 20:53:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 20:53:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 20:53:41 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 20:53:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:53:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:53:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 20:53:55 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 20:53:55 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 20:53:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:53:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3112b4ae6e1a6961c3b59de4b733095baef2a2ac136c1fad7d9c2ae6c42492d`  
		Last Modified: Wed, 02 Nov 2022 20:56:11 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c89cfb52d22682f78babb4c91e0091ab16e91e38a29acbcc8a924c6e0a2059`  
		Last Modified: Wed, 02 Nov 2022 20:56:12 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129efcacc87bccae32585727944036d41362d927953efc157220609baa63f6ec`  
		Last Modified: Wed, 02 Nov 2022 20:56:18 GMT  
		Size: 110.7 MB (110708707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:26c2bac6ae0667ebbae325805848a20b6037c7ed6d450190d97db28091be20b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331545745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86073f4afd276e313eac90b043f954f932c77e8eb1a843a26bfdc24206cbcb9b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 21:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 21:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 21:26:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:26:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:26:29 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 21:26:29 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 21:26:30 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 21:26:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 21:26:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449edc3d08e467ce37d14ad7fa99aac6b03a0517ba1199eff5c63e54cf7add1c`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b0f871a10e6921abeb9ee66ec6092c30fca9379c1f7f428047eb46ff850cf`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c44bbd671eb7f05a3596c9a2ed39098a38c3b7ec17520fcd09550a3cec5fd`  
		Last Modified: Wed, 02 Nov 2022 21:27:47 GMT  
		Size: 110.6 MB (110566224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:e021c6e0e7534db9b8190feebc1d5dc26d6f7283ac590cdc44cfc8ab86431df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b34e1e719be447231403dd94cfd345a05c8a392d41151e9793b982e6592f0000
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429865976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f220f6cd2b3afd2d99fa59ceaa3fc9b76744d78c90be6021ecd5e5948b5f4243`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:54:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 20:54:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 20:54:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 20:54:01 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 20:54:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:54:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:54:16 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 20:54:17 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 20:54:17 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 20:54:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:54:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949ddfe1fdeacf2ea67e79bc3abace5904dfd7dcd636be30d00a78f9ba919503`  
		Last Modified: Wed, 02 Nov 2022 20:56:36 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe1ea32a9edbccfd04f44d1138b64863fd3af16c0ab459d6419d3deef9f92b1`  
		Last Modified: Wed, 02 Nov 2022 20:56:36 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a228a3b945ff6c7b8b12c705b99f868be49a7b05748b4d73cde910ab6dbb2907`  
		Last Modified: Wed, 02 Nov 2022 20:56:46 GMT  
		Size: 206.3 MB (206296886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e3119bcd62fcef09e8864f6517b712b5296de5f58fe177e627a6698200cf7d74
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.1 MB (427132945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e695ccc82a44afd052c6eda03ebac0950167bdfc0e110c6b40f1528a146c85a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 21:26:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 21:26:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 21:26:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 21:26:34 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 21:26:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:26:46 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 21:26:46 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 21:26:46 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 21:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 21:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e1593c15c9163d2ee4a4e2391f77ac55b9c01f8f67f9c93dd104d15c108b16`  
		Last Modified: Wed, 02 Nov 2022 21:28:07 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33595905568863e78756e67cc0a78b42d4c5b7a0a84f6be00a47fa1ed511c2f`  
		Last Modified: Wed, 02 Nov 2022 21:28:07 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8773f8e2c7db03b2d9ded50475c64fc817c364574216c5f4c96a68dd02557a95`  
		Last Modified: Wed, 02 Nov 2022 21:28:15 GMT  
		Size: 206.2 MB (206153423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1.0`

```console
$ docker pull neo4j@sha256:fc99f5721a0badff3376526670a25a71f524dabb48f19ca383c1d2ff5db3c9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1.0` - linux; amd64

```console
$ docker pull neo4j@sha256:b780c8381e7f1ab5ca8fe737276dbefbe7525bbd31cdc009b5d3810938dcba26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334277794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b92f0b7f95023408457dd46c1832f690f17828af1ec34a4a2b5328f2f2e0ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:53:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 20:53:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 20:53:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 20:53:41 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 20:53:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:53:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:53:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 20:53:55 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 20:53:55 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 20:53:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:53:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3112b4ae6e1a6961c3b59de4b733095baef2a2ac136c1fad7d9c2ae6c42492d`  
		Last Modified: Wed, 02 Nov 2022 20:56:11 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c89cfb52d22682f78babb4c91e0091ab16e91e38a29acbcc8a924c6e0a2059`  
		Last Modified: Wed, 02 Nov 2022 20:56:12 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129efcacc87bccae32585727944036d41362d927953efc157220609baa63f6ec`  
		Last Modified: Wed, 02 Nov 2022 20:56:18 GMT  
		Size: 110.7 MB (110708707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:26c2bac6ae0667ebbae325805848a20b6037c7ed6d450190d97db28091be20b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331545745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86073f4afd276e313eac90b043f954f932c77e8eb1a843a26bfdc24206cbcb9b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 21:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 21:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 21:26:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:26:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:26:29 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 21:26:29 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 21:26:30 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 21:26:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 21:26:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449edc3d08e467ce37d14ad7fa99aac6b03a0517ba1199eff5c63e54cf7add1c`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b0f871a10e6921abeb9ee66ec6092c30fca9379c1f7f428047eb46ff850cf`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c44bbd671eb7f05a3596c9a2ed39098a38c3b7ec17520fcd09550a3cec5fd`  
		Last Modified: Wed, 02 Nov 2022 21:27:47 GMT  
		Size: 110.6 MB (110566224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1.0-community`

```console
$ docker pull neo4j@sha256:fc99f5721a0badff3376526670a25a71f524dabb48f19ca383c1d2ff5db3c9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b780c8381e7f1ab5ca8fe737276dbefbe7525bbd31cdc009b5d3810938dcba26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334277794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b92f0b7f95023408457dd46c1832f690f17828af1ec34a4a2b5328f2f2e0ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:53:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 20:53:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 20:53:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 20:53:41 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 20:53:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:53:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:53:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 20:53:55 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 20:53:55 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 20:53:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:53:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3112b4ae6e1a6961c3b59de4b733095baef2a2ac136c1fad7d9c2ae6c42492d`  
		Last Modified: Wed, 02 Nov 2022 20:56:11 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c89cfb52d22682f78babb4c91e0091ab16e91e38a29acbcc8a924c6e0a2059`  
		Last Modified: Wed, 02 Nov 2022 20:56:12 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129efcacc87bccae32585727944036d41362d927953efc157220609baa63f6ec`  
		Last Modified: Wed, 02 Nov 2022 20:56:18 GMT  
		Size: 110.7 MB (110708707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:26c2bac6ae0667ebbae325805848a20b6037c7ed6d450190d97db28091be20b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331545745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86073f4afd276e313eac90b043f954f932c77e8eb1a843a26bfdc24206cbcb9b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 21:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 21:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 21:26:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:26:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:26:29 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 21:26:29 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 21:26:30 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 21:26:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 21:26:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449edc3d08e467ce37d14ad7fa99aac6b03a0517ba1199eff5c63e54cf7add1c`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b0f871a10e6921abeb9ee66ec6092c30fca9379c1f7f428047eb46ff850cf`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c44bbd671eb7f05a3596c9a2ed39098a38c3b7ec17520fcd09550a3cec5fd`  
		Last Modified: Wed, 02 Nov 2022 21:27:47 GMT  
		Size: 110.6 MB (110566224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.1.0-enterprise`

```console
$ docker pull neo4j@sha256:e021c6e0e7534db9b8190feebc1d5dc26d6f7283ac590cdc44cfc8ab86431df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.1.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b34e1e719be447231403dd94cfd345a05c8a392d41151e9793b982e6592f0000
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429865976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f220f6cd2b3afd2d99fa59ceaa3fc9b76744d78c90be6021ecd5e5948b5f4243`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:54:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 20:54:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 20:54:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 20:54:01 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 20:54:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:54:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:54:16 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 20:54:17 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 20:54:17 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 20:54:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:54:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949ddfe1fdeacf2ea67e79bc3abace5904dfd7dcd636be30d00a78f9ba919503`  
		Last Modified: Wed, 02 Nov 2022 20:56:36 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe1ea32a9edbccfd04f44d1138b64863fd3af16c0ab459d6419d3deef9f92b1`  
		Last Modified: Wed, 02 Nov 2022 20:56:36 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a228a3b945ff6c7b8b12c705b99f868be49a7b05748b4d73cde910ab6dbb2907`  
		Last Modified: Wed, 02 Nov 2022 20:56:46 GMT  
		Size: 206.3 MB (206296886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.1.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e3119bcd62fcef09e8864f6517b712b5296de5f58fe177e627a6698200cf7d74
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.1 MB (427132945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e695ccc82a44afd052c6eda03ebac0950167bdfc0e110c6b40f1528a146c85a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 21:26:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 21:26:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 21:26:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 21:26:34 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 21:26:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:26:46 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 21:26:46 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 21:26:46 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 21:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 21:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e1593c15c9163d2ee4a4e2391f77ac55b9c01f8f67f9c93dd104d15c108b16`  
		Last Modified: Wed, 02 Nov 2022 21:28:07 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33595905568863e78756e67cc0a78b42d4c5b7a0a84f6be00a47fa1ed511c2f`  
		Last Modified: Wed, 02 Nov 2022 21:28:07 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8773f8e2c7db03b2d9ded50475c64fc817c364574216c5f4c96a68dd02557a95`  
		Last Modified: Wed, 02 Nov 2022 21:28:15 GMT  
		Size: 206.2 MB (206153423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:fc99f5721a0badff3376526670a25a71f524dabb48f19ca383c1d2ff5db3c9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:b780c8381e7f1ab5ca8fe737276dbefbe7525bbd31cdc009b5d3810938dcba26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334277794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b92f0b7f95023408457dd46c1832f690f17828af1ec34a4a2b5328f2f2e0ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:53:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 20:53:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 20:53:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 20:53:41 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 20:53:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:53:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:53:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 20:53:55 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 20:53:55 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 20:53:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:53:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3112b4ae6e1a6961c3b59de4b733095baef2a2ac136c1fad7d9c2ae6c42492d`  
		Last Modified: Wed, 02 Nov 2022 20:56:11 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c89cfb52d22682f78babb4c91e0091ab16e91e38a29acbcc8a924c6e0a2059`  
		Last Modified: Wed, 02 Nov 2022 20:56:12 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129efcacc87bccae32585727944036d41362d927953efc157220609baa63f6ec`  
		Last Modified: Wed, 02 Nov 2022 20:56:18 GMT  
		Size: 110.7 MB (110708707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:26c2bac6ae0667ebbae325805848a20b6037c7ed6d450190d97db28091be20b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331545745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86073f4afd276e313eac90b043f954f932c77e8eb1a843a26bfdc24206cbcb9b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 21:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 21:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 21:26:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:26:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:26:29 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 21:26:29 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 21:26:30 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 21:26:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 21:26:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449edc3d08e467ce37d14ad7fa99aac6b03a0517ba1199eff5c63e54cf7add1c`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b0f871a10e6921abeb9ee66ec6092c30fca9379c1f7f428047eb46ff850cf`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c44bbd671eb7f05a3596c9a2ed39098a38c3b7ec17520fcd09550a3cec5fd`  
		Last Modified: Wed, 02 Nov 2022 21:27:47 GMT  
		Size: 110.6 MB (110566224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:e021c6e0e7534db9b8190feebc1d5dc26d6f7283ac590cdc44cfc8ab86431df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b34e1e719be447231403dd94cfd345a05c8a392d41151e9793b982e6592f0000
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429865976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f220f6cd2b3afd2d99fa59ceaa3fc9b76744d78c90be6021ecd5e5948b5f4243`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:54:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 20:54:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 20:54:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 20:54:01 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 20:54:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:54:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:54:16 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 20:54:17 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 20:54:17 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 20:54:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:54:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949ddfe1fdeacf2ea67e79bc3abace5904dfd7dcd636be30d00a78f9ba919503`  
		Last Modified: Wed, 02 Nov 2022 20:56:36 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe1ea32a9edbccfd04f44d1138b64863fd3af16c0ab459d6419d3deef9f92b1`  
		Last Modified: Wed, 02 Nov 2022 20:56:36 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a228a3b945ff6c7b8b12c705b99f868be49a7b05748b4d73cde910ab6dbb2907`  
		Last Modified: Wed, 02 Nov 2022 20:56:46 GMT  
		Size: 206.3 MB (206296886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e3119bcd62fcef09e8864f6517b712b5296de5f58fe177e627a6698200cf7d74
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.1 MB (427132945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e695ccc82a44afd052c6eda03ebac0950167bdfc0e110c6b40f1528a146c85a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 21:26:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5f9b6b6ec624932ed4611e8fadac3f8198853e53b3318cc9a588f1f9ff9a1fb1 NEO4J_TARBALL=neo4j-enterprise-5.1.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 21:26:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 21:26:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 21:26:34 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 21:26:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:26:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:26:46 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 21:26:46 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 21:26:46 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 21:26:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 21:26:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e1593c15c9163d2ee4a4e2391f77ac55b9c01f8f67f9c93dd104d15c108b16`  
		Last Modified: Wed, 02 Nov 2022 21:28:07 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33595905568863e78756e67cc0a78b42d4c5b7a0a84f6be00a47fa1ed511c2f`  
		Last Modified: Wed, 02 Nov 2022 21:28:07 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8773f8e2c7db03b2d9ded50475c64fc817c364574216c5f4c96a68dd02557a95`  
		Last Modified: Wed, 02 Nov 2022 21:28:15 GMT  
		Size: 206.2 MB (206153423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:fc99f5721a0badff3376526670a25a71f524dabb48f19ca383c1d2ff5db3c9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:b780c8381e7f1ab5ca8fe737276dbefbe7525bbd31cdc009b5d3810938dcba26
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334277794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b92f0b7f95023408457dd46c1832f690f17828af1ec34a4a2b5328f2f2e0ce`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:15:23 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:53:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 20:53:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 20:53:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 20:53:41 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 20:53:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:53:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:53:55 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 20:53:55 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 20:53:55 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 20:53:55 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:53:55 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f9b9477aacca86981c880c8ed7c4dbb56574cdcda91a39effa9c2332b96765`  
		Last Modified: Wed, 02 Nov 2022 20:27:47 GMT  
		Size: 192.1 MB (192137557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3112b4ae6e1a6961c3b59de4b733095baef2a2ac136c1fad7d9c2ae6c42492d`  
		Last Modified: Wed, 02 Nov 2022 20:56:11 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c89cfb52d22682f78babb4c91e0091ab16e91e38a29acbcc8a924c6e0a2059`  
		Last Modified: Wed, 02 Nov 2022 20:56:12 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129efcacc87bccae32585727944036d41362d927953efc157220609baa63f6ec`  
		Last Modified: Wed, 02 Nov 2022 20:56:18 GMT  
		Size: 110.7 MB (110708707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:26c2bac6ae0667ebbae325805848a20b6037c7ed6d450190d97db28091be20b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331545745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86073f4afd276e313eac90b043f954f932c77e8eb1a843a26bfdc24206cbcb9b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:40 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 21:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c8086d1f8558376754e7248a7d12838f024ca2699aa59e0aba30816b229ed4f4 NEO4J_TARBALL=neo4j-community-5.1.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
# Wed, 02 Nov 2022 21:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 02 Nov 2022 21:26:19 GMT
COPY multi:a11635e58e35f289c454771630762b2132b546d160631e2fe7ed78f034b4cc21 in /startup/ 
# Wed, 02 Nov 2022 21:26:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.1.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 21:26:29 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 21:26:29 GMT
WORKDIR /var/lib/neo4j
# Wed, 02 Nov 2022 21:26:29 GMT
VOLUME [/data /logs]
# Wed, 02 Nov 2022 21:26:30 GMT
EXPOSE 7473 7474 7687
# Wed, 02 Nov 2022 21:26:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 02 Nov 2022 21:26:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23c78a656ff98cd4a277e3c01f4d0eb067085f7d111e0f4a4c913c75ed384c0`  
		Last Modified: Wed, 02 Nov 2022 21:01:35 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449edc3d08e467ce37d14ad7fa99aac6b03a0517ba1199eff5c63e54cf7add1c`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40b0f871a10e6921abeb9ee66ec6092c30fca9379c1f7f428047eb46ff850cf`  
		Last Modified: Wed, 02 Nov 2022 21:27:42 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c44bbd671eb7f05a3596c9a2ed39098a38c3b7ec17520fcd09550a3cec5fd`  
		Last Modified: Wed, 02 Nov 2022 21:27:47 GMT  
		Size: 110.6 MB (110566224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
