<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.20`](#neo4j4420)
-	[`neo4j:4.4.20-community`](#neo4j4420-community)
-	[`neo4j:4.4.20-enterprise`](#neo4j4420-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.8`](#neo4j58)
-	[`neo4j:5.8-community`](#neo4j58-community)
-	[`neo4j:5.8-enterprise`](#neo4j58-enterprise)
-	[`neo4j:5.8.0`](#neo4j580)
-	[`neo4j:5.8.0-community`](#neo4j580-community)
-	[`neo4j:5.8.0-enterprise`](#neo4j580-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:a090aae75a1196a77e8c4db63162b4dd24cff2c13f36098e20ef749bfb7a05a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:6a6b044a9bcfcf5471d2e6de18fd12f30c4a7d9524cba11d67a472b7f61cd236
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349352799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9e0cc69fa89529b81f9cf8a5018c4cdc0c4d1b159522416b281dc2649366a4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Tue, 23 May 2023 04:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:29 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 04:19:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:19:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:19:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:19:40 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:19:40 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:19:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:19:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d55670465870b4ed7e55422bc8d1f860406f6c721565762235803c9213fbf`  
		Last Modified: Tue, 23 May 2023 04:21:15 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944f9e30d8972620dc456eefd69097d7d849c96b9be7ff0162a8287915f4205`  
		Last Modified: Tue, 23 May 2023 04:21:16 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ea06cd4d09fe43e59d5aa732cdd882be111e1abba2590e660dbbf546cf06c9`  
		Last Modified: Tue, 23 May 2023 04:21:21 GMT  
		Size: 119.4 MB (119387122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e19a3904b1c9735505da358b43c0f67e643697582f500bcd8508f6baf8d554c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344633309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2642ffc3a3e6d0002c48db99d33c900f1fb40a26d9582e7aa9d03f3cf79e5413`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:27:27 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Tue, 23 May 2023 07:57:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:40 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 07:57:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:50 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:50 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78c86840ae584aab4d9f49c5158125ceb03a9fcfcbb243c03ce4819b42d8729`  
		Last Modified: Tue, 23 May 2023 01:35:49 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2aa66620d323071640459df76a612d4e26ef9aaac9cd1ee314b9ecb40f5e54`  
		Last Modified: Tue, 23 May 2023 07:59:08 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163714976cfe610baff9c117972c80736465b397771952cb3039ac974f36d004`  
		Last Modified: Tue, 23 May 2023 07:59:08 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a4bafd26ff133c0d001ad1095dfb12c1ad4b0bf571072467e8a1e9a96c7dbe`  
		Last Modified: Tue, 23 May 2023 07:59:13 GMT  
		Size: 119.2 MB (119243762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:a090aae75a1196a77e8c4db63162b4dd24cff2c13f36098e20ef749bfb7a05a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:6a6b044a9bcfcf5471d2e6de18fd12f30c4a7d9524cba11d67a472b7f61cd236
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349352799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9e0cc69fa89529b81f9cf8a5018c4cdc0c4d1b159522416b281dc2649366a4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Tue, 23 May 2023 04:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:29 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 04:19:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:19:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:19:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:19:40 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:19:40 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:19:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:19:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d55670465870b4ed7e55422bc8d1f860406f6c721565762235803c9213fbf`  
		Last Modified: Tue, 23 May 2023 04:21:15 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944f9e30d8972620dc456eefd69097d7d849c96b9be7ff0162a8287915f4205`  
		Last Modified: Tue, 23 May 2023 04:21:16 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ea06cd4d09fe43e59d5aa732cdd882be111e1abba2590e660dbbf546cf06c9`  
		Last Modified: Tue, 23 May 2023 04:21:21 GMT  
		Size: 119.4 MB (119387122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e19a3904b1c9735505da358b43c0f67e643697582f500bcd8508f6baf8d554c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344633309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2642ffc3a3e6d0002c48db99d33c900f1fb40a26d9582e7aa9d03f3cf79e5413`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:27:27 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Tue, 23 May 2023 07:57:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:40 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 07:57:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:50 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:50 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78c86840ae584aab4d9f49c5158125ceb03a9fcfcbb243c03ce4819b42d8729`  
		Last Modified: Tue, 23 May 2023 01:35:49 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2aa66620d323071640459df76a612d4e26ef9aaac9cd1ee314b9ecb40f5e54`  
		Last Modified: Tue, 23 May 2023 07:59:08 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163714976cfe610baff9c117972c80736465b397771952cb3039ac974f36d004`  
		Last Modified: Tue, 23 May 2023 07:59:08 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a4bafd26ff133c0d001ad1095dfb12c1ad4b0bf571072467e8a1e9a96c7dbe`  
		Last Modified: Tue, 23 May 2023 07:59:13 GMT  
		Size: 119.2 MB (119243762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:dab8a67dd5d8ebcae892525eaa01a382d46e91e98daa1af18eca00190d1b4f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1f923d5a2065ef0724f7d8879f7f8a859d1c1f356a62476b0124079706d8e51c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.7 MB (446655244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c4b1434625e0c234388b31b8a5415a44db07801663a571fea64e543f432c95`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d25329edbbf8a75e9e32d4d0c38fb817f155e171d4cf8b7509a7b50d35bb2549 NEO4J_TARBALL=neo4j-enterprise-4.4.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
# Tue, 23 May 2023 04:19:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:44 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 04:20:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:20:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:20:04 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:20:04 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:20:05 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:20:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:20:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91edb1f24e0fa5c54f5300b585704a4d401da13dadc7447121997849fd67342f`  
		Last Modified: Tue, 23 May 2023 04:21:40 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e0188044204c2900cc08bfb19fadd149e0066eb88101a348a62949de27a7f6`  
		Last Modified: Tue, 23 May 2023 04:21:40 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeed45053abf132b8a87e6a48b3b3ae1e7407e8a5412fe47eb18529ca784cb7`  
		Last Modified: Tue, 23 May 2023 04:21:49 GMT  
		Size: 216.7 MB (216689569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d03be8f353495a39e25b6178c9e7b1421fa1b4871d472d70ffe2714a9d0c6429
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.9 MB (441933070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2792ee70d94de35e44918463b174e04914b7dd30d44e6398e2634ca85fc1fd8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:27:27 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d25329edbbf8a75e9e32d4d0c38fb817f155e171d4cf8b7509a7b50d35bb2549 NEO4J_TARBALL=neo4j-enterprise-4.4.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
# Tue, 23 May 2023 07:57:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 07:58:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:58:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:58:07 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:58:07 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:58:07 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:58:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:58:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78c86840ae584aab4d9f49c5158125ceb03a9fcfcbb243c03ce4819b42d8729`  
		Last Modified: Tue, 23 May 2023 01:35:49 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc5e8a8bf2f631f7b0b9584f1b366c965794bd6a4e448a3f3489ea2856b97bb`  
		Last Modified: Tue, 23 May 2023 07:59:25 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1a215065eca4c41acd7366772d5c773013966e7935acdc4b9374a6a040fdaf`  
		Last Modified: Tue, 23 May 2023 07:59:25 GMT  
		Size: 8.7 KB (8702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015dcf261c2326e6a0a8d31d216255815758d79f20ecf7dce0cea87cf53a53c6`  
		Last Modified: Tue, 23 May 2023 07:59:33 GMT  
		Size: 216.5 MB (216543530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.20`

```console
$ docker pull neo4j@sha256:a090aae75a1196a77e8c4db63162b4dd24cff2c13f36098e20ef749bfb7a05a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.20` - linux; amd64

```console
$ docker pull neo4j@sha256:6a6b044a9bcfcf5471d2e6de18fd12f30c4a7d9524cba11d67a472b7f61cd236
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349352799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9e0cc69fa89529b81f9cf8a5018c4cdc0c4d1b159522416b281dc2649366a4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Tue, 23 May 2023 04:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:29 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 04:19:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:19:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:19:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:19:40 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:19:40 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:19:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:19:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d55670465870b4ed7e55422bc8d1f860406f6c721565762235803c9213fbf`  
		Last Modified: Tue, 23 May 2023 04:21:15 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944f9e30d8972620dc456eefd69097d7d849c96b9be7ff0162a8287915f4205`  
		Last Modified: Tue, 23 May 2023 04:21:16 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ea06cd4d09fe43e59d5aa732cdd882be111e1abba2590e660dbbf546cf06c9`  
		Last Modified: Tue, 23 May 2023 04:21:21 GMT  
		Size: 119.4 MB (119387122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.20` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e19a3904b1c9735505da358b43c0f67e643697582f500bcd8508f6baf8d554c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344633309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2642ffc3a3e6d0002c48db99d33c900f1fb40a26d9582e7aa9d03f3cf79e5413`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:27:27 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Tue, 23 May 2023 07:57:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:40 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 07:57:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:50 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:50 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78c86840ae584aab4d9f49c5158125ceb03a9fcfcbb243c03ce4819b42d8729`  
		Last Modified: Tue, 23 May 2023 01:35:49 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2aa66620d323071640459df76a612d4e26ef9aaac9cd1ee314b9ecb40f5e54`  
		Last Modified: Tue, 23 May 2023 07:59:08 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163714976cfe610baff9c117972c80736465b397771952cb3039ac974f36d004`  
		Last Modified: Tue, 23 May 2023 07:59:08 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a4bafd26ff133c0d001ad1095dfb12c1ad4b0bf571072467e8a1e9a96c7dbe`  
		Last Modified: Tue, 23 May 2023 07:59:13 GMT  
		Size: 119.2 MB (119243762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.20-community`

```console
$ docker pull neo4j@sha256:a090aae75a1196a77e8c4db63162b4dd24cff2c13f36098e20ef749bfb7a05a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.20-community` - linux; amd64

```console
$ docker pull neo4j@sha256:6a6b044a9bcfcf5471d2e6de18fd12f30c4a7d9524cba11d67a472b7f61cd236
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349352799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9e0cc69fa89529b81f9cf8a5018c4cdc0c4d1b159522416b281dc2649366a4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Tue, 23 May 2023 04:19:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:29 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 04:19:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:19:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:19:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:19:40 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:19:40 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:19:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:19:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d55670465870b4ed7e55422bc8d1f860406f6c721565762235803c9213fbf`  
		Last Modified: Tue, 23 May 2023 04:21:15 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944f9e30d8972620dc456eefd69097d7d849c96b9be7ff0162a8287915f4205`  
		Last Modified: Tue, 23 May 2023 04:21:16 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ea06cd4d09fe43e59d5aa732cdd882be111e1abba2590e660dbbf546cf06c9`  
		Last Modified: Tue, 23 May 2023 04:21:21 GMT  
		Size: 119.4 MB (119387122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.20-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e19a3904b1c9735505da358b43c0f67e643697582f500bcd8508f6baf8d554c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344633309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2642ffc3a3e6d0002c48db99d33c900f1fb40a26d9582e7aa9d03f3cf79e5413`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:27:27 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Tue, 23 May 2023 07:57:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:40 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 07:57:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:50 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:50 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:50 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:50 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:50 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:50 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78c86840ae584aab4d9f49c5158125ceb03a9fcfcbb243c03ce4819b42d8729`  
		Last Modified: Tue, 23 May 2023 01:35:49 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2aa66620d323071640459df76a612d4e26ef9aaac9cd1ee314b9ecb40f5e54`  
		Last Modified: Tue, 23 May 2023 07:59:08 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163714976cfe610baff9c117972c80736465b397771952cb3039ac974f36d004`  
		Last Modified: Tue, 23 May 2023 07:59:08 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a4bafd26ff133c0d001ad1095dfb12c1ad4b0bf571072467e8a1e9a96c7dbe`  
		Last Modified: Tue, 23 May 2023 07:59:13 GMT  
		Size: 119.2 MB (119243762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.20-enterprise`

```console
$ docker pull neo4j@sha256:dab8a67dd5d8ebcae892525eaa01a382d46e91e98daa1af18eca00190d1b4f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.20-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1f923d5a2065ef0724f7d8879f7f8a859d1c1f356a62476b0124079706d8e51c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.7 MB (446655244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c4b1434625e0c234388b31b8a5415a44db07801663a571fea64e543f432c95`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d25329edbbf8a75e9e32d4d0c38fb817f155e171d4cf8b7509a7b50d35bb2549 NEO4J_TARBALL=neo4j-enterprise-4.4.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
# Tue, 23 May 2023 04:19:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:44 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 04:20:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:20:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:20:04 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:20:04 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:20:05 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:20:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:20:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91edb1f24e0fa5c54f5300b585704a4d401da13dadc7447121997849fd67342f`  
		Last Modified: Tue, 23 May 2023 04:21:40 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e0188044204c2900cc08bfb19fadd149e0066eb88101a348a62949de27a7f6`  
		Last Modified: Tue, 23 May 2023 04:21:40 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeed45053abf132b8a87e6a48b3b3ae1e7407e8a5412fe47eb18529ca784cb7`  
		Last Modified: Tue, 23 May 2023 04:21:49 GMT  
		Size: 216.7 MB (216689569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.20-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d03be8f353495a39e25b6178c9e7b1421fa1b4871d472d70ffe2714a9d0c6429
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.9 MB (441933070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2792ee70d94de35e44918463b174e04914b7dd30d44e6398e2634ca85fc1fd8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:27:27 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d25329edbbf8a75e9e32d4d0c38fb817f155e171d4cf8b7509a7b50d35bb2549 NEO4J_TARBALL=neo4j-enterprise-4.4.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
# Tue, 23 May 2023 07:57:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Tue, 23 May 2023 07:58:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:58:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:58:07 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:58:07 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:58:07 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:58:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:58:07 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78c86840ae584aab4d9f49c5158125ceb03a9fcfcbb243c03ce4819b42d8729`  
		Last Modified: Tue, 23 May 2023 01:35:49 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc5e8a8bf2f631f7b0b9584f1b366c965794bd6a4e448a3f3489ea2856b97bb`  
		Last Modified: Tue, 23 May 2023 07:59:25 GMT  
		Size: 3.9 KB (3882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1a215065eca4c41acd7366772d5c773013966e7935acdc4b9374a6a040fdaf`  
		Last Modified: Tue, 23 May 2023 07:59:25 GMT  
		Size: 8.7 KB (8702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015dcf261c2326e6a0a8d31d216255815758d79f20ecf7dce0cea87cf53a53c6`  
		Last Modified: Tue, 23 May 2023 07:59:33 GMT  
		Size: 216.5 MB (216543530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:7ea588795119ec4895bc2ee241bc1bb0babb91f745aa79c3abff217553516c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:3546a3130e80a51d420e7a07e925aa6465d2af87b77add87cb35f43c7a14caeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856754509efc0504255ca580c2f4308504989facbbc2f883e5be0eb8553b71a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:18:42 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:18:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:18:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:18:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:18:54 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:18:54 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:18:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:18:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f729f64977b963f46455a8c8eac4f2d66517b11d7bfc809833c1ded8562aef`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73577e5c94088cfb6c46a1b5b7842a84de0cfa9f0a77db52f267a2effe3bc56b`  
		Last Modified: Tue, 23 May 2023 04:20:24 GMT  
		Size: 114.7 MB (114688687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58f84aa8f52e3e23cf8f32852a4c4ce52d494dbfe37e874d6933b5c23f60d4d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d38afe56dd7904476cd5c55fa58f0f761fcf9cf258edffbb66d71d8240f481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:14 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:14 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:14 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9405ba3d07fb1648e429cb012b11fa1e9e0bc8f9e32cbb1ecc7a6336645a7`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43d5afb8207c802f6936e201f3e5fca058072eddcd1ec7a81612cdcb274e54`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc2a4561d824a9a0379e832a6bef3a66e3dee4a9b6509d9cee328294b4b8ca`  
		Last Modified: Tue, 23 May 2023 07:58:24 GMT  
		Size: 114.5 MB (114544975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:7ea588795119ec4895bc2ee241bc1bb0babb91f745aa79c3abff217553516c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3546a3130e80a51d420e7a07e925aa6465d2af87b77add87cb35f43c7a14caeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856754509efc0504255ca580c2f4308504989facbbc2f883e5be0eb8553b71a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:18:42 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:18:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:18:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:18:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:18:54 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:18:54 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:18:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:18:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f729f64977b963f46455a8c8eac4f2d66517b11d7bfc809833c1ded8562aef`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73577e5c94088cfb6c46a1b5b7842a84de0cfa9f0a77db52f267a2effe3bc56b`  
		Last Modified: Tue, 23 May 2023 04:20:24 GMT  
		Size: 114.7 MB (114688687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58f84aa8f52e3e23cf8f32852a4c4ce52d494dbfe37e874d6933b5c23f60d4d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d38afe56dd7904476cd5c55fa58f0f761fcf9cf258edffbb66d71d8240f481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:14 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:14 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:14 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9405ba3d07fb1648e429cb012b11fa1e9e0bc8f9e32cbb1ecc7a6336645a7`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43d5afb8207c802f6936e201f3e5fca058072eddcd1ec7a81612cdcb274e54`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc2a4561d824a9a0379e832a6bef3a66e3dee4a9b6509d9cee328294b4b8ca`  
		Last Modified: Tue, 23 May 2023 07:58:24 GMT  
		Size: 114.5 MB (114544975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:b156f6aa61bcc78b160f509e3c8dc756d6e41c534c1b5a63197f36f0b5cbf4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e89709d490cfe4ad4f7a49e9690a1d4397b18f251acf68f8b6f4f0e847f84032
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b1df17c9a9394414568590a6e11207fe6489768a304faa439ed658aab1f353`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:19:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:19:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:19:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:19:18 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:19:18 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:19:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:19:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5011326b12928bcd6584016f6aea605e8a53b9a1d6ac9a647ce032b78f52fad`  
		Last Modified: Tue, 23 May 2023 04:20:50 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52b348a8efca0e9ac27d6a133a3ac8ae18412cac16ac1971201175e18477aee`  
		Last Modified: Tue, 23 May 2023 04:20:49 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61c95b5adb6f2b7ba27e4fd29866e1a9e6af175a955727d5983fa7352d7e09a`  
		Last Modified: Tue, 23 May 2023 04:21:04 GMT  
		Size: 379.7 MB (379683148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:32ded246aadeb8ee061ec50663e26a4444eba7507a4df582d56ca3d26b955cd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0875faf7fcdd75294a86408d7d195d3c6b686d627662ea5ddeefc6a0595974b5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:17 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:35 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:35 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815452b64991cc8961cb048ef3e1bedd694c39634170adf9a67b672e7a31cd02`  
		Last Modified: Tue, 23 May 2023 07:58:43 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55dc57c3622b773ea70563455a583cc5e7ea3aeea05840c1fb6fc392f211ae3`  
		Last Modified: Tue, 23 May 2023 07:58:43 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ccd16d771409a85e60a6eb41535438c1a0571d753537819e4c25b2cb31eb48`  
		Last Modified: Tue, 23 May 2023 07:58:56 GMT  
		Size: 379.5 MB (379541292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8`

```console
$ docker pull neo4j@sha256:7ea588795119ec4895bc2ee241bc1bb0babb91f745aa79c3abff217553516c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8` - linux; amd64

```console
$ docker pull neo4j@sha256:3546a3130e80a51d420e7a07e925aa6465d2af87b77add87cb35f43c7a14caeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856754509efc0504255ca580c2f4308504989facbbc2f883e5be0eb8553b71a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:18:42 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:18:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:18:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:18:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:18:54 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:18:54 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:18:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:18:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f729f64977b963f46455a8c8eac4f2d66517b11d7bfc809833c1ded8562aef`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73577e5c94088cfb6c46a1b5b7842a84de0cfa9f0a77db52f267a2effe3bc56b`  
		Last Modified: Tue, 23 May 2023 04:20:24 GMT  
		Size: 114.7 MB (114688687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58f84aa8f52e3e23cf8f32852a4c4ce52d494dbfe37e874d6933b5c23f60d4d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d38afe56dd7904476cd5c55fa58f0f761fcf9cf258edffbb66d71d8240f481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:14 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:14 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:14 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9405ba3d07fb1648e429cb012b11fa1e9e0bc8f9e32cbb1ecc7a6336645a7`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43d5afb8207c802f6936e201f3e5fca058072eddcd1ec7a81612cdcb274e54`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc2a4561d824a9a0379e832a6bef3a66e3dee4a9b6509d9cee328294b4b8ca`  
		Last Modified: Tue, 23 May 2023 07:58:24 GMT  
		Size: 114.5 MB (114544975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8-community`

```console
$ docker pull neo4j@sha256:7ea588795119ec4895bc2ee241bc1bb0babb91f745aa79c3abff217553516c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3546a3130e80a51d420e7a07e925aa6465d2af87b77add87cb35f43c7a14caeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856754509efc0504255ca580c2f4308504989facbbc2f883e5be0eb8553b71a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:18:42 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:18:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:18:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:18:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:18:54 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:18:54 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:18:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:18:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f729f64977b963f46455a8c8eac4f2d66517b11d7bfc809833c1ded8562aef`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73577e5c94088cfb6c46a1b5b7842a84de0cfa9f0a77db52f267a2effe3bc56b`  
		Last Modified: Tue, 23 May 2023 04:20:24 GMT  
		Size: 114.7 MB (114688687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58f84aa8f52e3e23cf8f32852a4c4ce52d494dbfe37e874d6933b5c23f60d4d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d38afe56dd7904476cd5c55fa58f0f761fcf9cf258edffbb66d71d8240f481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:14 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:14 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:14 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9405ba3d07fb1648e429cb012b11fa1e9e0bc8f9e32cbb1ecc7a6336645a7`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43d5afb8207c802f6936e201f3e5fca058072eddcd1ec7a81612cdcb274e54`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc2a4561d824a9a0379e832a6bef3a66e3dee4a9b6509d9cee328294b4b8ca`  
		Last Modified: Tue, 23 May 2023 07:58:24 GMT  
		Size: 114.5 MB (114544975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8-enterprise`

```console
$ docker pull neo4j@sha256:b156f6aa61bcc78b160f509e3c8dc756d6e41c534c1b5a63197f36f0b5cbf4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e89709d490cfe4ad4f7a49e9690a1d4397b18f251acf68f8b6f4f0e847f84032
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b1df17c9a9394414568590a6e11207fe6489768a304faa439ed658aab1f353`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:19:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:19:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:19:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:19:18 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:19:18 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:19:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:19:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5011326b12928bcd6584016f6aea605e8a53b9a1d6ac9a647ce032b78f52fad`  
		Last Modified: Tue, 23 May 2023 04:20:50 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52b348a8efca0e9ac27d6a133a3ac8ae18412cac16ac1971201175e18477aee`  
		Last Modified: Tue, 23 May 2023 04:20:49 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61c95b5adb6f2b7ba27e4fd29866e1a9e6af175a955727d5983fa7352d7e09a`  
		Last Modified: Tue, 23 May 2023 04:21:04 GMT  
		Size: 379.7 MB (379683148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:32ded246aadeb8ee061ec50663e26a4444eba7507a4df582d56ca3d26b955cd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0875faf7fcdd75294a86408d7d195d3c6b686d627662ea5ddeefc6a0595974b5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:17 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:35 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:35 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815452b64991cc8961cb048ef3e1bedd694c39634170adf9a67b672e7a31cd02`  
		Last Modified: Tue, 23 May 2023 07:58:43 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55dc57c3622b773ea70563455a583cc5e7ea3aeea05840c1fb6fc392f211ae3`  
		Last Modified: Tue, 23 May 2023 07:58:43 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ccd16d771409a85e60a6eb41535438c1a0571d753537819e4c25b2cb31eb48`  
		Last Modified: Tue, 23 May 2023 07:58:56 GMT  
		Size: 379.5 MB (379541292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0`

```console
$ docker pull neo4j@sha256:7ea588795119ec4895bc2ee241bc1bb0babb91f745aa79c3abff217553516c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0` - linux; amd64

```console
$ docker pull neo4j@sha256:3546a3130e80a51d420e7a07e925aa6465d2af87b77add87cb35f43c7a14caeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856754509efc0504255ca580c2f4308504989facbbc2f883e5be0eb8553b71a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:18:42 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:18:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:18:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:18:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:18:54 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:18:54 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:18:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:18:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f729f64977b963f46455a8c8eac4f2d66517b11d7bfc809833c1ded8562aef`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73577e5c94088cfb6c46a1b5b7842a84de0cfa9f0a77db52f267a2effe3bc56b`  
		Last Modified: Tue, 23 May 2023 04:20:24 GMT  
		Size: 114.7 MB (114688687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58f84aa8f52e3e23cf8f32852a4c4ce52d494dbfe37e874d6933b5c23f60d4d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d38afe56dd7904476cd5c55fa58f0f761fcf9cf258edffbb66d71d8240f481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:14 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:14 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:14 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9405ba3d07fb1648e429cb012b11fa1e9e0bc8f9e32cbb1ecc7a6336645a7`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43d5afb8207c802f6936e201f3e5fca058072eddcd1ec7a81612cdcb274e54`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc2a4561d824a9a0379e832a6bef3a66e3dee4a9b6509d9cee328294b4b8ca`  
		Last Modified: Tue, 23 May 2023 07:58:24 GMT  
		Size: 114.5 MB (114544975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0-community`

```console
$ docker pull neo4j@sha256:7ea588795119ec4895bc2ee241bc1bb0babb91f745aa79c3abff217553516c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3546a3130e80a51d420e7a07e925aa6465d2af87b77add87cb35f43c7a14caeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856754509efc0504255ca580c2f4308504989facbbc2f883e5be0eb8553b71a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:18:42 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:18:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:18:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:18:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:18:54 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:18:54 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:18:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:18:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f729f64977b963f46455a8c8eac4f2d66517b11d7bfc809833c1ded8562aef`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73577e5c94088cfb6c46a1b5b7842a84de0cfa9f0a77db52f267a2effe3bc56b`  
		Last Modified: Tue, 23 May 2023 04:20:24 GMT  
		Size: 114.7 MB (114688687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58f84aa8f52e3e23cf8f32852a4c4ce52d494dbfe37e874d6933b5c23f60d4d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d38afe56dd7904476cd5c55fa58f0f761fcf9cf258edffbb66d71d8240f481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:14 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:14 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:14 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9405ba3d07fb1648e429cb012b11fa1e9e0bc8f9e32cbb1ecc7a6336645a7`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43d5afb8207c802f6936e201f3e5fca058072eddcd1ec7a81612cdcb274e54`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc2a4561d824a9a0379e832a6bef3a66e3dee4a9b6509d9cee328294b4b8ca`  
		Last Modified: Tue, 23 May 2023 07:58:24 GMT  
		Size: 114.5 MB (114544975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0-enterprise`

```console
$ docker pull neo4j@sha256:b156f6aa61bcc78b160f509e3c8dc756d6e41c534c1b5a63197f36f0b5cbf4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e89709d490cfe4ad4f7a49e9690a1d4397b18f251acf68f8b6f4f0e847f84032
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b1df17c9a9394414568590a6e11207fe6489768a304faa439ed658aab1f353`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:19:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:19:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:19:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:19:18 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:19:18 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:19:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:19:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5011326b12928bcd6584016f6aea605e8a53b9a1d6ac9a647ce032b78f52fad`  
		Last Modified: Tue, 23 May 2023 04:20:50 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52b348a8efca0e9ac27d6a133a3ac8ae18412cac16ac1971201175e18477aee`  
		Last Modified: Tue, 23 May 2023 04:20:49 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61c95b5adb6f2b7ba27e4fd29866e1a9e6af175a955727d5983fa7352d7e09a`  
		Last Modified: Tue, 23 May 2023 04:21:04 GMT  
		Size: 379.7 MB (379683148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:32ded246aadeb8ee061ec50663e26a4444eba7507a4df582d56ca3d26b955cd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0875faf7fcdd75294a86408d7d195d3c6b686d627662ea5ddeefc6a0595974b5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:17 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:35 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:35 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815452b64991cc8961cb048ef3e1bedd694c39634170adf9a67b672e7a31cd02`  
		Last Modified: Tue, 23 May 2023 07:58:43 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55dc57c3622b773ea70563455a583cc5e7ea3aeea05840c1fb6fc392f211ae3`  
		Last Modified: Tue, 23 May 2023 07:58:43 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ccd16d771409a85e60a6eb41535438c1a0571d753537819e4c25b2cb31eb48`  
		Last Modified: Tue, 23 May 2023 07:58:56 GMT  
		Size: 379.5 MB (379541292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:7ea588795119ec4895bc2ee241bc1bb0babb91f745aa79c3abff217553516c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:3546a3130e80a51d420e7a07e925aa6465d2af87b77add87cb35f43c7a14caeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856754509efc0504255ca580c2f4308504989facbbc2f883e5be0eb8553b71a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:18:42 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:18:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:18:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:18:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:18:54 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:18:54 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:18:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:18:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f729f64977b963f46455a8c8eac4f2d66517b11d7bfc809833c1ded8562aef`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73577e5c94088cfb6c46a1b5b7842a84de0cfa9f0a77db52f267a2effe3bc56b`  
		Last Modified: Tue, 23 May 2023 04:20:24 GMT  
		Size: 114.7 MB (114688687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58f84aa8f52e3e23cf8f32852a4c4ce52d494dbfe37e874d6933b5c23f60d4d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d38afe56dd7904476cd5c55fa58f0f761fcf9cf258edffbb66d71d8240f481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:14 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:14 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:14 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9405ba3d07fb1648e429cb012b11fa1e9e0bc8f9e32cbb1ecc7a6336645a7`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43d5afb8207c802f6936e201f3e5fca058072eddcd1ec7a81612cdcb274e54`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc2a4561d824a9a0379e832a6bef3a66e3dee4a9b6509d9cee328294b4b8ca`  
		Last Modified: Tue, 23 May 2023 07:58:24 GMT  
		Size: 114.5 MB (114544975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:b156f6aa61bcc78b160f509e3c8dc756d6e41c534c1b5a63197f36f0b5cbf4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e89709d490cfe4ad4f7a49e9690a1d4397b18f251acf68f8b6f4f0e847f84032
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b1df17c9a9394414568590a6e11207fe6489768a304faa439ed658aab1f353`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:19:00 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:19:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:19:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:19:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:19:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:19:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:19:18 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:19:18 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:19:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:19:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5011326b12928bcd6584016f6aea605e8a53b9a1d6ac9a647ce032b78f52fad`  
		Last Modified: Tue, 23 May 2023 04:20:50 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52b348a8efca0e9ac27d6a133a3ac8ae18412cac16ac1971201175e18477aee`  
		Last Modified: Tue, 23 May 2023 04:20:49 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61c95b5adb6f2b7ba27e4fd29866e1a9e6af175a955727d5983fa7352d7e09a`  
		Last Modified: Tue, 23 May 2023 04:21:04 GMT  
		Size: 379.7 MB (379683148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:32ded246aadeb8ee061ec50663e26a4444eba7507a4df582d56ca3d26b955cd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0875faf7fcdd75294a86408d7d195d3c6b686d627662ea5ddeefc6a0595974b5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:17 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:35 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:35 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815452b64991cc8961cb048ef3e1bedd694c39634170adf9a67b672e7a31cd02`  
		Last Modified: Tue, 23 May 2023 07:58:43 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55dc57c3622b773ea70563455a583cc5e7ea3aeea05840c1fb6fc392f211ae3`  
		Last Modified: Tue, 23 May 2023 07:58:43 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ccd16d771409a85e60a6eb41535438c1a0571d753537819e4c25b2cb31eb48`  
		Last Modified: Tue, 23 May 2023 07:58:56 GMT  
		Size: 379.5 MB (379541292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:7ea588795119ec4895bc2ee241bc1bb0babb91f745aa79c3abff217553516c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:3546a3130e80a51d420e7a07e925aa6465d2af87b77add87cb35f43c7a14caeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7856754509efc0504255ca580c2f4308504989facbbc2f883e5be0eb8553b71a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 04:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 04:18:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 04:18:42 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 04:18:42 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 04:18:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 04:18:54 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 04:18:54 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 04:18:54 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 04:18:54 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 04:18:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 04:18:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0787c8d764ee0036e5e76c521001f9628f82954d6c48640bdcc21b5242c109b`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f729f64977b963f46455a8c8eac4f2d66517b11d7bfc809833c1ded8562aef`  
		Last Modified: Tue, 23 May 2023 04:20:18 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73577e5c94088cfb6c46a1b5b7842a84de0cfa9f0a77db52f267a2effe3bc56b`  
		Last Modified: Tue, 23 May 2023 04:20:24 GMT  
		Size: 114.7 MB (114688687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:58f84aa8f52e3e23cf8f32852a4c4ce52d494dbfe37e874d6933b5c23f60d4d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d38afe56dd7904476cd5c55fa58f0f761fcf9cf258edffbb66d71d8240f481`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 01:29:51 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Tue, 23 May 2023 07:57:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 23 May 2023 07:57:01 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Tue, 23 May 2023 07:57:01 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 23 May 2023 07:57:01 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Tue, 23 May 2023 07:57:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:57:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:57:14 GMT
WORKDIR /var/lib/neo4j
# Tue, 23 May 2023 07:57:14 GMT
VOLUME [/data /logs]
# Tue, 23 May 2023 07:57:14 GMT
EXPOSE 7473 7474 7687
# Tue, 23 May 2023 07:57:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 23 May 2023 07:57:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04300dd851e66af00281d635f3fa075517249f6b42bf7ebe21fbbe2828ef53bd`  
		Last Modified: Tue, 23 May 2023 01:37:21 GMT  
		Size: 191.4 MB (191387691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f9405ba3d07fb1648e429cb012b11fa1e9e0bc8f9e32cbb1ecc7a6336645a7`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43d5afb8207c802f6936e201f3e5fca058072eddcd1ec7a81612cdcb274e54`  
		Last Modified: Tue, 23 May 2023 07:58:20 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bc2a4561d824a9a0379e832a6bef3a66e3dee4a9b6509d9cee328294b4b8ca`  
		Last Modified: Tue, 23 May 2023 07:58:24 GMT  
		Size: 114.5 MB (114544975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
