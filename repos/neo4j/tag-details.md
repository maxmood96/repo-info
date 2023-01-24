<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.3`](#neo4j43)
-	[`neo4j:4.3-community`](#neo4j43-community)
-	[`neo4j:4.3-enterprise`](#neo4j43-enterprise)
-	[`neo4j:4.3.23`](#neo4j4323)
-	[`neo4j:4.3.23-community`](#neo4j4323-community)
-	[`neo4j:4.3.23-enterprise`](#neo4j4323-enterprise)
-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.16`](#neo4j4416)
-	[`neo4j:4.4.16-community`](#neo4j4416-community)
-	[`neo4j:4.4.16-enterprise`](#neo4j4416-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5.3`](#neo4j53)
-	[`neo4j:5.3-enterprise`](#neo4j53-enterprise)
-	[`neo4j:5.3.0`](#neo4j530)
-	[`neo4j:5.3.0-community`](#neo4j530-community)
-	[`neo4j:5.3.0-enterprise`](#neo4j530-enterprise)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:latest`](#neo4jlatest)

## `neo4j:4.3`

```console
$ docker pull neo4j@sha256:cf11f25475ffe0822abf9c7f50fe2a1a11a192e3ddc086a878e43f9b38748e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3` - linux; amd64

```console
$ docker pull neo4j@sha256:62fad3ec429063de9b6e3d96730e05bf063c46df6d133d41b0582f242fb82a45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.9 MB (361911813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c293e3028d56fba7e7b7f5310095b5045bcf24826a96756fa9b9d3349e1ea0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f454b5e714e8444e0f601469d057bb9c730900f9027c82f7b07ef8a4c31f83da NEO4J_TARBALL=neo4j-community-4.3.23-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:27:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
# Wed, 11 Jan 2023 06:27:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:27:40 GMT
COPY multi:c237d33f8ae77693f461a49ebfa948d0245c97e750ef0e7e1c70bf8b956e1fed in /startup/ 
# Wed, 11 Jan 2023 06:27:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:53 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:53 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9186086f62f28047acafe35a8b8a1ce0b6e83963ea084d13b10e83f932341916`  
		Last Modified: Wed, 11 Jan 2023 06:30:04 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e87d8614888a8621133d301423614243984c0bb045d1a20299178bc1eae119`  
		Last Modified: Wed, 11 Jan 2023 06:30:04 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18b5bfd0b34da09d85f6b8d91c40cb99dfdc4464334b7ffa48aa58c92f02d2`  
		Last Modified: Wed, 11 Jan 2023 06:30:11 GMT  
		Size: 132.0 MB (132048802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-community`

```console
$ docker pull neo4j@sha256:cf11f25475ffe0822abf9c7f50fe2a1a11a192e3ddc086a878e43f9b38748e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-community` - linux; amd64

```console
$ docker pull neo4j@sha256:62fad3ec429063de9b6e3d96730e05bf063c46df6d133d41b0582f242fb82a45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.9 MB (361911813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c293e3028d56fba7e7b7f5310095b5045bcf24826a96756fa9b9d3349e1ea0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f454b5e714e8444e0f601469d057bb9c730900f9027c82f7b07ef8a4c31f83da NEO4J_TARBALL=neo4j-community-4.3.23-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:27:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
# Wed, 11 Jan 2023 06:27:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:27:40 GMT
COPY multi:c237d33f8ae77693f461a49ebfa948d0245c97e750ef0e7e1c70bf8b956e1fed in /startup/ 
# Wed, 11 Jan 2023 06:27:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:53 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:53 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9186086f62f28047acafe35a8b8a1ce0b6e83963ea084d13b10e83f932341916`  
		Last Modified: Wed, 11 Jan 2023 06:30:04 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e87d8614888a8621133d301423614243984c0bb045d1a20299178bc1eae119`  
		Last Modified: Wed, 11 Jan 2023 06:30:04 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18b5bfd0b34da09d85f6b8d91c40cb99dfdc4464334b7ffa48aa58c92f02d2`  
		Last Modified: Wed, 11 Jan 2023 06:30:11 GMT  
		Size: 132.0 MB (132048802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3-enterprise`

```console
$ docker pull neo4j@sha256:c3d12bc85137e02908a0f6b1f4ddadfa4092dd396baa2d58a3b19e6e65a0a69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:472593a10bb06587766c2668084aeb157eba5220bed7de08ff2f9eb461ee18f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.5 MB (392484421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50486bffc32d601b76ff867b3351014108b2c1e843c77925d0755569199cd767`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:27:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cde8ca90702604165c87e0f94e19e89d26d745f74043f8d6bf558b4b1626c5fa NEO4J_TARBALL=neo4j-enterprise-4.3.23-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:27:56 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.23-unix.tar.gz
# Wed, 11 Jan 2023 06:27:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.23-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:27:57 GMT
COPY multi:c237d33f8ae77693f461a49ebfa948d0245c97e750ef0e7e1c70bf8b956e1fed in /startup/ 
# Wed, 11 Jan 2023 06:28:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.23-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:28:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:28:10 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:28:10 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:28:10 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:28:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:28:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b0918b44a084e9b2f55dc08f14d74510808c014cbcb8cca29a0722678af327`  
		Last Modified: Wed, 11 Jan 2023 06:30:24 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e44688c1bfd6ccd4e18652fd6b1e0711a35dd410264909ca2d23afb977ca6e`  
		Last Modified: Wed, 11 Jan 2023 06:30:23 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a9465053f5da74858a6f47f0eaa561a0db178085c1b89f3a4c4e0a0b9af50`  
		Last Modified: Wed, 11 Jan 2023 06:30:32 GMT  
		Size: 162.6 MB (162621413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.23`

```console
$ docker pull neo4j@sha256:cf11f25475ffe0822abf9c7f50fe2a1a11a192e3ddc086a878e43f9b38748e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.23` - linux; amd64

```console
$ docker pull neo4j@sha256:62fad3ec429063de9b6e3d96730e05bf063c46df6d133d41b0582f242fb82a45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.9 MB (361911813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c293e3028d56fba7e7b7f5310095b5045bcf24826a96756fa9b9d3349e1ea0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f454b5e714e8444e0f601469d057bb9c730900f9027c82f7b07ef8a4c31f83da NEO4J_TARBALL=neo4j-community-4.3.23-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:27:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
# Wed, 11 Jan 2023 06:27:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:27:40 GMT
COPY multi:c237d33f8ae77693f461a49ebfa948d0245c97e750ef0e7e1c70bf8b956e1fed in /startup/ 
# Wed, 11 Jan 2023 06:27:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:53 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:53 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9186086f62f28047acafe35a8b8a1ce0b6e83963ea084d13b10e83f932341916`  
		Last Modified: Wed, 11 Jan 2023 06:30:04 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e87d8614888a8621133d301423614243984c0bb045d1a20299178bc1eae119`  
		Last Modified: Wed, 11 Jan 2023 06:30:04 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18b5bfd0b34da09d85f6b8d91c40cb99dfdc4464334b7ffa48aa58c92f02d2`  
		Last Modified: Wed, 11 Jan 2023 06:30:11 GMT  
		Size: 132.0 MB (132048802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.23-community`

```console
$ docker pull neo4j@sha256:cf11f25475ffe0822abf9c7f50fe2a1a11a192e3ddc086a878e43f9b38748e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.23-community` - linux; amd64

```console
$ docker pull neo4j@sha256:62fad3ec429063de9b6e3d96730e05bf063c46df6d133d41b0582f242fb82a45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.9 MB (361911813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c293e3028d56fba7e7b7f5310095b5045bcf24826a96756fa9b9d3349e1ea0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f454b5e714e8444e0f601469d057bb9c730900f9027c82f7b07ef8a4c31f83da NEO4J_TARBALL=neo4j-community-4.3.23-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:27:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
# Wed, 11 Jan 2023 06:27:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:27:40 GMT
COPY multi:c237d33f8ae77693f461a49ebfa948d0245c97e750ef0e7e1c70bf8b956e1fed in /startup/ 
# Wed, 11 Jan 2023 06:27:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.3.23-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:53 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:53 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:53 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9186086f62f28047acafe35a8b8a1ce0b6e83963ea084d13b10e83f932341916`  
		Last Modified: Wed, 11 Jan 2023 06:30:04 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e87d8614888a8621133d301423614243984c0bb045d1a20299178bc1eae119`  
		Last Modified: Wed, 11 Jan 2023 06:30:04 GMT  
		Size: 7.6 KB (7625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18b5bfd0b34da09d85f6b8d91c40cb99dfdc4464334b7ffa48aa58c92f02d2`  
		Last Modified: Wed, 11 Jan 2023 06:30:11 GMT  
		Size: 132.0 MB (132048802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.3.23-enterprise`

```console
$ docker pull neo4j@sha256:c3d12bc85137e02908a0f6b1f4ddadfa4092dd396baa2d58a3b19e6e65a0a69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `neo4j:4.3.23-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:472593a10bb06587766c2668084aeb157eba5220bed7de08ff2f9eb461ee18f7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.5 MB (392484421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50486bffc32d601b76ff867b3351014108b2c1e843c77925d0755569199cd767`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:27:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cde8ca90702604165c87e0f94e19e89d26d745f74043f8d6bf558b4b1626c5fa NEO4J_TARBALL=neo4j-enterprise-4.3.23-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:27:56 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.23-unix.tar.gz
# Wed, 11 Jan 2023 06:27:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.23-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:27:57 GMT
COPY multi:c237d33f8ae77693f461a49ebfa948d0245c97e750ef0e7e1c70bf8b956e1fed in /startup/ 
# Wed, 11 Jan 2023 06:28:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.3.23-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:28:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:28:10 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:28:10 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:28:10 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:28:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:28:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b0918b44a084e9b2f55dc08f14d74510808c014cbcb8cca29a0722678af327`  
		Last Modified: Wed, 11 Jan 2023 06:30:24 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e44688c1bfd6ccd4e18652fd6b1e0711a35dd410264909ca2d23afb977ca6e`  
		Last Modified: Wed, 11 Jan 2023 06:30:23 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a9465053f5da74858a6f47f0eaa561a0db178085c1b89f3a4c4e0a0b9af50`  
		Last Modified: Wed, 11 Jan 2023 06:30:32 GMT  
		Size: 162.6 MB (162621413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:5bc2e798a1846fed009e803dfee0395f96d274295daf708b928ded3c9ccf8598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:8bdefa6bb230c9644e836b981ff14974a5af9051e50c3317b6b60bb0dbd9b3e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366747236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16d430a91c259bed78cc50c88b1e6f77737b346e3a4550f8b4f3b47f438592a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e4ae513dc1a297dc2cbf4f07af5ced366038055385de9c9d598df1b4aceed91 NEO4J_TARBALL=neo4j-community-4.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
# Wed, 11 Jan 2023 06:26:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:56 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Wed, 11 Jan 2023 06:27:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:13 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:13 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:13 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c4b74cbdecd1a70a6883b46baca935725720406c8148ffff67cdf3bca8b03`  
		Last Modified: Wed, 11 Jan 2023 06:29:25 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e577986c4e68297fe879d26d8edc95d888209116ff35cf04c9d61b3b37b62`  
		Last Modified: Wed, 11 Jan 2023 06:29:25 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9992115395abf4e6141b21145db9b1818f94bd6510b226d75dbb0512da7c7d8b`  
		Last Modified: Wed, 11 Jan 2023 06:29:33 GMT  
		Size: 136.9 MB (136883680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8da5083a3f14e43acd769e664938116a73f38b31f88bd58e5746ea09e01471da
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362037380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3a125530376e46b806b5d3f5a7a7d1151dd8efcf4d1030185bac0c491db011`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 20:59:22 GMT
COPY dir:b5081ac7f31ec5da21215ff6126fdb71f9fa63a8c9b5dc5e3f45f611c1765726 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e4ae513dc1a297dc2cbf4f07af5ced366038055385de9c9d598df1b4aceed91 NEO4J_TARBALL=neo4j-community-4.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
# Tue, 24 Jan 2023 21:23:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:27 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Tue, 24 Jan 2023 21:23:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:23:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:42 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:42 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8fec50bc484d6341eb4f90d4749394a389a13ec00c2b3ab78c9140d9d4cda0`  
		Last Modified: Tue, 24 Jan 2023 21:11:01 GMT  
		Size: 195.2 MB (195239953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b52c77927d8d2e485192a8d752f867d8024b262943748c71854ecdd831b3b`  
		Last Modified: Tue, 24 Jan 2023 21:25:21 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b0cb9ba3614914e8bbd97d58661197655cbc02d0b99cd70fccf61dd1e76b7f`  
		Last Modified: Tue, 24 Jan 2023 21:25:21 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aabba8a30d8f3a58d58599d6f9643cd5fa04b27cec324e1acac4cce3dfea88e`  
		Last Modified: Tue, 24 Jan 2023 21:25:27 GMT  
		Size: 136.7 MB (136740555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:5bc2e798a1846fed009e803dfee0395f96d274295daf708b928ded3c9ccf8598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:8bdefa6bb230c9644e836b981ff14974a5af9051e50c3317b6b60bb0dbd9b3e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366747236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16d430a91c259bed78cc50c88b1e6f77737b346e3a4550f8b4f3b47f438592a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e4ae513dc1a297dc2cbf4f07af5ced366038055385de9c9d598df1b4aceed91 NEO4J_TARBALL=neo4j-community-4.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
# Wed, 11 Jan 2023 06:26:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:56 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Wed, 11 Jan 2023 06:27:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:13 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:13 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:13 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c4b74cbdecd1a70a6883b46baca935725720406c8148ffff67cdf3bca8b03`  
		Last Modified: Wed, 11 Jan 2023 06:29:25 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e577986c4e68297fe879d26d8edc95d888209116ff35cf04c9d61b3b37b62`  
		Last Modified: Wed, 11 Jan 2023 06:29:25 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9992115395abf4e6141b21145db9b1818f94bd6510b226d75dbb0512da7c7d8b`  
		Last Modified: Wed, 11 Jan 2023 06:29:33 GMT  
		Size: 136.9 MB (136883680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8da5083a3f14e43acd769e664938116a73f38b31f88bd58e5746ea09e01471da
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362037380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3a125530376e46b806b5d3f5a7a7d1151dd8efcf4d1030185bac0c491db011`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 20:59:22 GMT
COPY dir:b5081ac7f31ec5da21215ff6126fdb71f9fa63a8c9b5dc5e3f45f611c1765726 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e4ae513dc1a297dc2cbf4f07af5ced366038055385de9c9d598df1b4aceed91 NEO4J_TARBALL=neo4j-community-4.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
# Tue, 24 Jan 2023 21:23:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:27 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Tue, 24 Jan 2023 21:23:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:23:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:42 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:42 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8fec50bc484d6341eb4f90d4749394a389a13ec00c2b3ab78c9140d9d4cda0`  
		Last Modified: Tue, 24 Jan 2023 21:11:01 GMT  
		Size: 195.2 MB (195239953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b52c77927d8d2e485192a8d752f867d8024b262943748c71854ecdd831b3b`  
		Last Modified: Tue, 24 Jan 2023 21:25:21 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b0cb9ba3614914e8bbd97d58661197655cbc02d0b99cd70fccf61dd1e76b7f`  
		Last Modified: Tue, 24 Jan 2023 21:25:21 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aabba8a30d8f3a58d58599d6f9643cd5fa04b27cec324e1acac4cce3dfea88e`  
		Last Modified: Tue, 24 Jan 2023 21:25:27 GMT  
		Size: 136.7 MB (136740555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:e499ea6e75a0e65df1b5f43b9b41449615213caf95ff7fe08974c308d21d6761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9c06edd20fb92d5d197ae7960cbc2e2dcc52c7e28be0be792434ecfa163afc38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.1 MB (463074013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d946b51782ad6820075aada9404ab570b03c8c7639d0ba1f9975d70d584dad7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:27:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c4db0c4625e4c56a74140560601524bd6dd44e00de9b61b6c23cda71aaaf18c3 NEO4J_TARBALL=neo4j-enterprise-4.4.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:27:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
# Wed, 11 Jan 2023 06:27:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:27:20 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Wed, 11 Jan 2023 06:27:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:36 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:36 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:36 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017113cfefd12d87ff2f2d2b950e00fad35695069a11eb65c768d18c7aa74d9f`  
		Last Modified: Wed, 11 Jan 2023 06:29:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12352dd08ce3ae37dfc8a189740ae058623fb91a2a914e3b1d428fa40496c002`  
		Last Modified: Wed, 11 Jan 2023 06:29:45 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc6417895030577a80a4bdd50432a11eb630b2f178d26183405ea023c605ea`  
		Last Modified: Wed, 11 Jan 2023 06:29:56 GMT  
		Size: 233.2 MB (233210455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:51d2d753a1f45e26281bdc355f10a668db8a26acfb731e96e94e8dec3ccfd3d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.4 MB (458364158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48f2301f51e0c1f2ac87f64e24d9556c0624dd208caf06ac94495f118a7a48e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 20:59:22 GMT
COPY dir:b5081ac7f31ec5da21215ff6126fdb71f9fa63a8c9b5dc5e3f45f611c1765726 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c4db0c4625e4c56a74140560601524bd6dd44e00de9b61b6c23cda71aaaf18c3 NEO4J_TARBALL=neo4j-enterprise-4.4.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
# Tue, 24 Jan 2023 21:23:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:47 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Tue, 24 Jan 2023 21:24:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:24:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:24:08 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:24:08 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:24:08 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:24:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:24:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8fec50bc484d6341eb4f90d4749394a389a13ec00c2b3ab78c9140d9d4cda0`  
		Last Modified: Tue, 24 Jan 2023 21:11:01 GMT  
		Size: 195.2 MB (195239953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bf483f53dbf1548e92dcc5790c02a84724ff0c256c4ca5a3949d562c28656b`  
		Last Modified: Tue, 24 Jan 2023 21:25:39 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de0a2069d0c0481d1bdc6839a70cefc1d063cd2ec5d548ca666e7736172319d`  
		Last Modified: Tue, 24 Jan 2023 21:25:39 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1602de26e151043b7887f949b827eff8c4c1a3f657da8901942ee931b17c35b1`  
		Last Modified: Tue, 24 Jan 2023 21:25:49 GMT  
		Size: 233.1 MB (233067332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.16`

```console
$ docker pull neo4j@sha256:5bc2e798a1846fed009e803dfee0395f96d274295daf708b928ded3c9ccf8598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.16` - linux; amd64

```console
$ docker pull neo4j@sha256:8bdefa6bb230c9644e836b981ff14974a5af9051e50c3317b6b60bb0dbd9b3e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366747236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16d430a91c259bed78cc50c88b1e6f77737b346e3a4550f8b4f3b47f438592a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e4ae513dc1a297dc2cbf4f07af5ced366038055385de9c9d598df1b4aceed91 NEO4J_TARBALL=neo4j-community-4.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
# Wed, 11 Jan 2023 06:26:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:56 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Wed, 11 Jan 2023 06:27:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:13 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:13 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:13 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c4b74cbdecd1a70a6883b46baca935725720406c8148ffff67cdf3bca8b03`  
		Last Modified: Wed, 11 Jan 2023 06:29:25 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e577986c4e68297fe879d26d8edc95d888209116ff35cf04c9d61b3b37b62`  
		Last Modified: Wed, 11 Jan 2023 06:29:25 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9992115395abf4e6141b21145db9b1818f94bd6510b226d75dbb0512da7c7d8b`  
		Last Modified: Wed, 11 Jan 2023 06:29:33 GMT  
		Size: 136.9 MB (136883680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.16` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8da5083a3f14e43acd769e664938116a73f38b31f88bd58e5746ea09e01471da
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362037380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3a125530376e46b806b5d3f5a7a7d1151dd8efcf4d1030185bac0c491db011`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 20:59:22 GMT
COPY dir:b5081ac7f31ec5da21215ff6126fdb71f9fa63a8c9b5dc5e3f45f611c1765726 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e4ae513dc1a297dc2cbf4f07af5ced366038055385de9c9d598df1b4aceed91 NEO4J_TARBALL=neo4j-community-4.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
# Tue, 24 Jan 2023 21:23:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:27 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Tue, 24 Jan 2023 21:23:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:23:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:42 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:42 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8fec50bc484d6341eb4f90d4749394a389a13ec00c2b3ab78c9140d9d4cda0`  
		Last Modified: Tue, 24 Jan 2023 21:11:01 GMT  
		Size: 195.2 MB (195239953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b52c77927d8d2e485192a8d752f867d8024b262943748c71854ecdd831b3b`  
		Last Modified: Tue, 24 Jan 2023 21:25:21 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b0cb9ba3614914e8bbd97d58661197655cbc02d0b99cd70fccf61dd1e76b7f`  
		Last Modified: Tue, 24 Jan 2023 21:25:21 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aabba8a30d8f3a58d58599d6f9643cd5fa04b27cec324e1acac4cce3dfea88e`  
		Last Modified: Tue, 24 Jan 2023 21:25:27 GMT  
		Size: 136.7 MB (136740555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.16-community`

```console
$ docker pull neo4j@sha256:5bc2e798a1846fed009e803dfee0395f96d274295daf708b928ded3c9ccf8598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.16-community` - linux; amd64

```console
$ docker pull neo4j@sha256:8bdefa6bb230c9644e836b981ff14974a5af9051e50c3317b6b60bb0dbd9b3e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366747236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16d430a91c259bed78cc50c88b1e6f77737b346e3a4550f8b4f3b47f438592a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e4ae513dc1a297dc2cbf4f07af5ced366038055385de9c9d598df1b4aceed91 NEO4J_TARBALL=neo4j-community-4.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
# Wed, 11 Jan 2023 06:26:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:56 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Wed, 11 Jan 2023 06:27:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:13 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:13 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:13 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c4b74cbdecd1a70a6883b46baca935725720406c8148ffff67cdf3bca8b03`  
		Last Modified: Wed, 11 Jan 2023 06:29:25 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55e577986c4e68297fe879d26d8edc95d888209116ff35cf04c9d61b3b37b62`  
		Last Modified: Wed, 11 Jan 2023 06:29:25 GMT  
		Size: 8.2 KB (8170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9992115395abf4e6141b21145db9b1818f94bd6510b226d75dbb0512da7c7d8b`  
		Last Modified: Wed, 11 Jan 2023 06:29:33 GMT  
		Size: 136.9 MB (136883680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.16-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8da5083a3f14e43acd769e664938116a73f38b31f88bd58e5746ea09e01471da
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.0 MB (362037380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3a125530376e46b806b5d3f5a7a7d1151dd8efcf4d1030185bac0c491db011`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 20:59:22 GMT
COPY dir:b5081ac7f31ec5da21215ff6126fdb71f9fa63a8c9b5dc5e3f45f611c1765726 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9e4ae513dc1a297dc2cbf4f07af5ced366038055385de9c9d598df1b4aceed91 NEO4J_TARBALL=neo4j-community-4.4.16-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:26 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
# Tue, 24 Jan 2023 21:23:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:27 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Tue, 24 Jan 2023 21:23:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:23:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:42 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:42 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:42 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:42 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:42 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8fec50bc484d6341eb4f90d4749394a389a13ec00c2b3ab78c9140d9d4cda0`  
		Last Modified: Tue, 24 Jan 2023 21:11:01 GMT  
		Size: 195.2 MB (195239953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b52c77927d8d2e485192a8d752f867d8024b262943748c71854ecdd831b3b`  
		Last Modified: Tue, 24 Jan 2023 21:25:21 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b0cb9ba3614914e8bbd97d58661197655cbc02d0b99cd70fccf61dd1e76b7f`  
		Last Modified: Tue, 24 Jan 2023 21:25:21 GMT  
		Size: 8.2 KB (8169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aabba8a30d8f3a58d58599d6f9643cd5fa04b27cec324e1acac4cce3dfea88e`  
		Last Modified: Tue, 24 Jan 2023 21:25:27 GMT  
		Size: 136.7 MB (136740555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.16-enterprise`

```console
$ docker pull neo4j@sha256:e499ea6e75a0e65df1b5f43b9b41449615213caf95ff7fe08974c308d21d6761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.16-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9c06edd20fb92d5d197ae7960cbc2e2dcc52c7e28be0be792434ecfa163afc38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.1 MB (463074013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d946b51782ad6820075aada9404ab570b03c8c7639d0ba1f9975d70d584dad7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:23:09 GMT
COPY dir:a503569ef9354f7d11d0273f2ab0ff91f3e5c47f548dc54f07c58e44ff27a8a0 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:27:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c4db0c4625e4c56a74140560601524bd6dd44e00de9b61b6c23cda71aaaf18c3 NEO4J_TARBALL=neo4j-enterprise-4.4.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:27:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
# Wed, 11 Jan 2023 06:27:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:27:20 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Wed, 11 Jan 2023 06:27:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:27:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:27:36 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:27:36 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:27:36 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:27:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:27:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6154d41a3f1328e19471ffc2c51bb92391c00f8d743c0e0d90ec13704d92355f`  
		Last Modified: Wed, 11 Jan 2023 03:36:43 GMT  
		Size: 198.5 MB (198454554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017113cfefd12d87ff2f2d2b950e00fad35695069a11eb65c768d18c7aa74d9f`  
		Last Modified: Wed, 11 Jan 2023 06:29:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12352dd08ce3ae37dfc8a189740ae058623fb91a2a914e3b1d428fa40496c002`  
		Last Modified: Wed, 11 Jan 2023 06:29:45 GMT  
		Size: 8.2 KB (8173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc6417895030577a80a4bdd50432a11eb630b2f178d26183405ea023c605ea`  
		Last Modified: Wed, 11 Jan 2023 06:29:56 GMT  
		Size: 233.2 MB (233210455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.16-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:51d2d753a1f45e26281bdc355f10a668db8a26acfb731e96e94e8dec3ccfd3d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.4 MB (458364158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48f2301f51e0c1f2ac87f64e24d9556c0624dd208caf06ac94495f118a7a48e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 20:59:22 GMT
COPY dir:b5081ac7f31ec5da21215ff6126fdb71f9fa63a8c9b5dc5e3f45f611c1765726 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=c4db0c4625e4c56a74140560601524bd6dd44e00de9b61b6c23cda71aaaf18c3 NEO4J_TARBALL=neo4j-enterprise-4.4.16-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
# Tue, 24 Jan 2023 21:23:47 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:47 GMT
COPY multi:bcdd0bea98c64e6ecaf1a248e9edc31123c2bb38e4099e0a080dab2e2d5a11a8 in /startup/ 
# Tue, 24 Jan 2023 21:24:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.16-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:24:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:24:08 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:24:08 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:24:08 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:24:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:24:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8fec50bc484d6341eb4f90d4749394a389a13ec00c2b3ab78c9140d9d4cda0`  
		Last Modified: Tue, 24 Jan 2023 21:11:01 GMT  
		Size: 195.2 MB (195239953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bf483f53dbf1548e92dcc5790c02a84724ff0c256c4ca5a3949d562c28656b`  
		Last Modified: Tue, 24 Jan 2023 21:25:39 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de0a2069d0c0481d1bdc6839a70cefc1d063cd2ec5d548ca666e7736172319d`  
		Last Modified: Tue, 24 Jan 2023 21:25:39 GMT  
		Size: 8.2 KB (8171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1602de26e151043b7887f949b827eff8c4c1a3f657da8901942ee931b17c35b1`  
		Last Modified: Tue, 24 Jan 2023 21:25:49 GMT  
		Size: 233.1 MB (233067332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:093b7dc7c74f6308dc5897ba8a3ca6f58da1d3cba8be55eb87f241a5da8c5185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:90bb7986b729997c0324b0033e2f47525c146a2eeec3841bcb91456cf268dbc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2274885f564bf979c6734fcbc64264d1c649ebf5c352ca1868458ffd8112ea8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:19 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:32 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:32 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413a32157313eeefe235570facba73aa3f3a27a3c673e299eb00e57a8dec08c`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c991a7f1285dc4b8840490a1ff30b5a16b08170a263b11005ee70be05816025`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba1a46d62a9b8f7a123ca1970cc7b116ec025cbd33c75849b110d1eadc001d`  
		Last Modified: Wed, 11 Jan 2023 06:28:45 GMT  
		Size: 114.6 MB (114606322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8b8a29d13efb2898698633a68bf0fd63b1664d5cf6ce8788da0dec0a56e438a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335781526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fc1c011e072ed217b30eac2a97fd6558a2c8a2c8af7f516c2212836e0321ca`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:22:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:22:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:22:49 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:22:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:22:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:00 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:00 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:00 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bfcbe1990bf40a44f1d6e9d0db53067dd92c968a0d6b488295d8441057b4f`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c08ec1f03ee4c2797e19dc16bc9b6452159eadf5eb22913cb7b338088ce2f3`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6ca0015d37331c71114de6a4f4f0cd44527a5cf5bdde1f4de2d24f92ac1243`  
		Last Modified: Tue, 24 Jan 2023 21:24:40 GMT  
		Size: 114.5 MB (114464057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:093b7dc7c74f6308dc5897ba8a3ca6f58da1d3cba8be55eb87f241a5da8c5185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:90bb7986b729997c0324b0033e2f47525c146a2eeec3841bcb91456cf268dbc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2274885f564bf979c6734fcbc64264d1c649ebf5c352ca1868458ffd8112ea8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:19 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:32 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:32 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413a32157313eeefe235570facba73aa3f3a27a3c673e299eb00e57a8dec08c`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c991a7f1285dc4b8840490a1ff30b5a16b08170a263b11005ee70be05816025`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba1a46d62a9b8f7a123ca1970cc7b116ec025cbd33c75849b110d1eadc001d`  
		Last Modified: Wed, 11 Jan 2023 06:28:45 GMT  
		Size: 114.6 MB (114606322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8b8a29d13efb2898698633a68bf0fd63b1664d5cf6ce8788da0dec0a56e438a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335781526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fc1c011e072ed217b30eac2a97fd6558a2c8a2c8af7f516c2212836e0321ca`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:22:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:22:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:22:49 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:22:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:22:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:00 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:00 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:00 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bfcbe1990bf40a44f1d6e9d0db53067dd92c968a0d6b488295d8441057b4f`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c08ec1f03ee4c2797e19dc16bc9b6452159eadf5eb22913cb7b338088ce2f3`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6ca0015d37331c71114de6a4f4f0cd44527a5cf5bdde1f4de2d24f92ac1243`  
		Last Modified: Tue, 24 Jan 2023 21:24:40 GMT  
		Size: 114.5 MB (114464057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:aa30426c25409e91c2ed5d2492cb60bbb6674b9090eb7491cd90c189328fe0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:40d43a47ecfe1dbfd0c97fbf5ead7dc6cfc205c64f3e257002d183019ac0bb75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434823786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0959909995b7d31b1f06a274ee0ff4b3d05fcf75d995276b90307720bbad10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:36 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:51 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:51 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:51 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a457411e2e9f04e93beb9cb89e47fa4ca50663983a94c8fcdc65db42e6d7f3d4`  
		Last Modified: Wed, 11 Jan 2023 06:29:02 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7741924512acec613969b2083e8559ee6d89acfae26f99713c9d299bc340b`  
		Last Modified: Wed, 11 Jan 2023 06:29:02 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b503f28b2f71af7a4d51e051eb390a314227b7060e3d6bb736e25237b15815b`  
		Last Modified: Wed, 11 Jan 2023 06:29:13 GMT  
		Size: 211.0 MB (210983347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c6f29915dd5e1193250456f99c47134815b11b808fe4d320d4abea0feb76470
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.2 MB (432157224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8552e96337ffc96af019ba7bd8bdf228f35c05335889a24dec35020d97125dee`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:23:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:03 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:23:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:23:23 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:23 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:23 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:23 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de495238dbcd8e4b231e9337720573937f5b42ae43adee3827c0372430c3b8af`  
		Last Modified: Tue, 24 Jan 2023 21:25:00 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c4da9899170dfe57534f70387fd0ebdba1d8d76a7f7cf86ffb63ab13bc5df0`  
		Last Modified: Tue, 24 Jan 2023 21:25:00 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa03c45a752aa67f7d960c8b4b09ac3eef60007132e5efeea3679b7988f108f3`  
		Last Modified: Tue, 24 Jan 2023 21:25:08 GMT  
		Size: 210.8 MB (210839749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.3`

```console
$ docker pull neo4j@sha256:093b7dc7c74f6308dc5897ba8a3ca6f58da1d3cba8be55eb87f241a5da8c5185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3` - linux; amd64

```console
$ docker pull neo4j@sha256:90bb7986b729997c0324b0033e2f47525c146a2eeec3841bcb91456cf268dbc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2274885f564bf979c6734fcbc64264d1c649ebf5c352ca1868458ffd8112ea8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:19 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:32 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:32 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413a32157313eeefe235570facba73aa3f3a27a3c673e299eb00e57a8dec08c`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c991a7f1285dc4b8840490a1ff30b5a16b08170a263b11005ee70be05816025`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba1a46d62a9b8f7a123ca1970cc7b116ec025cbd33c75849b110d1eadc001d`  
		Last Modified: Wed, 11 Jan 2023 06:28:45 GMT  
		Size: 114.6 MB (114606322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8b8a29d13efb2898698633a68bf0fd63b1664d5cf6ce8788da0dec0a56e438a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335781526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fc1c011e072ed217b30eac2a97fd6558a2c8a2c8af7f516c2212836e0321ca`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:22:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:22:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:22:49 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:22:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:22:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:00 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:00 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:00 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bfcbe1990bf40a44f1d6e9d0db53067dd92c968a0d6b488295d8441057b4f`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c08ec1f03ee4c2797e19dc16bc9b6452159eadf5eb22913cb7b338088ce2f3`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6ca0015d37331c71114de6a4f4f0cd44527a5cf5bdde1f4de2d24f92ac1243`  
		Last Modified: Tue, 24 Jan 2023 21:24:40 GMT  
		Size: 114.5 MB (114464057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.3-enterprise`

```console
$ docker pull neo4j@sha256:aa30426c25409e91c2ed5d2492cb60bbb6674b9090eb7491cd90c189328fe0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:40d43a47ecfe1dbfd0c97fbf5ead7dc6cfc205c64f3e257002d183019ac0bb75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434823786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0959909995b7d31b1f06a274ee0ff4b3d05fcf75d995276b90307720bbad10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:36 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:51 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:51 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:51 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a457411e2e9f04e93beb9cb89e47fa4ca50663983a94c8fcdc65db42e6d7f3d4`  
		Last Modified: Wed, 11 Jan 2023 06:29:02 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7741924512acec613969b2083e8559ee6d89acfae26f99713c9d299bc340b`  
		Last Modified: Wed, 11 Jan 2023 06:29:02 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b503f28b2f71af7a4d51e051eb390a314227b7060e3d6bb736e25237b15815b`  
		Last Modified: Wed, 11 Jan 2023 06:29:13 GMT  
		Size: 211.0 MB (210983347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c6f29915dd5e1193250456f99c47134815b11b808fe4d320d4abea0feb76470
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.2 MB (432157224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8552e96337ffc96af019ba7bd8bdf228f35c05335889a24dec35020d97125dee`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:23:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:03 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:23:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:23:23 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:23 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:23 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:23 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de495238dbcd8e4b231e9337720573937f5b42ae43adee3827c0372430c3b8af`  
		Last Modified: Tue, 24 Jan 2023 21:25:00 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c4da9899170dfe57534f70387fd0ebdba1d8d76a7f7cf86ffb63ab13bc5df0`  
		Last Modified: Tue, 24 Jan 2023 21:25:00 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa03c45a752aa67f7d960c8b4b09ac3eef60007132e5efeea3679b7988f108f3`  
		Last Modified: Tue, 24 Jan 2023 21:25:08 GMT  
		Size: 210.8 MB (210839749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.3.0`

```console
$ docker pull neo4j@sha256:093b7dc7c74f6308dc5897ba8a3ca6f58da1d3cba8be55eb87f241a5da8c5185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3.0` - linux; amd64

```console
$ docker pull neo4j@sha256:90bb7986b729997c0324b0033e2f47525c146a2eeec3841bcb91456cf268dbc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2274885f564bf979c6734fcbc64264d1c649ebf5c352ca1868458ffd8112ea8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:19 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:32 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:32 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413a32157313eeefe235570facba73aa3f3a27a3c673e299eb00e57a8dec08c`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c991a7f1285dc4b8840490a1ff30b5a16b08170a263b11005ee70be05816025`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba1a46d62a9b8f7a123ca1970cc7b116ec025cbd33c75849b110d1eadc001d`  
		Last Modified: Wed, 11 Jan 2023 06:28:45 GMT  
		Size: 114.6 MB (114606322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8b8a29d13efb2898698633a68bf0fd63b1664d5cf6ce8788da0dec0a56e438a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335781526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fc1c011e072ed217b30eac2a97fd6558a2c8a2c8af7f516c2212836e0321ca`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:22:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:22:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:22:49 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:22:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:22:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:00 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:00 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:00 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bfcbe1990bf40a44f1d6e9d0db53067dd92c968a0d6b488295d8441057b4f`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c08ec1f03ee4c2797e19dc16bc9b6452159eadf5eb22913cb7b338088ce2f3`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6ca0015d37331c71114de6a4f4f0cd44527a5cf5bdde1f4de2d24f92ac1243`  
		Last Modified: Tue, 24 Jan 2023 21:24:40 GMT  
		Size: 114.5 MB (114464057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.3.0-community`

```console
$ docker pull neo4j@sha256:093b7dc7c74f6308dc5897ba8a3ca6f58da1d3cba8be55eb87f241a5da8c5185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:90bb7986b729997c0324b0033e2f47525c146a2eeec3841bcb91456cf268dbc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2274885f564bf979c6734fcbc64264d1c649ebf5c352ca1868458ffd8112ea8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:19 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:32 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:32 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413a32157313eeefe235570facba73aa3f3a27a3c673e299eb00e57a8dec08c`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c991a7f1285dc4b8840490a1ff30b5a16b08170a263b11005ee70be05816025`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba1a46d62a9b8f7a123ca1970cc7b116ec025cbd33c75849b110d1eadc001d`  
		Last Modified: Wed, 11 Jan 2023 06:28:45 GMT  
		Size: 114.6 MB (114606322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8b8a29d13efb2898698633a68bf0fd63b1664d5cf6ce8788da0dec0a56e438a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335781526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fc1c011e072ed217b30eac2a97fd6558a2c8a2c8af7f516c2212836e0321ca`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:22:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:22:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:22:49 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:22:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:22:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:00 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:00 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:00 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bfcbe1990bf40a44f1d6e9d0db53067dd92c968a0d6b488295d8441057b4f`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c08ec1f03ee4c2797e19dc16bc9b6452159eadf5eb22913cb7b338088ce2f3`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6ca0015d37331c71114de6a4f4f0cd44527a5cf5bdde1f4de2d24f92ac1243`  
		Last Modified: Tue, 24 Jan 2023 21:24:40 GMT  
		Size: 114.5 MB (114464057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.3.0-enterprise`

```console
$ docker pull neo4j@sha256:aa30426c25409e91c2ed5d2492cb60bbb6674b9090eb7491cd90c189328fe0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.3.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:40d43a47ecfe1dbfd0c97fbf5ead7dc6cfc205c64f3e257002d183019ac0bb75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434823786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0959909995b7d31b1f06a274ee0ff4b3d05fcf75d995276b90307720bbad10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:36 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:51 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:51 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:51 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a457411e2e9f04e93beb9cb89e47fa4ca50663983a94c8fcdc65db42e6d7f3d4`  
		Last Modified: Wed, 11 Jan 2023 06:29:02 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7741924512acec613969b2083e8559ee6d89acfae26f99713c9d299bc340b`  
		Last Modified: Wed, 11 Jan 2023 06:29:02 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b503f28b2f71af7a4d51e051eb390a314227b7060e3d6bb736e25237b15815b`  
		Last Modified: Wed, 11 Jan 2023 06:29:13 GMT  
		Size: 211.0 MB (210983347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.3.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c6f29915dd5e1193250456f99c47134815b11b808fe4d320d4abea0feb76470
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.2 MB (432157224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8552e96337ffc96af019ba7bd8bdf228f35c05335889a24dec35020d97125dee`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:23:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:03 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:23:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:23:23 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:23 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:23 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:23 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de495238dbcd8e4b231e9337720573937f5b42ae43adee3827c0372430c3b8af`  
		Last Modified: Tue, 24 Jan 2023 21:25:00 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c4da9899170dfe57534f70387fd0ebdba1d8d76a7f7cf86ffb63ab13bc5df0`  
		Last Modified: Tue, 24 Jan 2023 21:25:00 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa03c45a752aa67f7d960c8b4b09ac3eef60007132e5efeea3679b7988f108f3`  
		Last Modified: Tue, 24 Jan 2023 21:25:08 GMT  
		Size: 210.8 MB (210839749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:093b7dc7c74f6308dc5897ba8a3ca6f58da1d3cba8be55eb87f241a5da8c5185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:90bb7986b729997c0324b0033e2f47525c146a2eeec3841bcb91456cf268dbc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2274885f564bf979c6734fcbc64264d1c649ebf5c352ca1868458ffd8112ea8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:19 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:32 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:32 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413a32157313eeefe235570facba73aa3f3a27a3c673e299eb00e57a8dec08c`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c991a7f1285dc4b8840490a1ff30b5a16b08170a263b11005ee70be05816025`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba1a46d62a9b8f7a123ca1970cc7b116ec025cbd33c75849b110d1eadc001d`  
		Last Modified: Wed, 11 Jan 2023 06:28:45 GMT  
		Size: 114.6 MB (114606322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8b8a29d13efb2898698633a68bf0fd63b1664d5cf6ce8788da0dec0a56e438a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335781526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fc1c011e072ed217b30eac2a97fd6558a2c8a2c8af7f516c2212836e0321ca`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:22:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:22:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:22:49 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:22:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:22:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:00 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:00 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:00 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bfcbe1990bf40a44f1d6e9d0db53067dd92c968a0d6b488295d8441057b4f`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c08ec1f03ee4c2797e19dc16bc9b6452159eadf5eb22913cb7b338088ce2f3`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6ca0015d37331c71114de6a4f4f0cd44527a5cf5bdde1f4de2d24f92ac1243`  
		Last Modified: Tue, 24 Jan 2023 21:24:40 GMT  
		Size: 114.5 MB (114464057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:aa30426c25409e91c2ed5d2492cb60bbb6674b9090eb7491cd90c189328fe0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:40d43a47ecfe1dbfd0c97fbf5ead7dc6cfc205c64f3e257002d183019ac0bb75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434823786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0959909995b7d31b1f06a274ee0ff4b3d05fcf75d995276b90307720bbad10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:36 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:51 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:51 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:51 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a457411e2e9f04e93beb9cb89e47fa4ca50663983a94c8fcdc65db42e6d7f3d4`  
		Last Modified: Wed, 11 Jan 2023 06:29:02 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b7741924512acec613969b2083e8559ee6d89acfae26f99713c9d299bc340b`  
		Last Modified: Wed, 11 Jan 2023 06:29:02 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b503f28b2f71af7a4d51e051eb390a314227b7060e3d6bb736e25237b15815b`  
		Last Modified: Wed, 11 Jan 2023 06:29:13 GMT  
		Size: 211.0 MB (210983347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4c6f29915dd5e1193250456f99c47134815b11b808fe4d320d4abea0feb76470
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.2 MB (432157224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8552e96337ffc96af019ba7bd8bdf228f35c05335889a24dec35020d97125dee`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:23:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=078aaf4da22ed43eae8164d8446b52c6d3751476db9000b83daa163dcf634bc2 NEO4J_TARBALL=neo4j-enterprise-5.3.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:23:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:23:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:23:03 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:23:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:23:23 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:23 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:23 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:23 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:23 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:23 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de495238dbcd8e4b231e9337720573937f5b42ae43adee3827c0372430c3b8af`  
		Last Modified: Tue, 24 Jan 2023 21:25:00 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c4da9899170dfe57534f70387fd0ebdba1d8d76a7f7cf86ffb63ab13bc5df0`  
		Last Modified: Tue, 24 Jan 2023 21:25:00 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa03c45a752aa67f7d960c8b4b09ac3eef60007132e5efeea3679b7988f108f3`  
		Last Modified: Tue, 24 Jan 2023 21:25:08 GMT  
		Size: 210.8 MB (210839749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:093b7dc7c74f6308dc5897ba8a3ca6f58da1d3cba8be55eb87f241a5da8c5185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:90bb7986b729997c0324b0033e2f47525c146a2eeec3841bcb91456cf268dbc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338446754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2274885f564bf979c6734fcbc64264d1c649ebf5c352ca1868458ffd8112ea8a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:20:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Jan 2023 03:26:17 GMT
COPY dir:6d447c71fb5cab25c46568db16879377c790ade488ebb14a9cc6935f6b8bd709 in /opt/java/openjdk 
# Wed, 11 Jan 2023 06:26:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 11 Jan 2023 06:26:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Wed, 11 Jan 2023 06:26:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Wed, 11 Jan 2023 06:26:19 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Wed, 11 Jan 2023 06:26:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:26:32 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Jan 2023 06:26:32 GMT
WORKDIR /var/lib/neo4j
# Wed, 11 Jan 2023 06:26:32 GMT
VOLUME [/data /logs]
# Wed, 11 Jan 2023 06:26:32 GMT
EXPOSE 7473 7474 7687
# Wed, 11 Jan 2023 06:26:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 06:26:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d96920cde608b8c4fa7937cb3a26411ad5c2a11f9476a38a3695c1d8ad93cd3`  
		Last Modified: Wed, 11 Jan 2023 03:38:36 GMT  
		Size: 192.4 MB (192431265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413a32157313eeefe235570facba73aa3f3a27a3c673e299eb00e57a8dec08c`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c991a7f1285dc4b8840490a1ff30b5a16b08170a263b11005ee70be05816025`  
		Last Modified: Wed, 11 Jan 2023 06:28:39 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba1a46d62a9b8f7a123ca1970cc7b116ec025cbd33c75849b110d1eadc001d`  
		Last Modified: Wed, 11 Jan 2023 06:28:45 GMT  
		Size: 114.6 MB (114606322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8b8a29d13efb2898698633a68bf0fd63b1664d5cf6ce8788da0dec0a56e438a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335781526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fc1c011e072ed217b30eac2a97fd6558a2c8a2c8af7f516c2212836e0321ca`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:38:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Jan 2023 21:04:04 GMT
COPY dir:6138ae24df63cd8b909473221414960a006ae73d2e2f1e88f48051984c7a0e00 in /opt/java/openjdk 
# Tue, 24 Jan 2023 21:22:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b20a3f253c42faccd1d2c37f9cc8bf6d557f0e645dced39e163da5ae12bb8d0a NEO4J_TARBALL=neo4j-community-5.3.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 24 Jan 2023 21:22:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
# Tue, 24 Jan 2023 21:22:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 24 Jan 2023 21:22:49 GMT
COPY multi:81f46e88e454671d24b1557a3a4cbb35163739c6808b91d7f90db70483d2b6ac in /startup/ 
# Tue, 24 Jan 2023 21:22:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.3.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 21:22:59 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Jan 2023 21:23:00 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Jan 2023 21:23:00 GMT
VOLUME [/data /logs]
# Tue, 24 Jan 2023 21:23:00 GMT
EXPOSE 7473 7474 7687
# Tue, 24 Jan 2023 21:23:00 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Jan 2023 21:23:00 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35e12b4b859554fa3c720b691ca2e6d60e7e2e24c6332157caccf058052ab7`  
		Last Modified: Tue, 24 Jan 2023 21:14:03 GMT  
		Size: 191.3 MB (191260429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bfcbe1990bf40a44f1d6e9d0db53067dd92c968a0d6b488295d8441057b4f`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 3.9 KB (3890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c08ec1f03ee4c2797e19dc16bc9b6452159eadf5eb22913cb7b338088ce2f3`  
		Last Modified: Tue, 24 Jan 2023 21:24:34 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6ca0015d37331c71114de6a4f4f0cd44527a5cf5bdde1f4de2d24f92ac1243`  
		Last Modified: Tue, 24 Jan 2023 21:24:40 GMT  
		Size: 114.5 MB (114464057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
