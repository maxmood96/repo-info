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
$ docker pull neo4j@sha256:6fdc57dab05c4eacb3fa9eb45b2b3944f5e6245391a29dd425d712c619ace055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:3c1bc38b2ee107cfee02c25dbbfbf1d9d8da9f5d4039970cdecb44c123159832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349352723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22a33d77dddc481fba99555a4e7f6f151baafe444ff2d1a93cde7e2fbc8ae42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Fri, 05 May 2023 18:40:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:40:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:40:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:41:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:41:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:41:09 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:41:09 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:41:10 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:41:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:41:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdea0e5018e1e8cc2b331e1ed2c4f1da84af25221910a1de76e337fce3f545`  
		Last Modified: Fri, 05 May 2023 18:41:45 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f595bfbecb37e114df202f90bab7195189bef04dda60cbede4979c09d3ba64b`  
		Last Modified: Fri, 05 May 2023 18:41:45 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a776250046198e86aba4237e6d8b9c415cbf67db951ceb13f5178ab58e805fb7`  
		Last Modified: Fri, 05 May 2023 18:41:51 GMT  
		Size: 119.4 MB (119387138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d40881fe3ef39538595f3f453d57d7ebea09a143e5d3df1907bf4b684921e1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344633450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe233903eaead3cbcb38fe3cac6c52ea831042611b133da2323a8add4015b81c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Fri, 05 May 2023 18:54:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:54:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:54:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:54:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:55:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:55:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:55:04 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:55:05 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:55:05 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:55:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:55:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa3476c1a9b5d9dca9b0f0758094b3ac19d32c73b84d54aff3fac3c7bec504`  
		Last Modified: Fri, 05 May 2023 18:55:37 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5cfa49c626a3633555164de938e107b78241081aac16df792096779feb2efb`  
		Last Modified: Fri, 05 May 2023 18:55:37 GMT  
		Size: 8.7 KB (8704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f9cbbfae074869c2dee87914fd1be657a8e842fd8bc1823fe4e87ea5bb195`  
		Last Modified: Fri, 05 May 2023 18:55:42 GMT  
		Size: 119.2 MB (119243920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:6fdc57dab05c4eacb3fa9eb45b2b3944f5e6245391a29dd425d712c619ace055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3c1bc38b2ee107cfee02c25dbbfbf1d9d8da9f5d4039970cdecb44c123159832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349352723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22a33d77dddc481fba99555a4e7f6f151baafe444ff2d1a93cde7e2fbc8ae42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Fri, 05 May 2023 18:40:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:40:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:40:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:41:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:41:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:41:09 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:41:09 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:41:10 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:41:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:41:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdea0e5018e1e8cc2b331e1ed2c4f1da84af25221910a1de76e337fce3f545`  
		Last Modified: Fri, 05 May 2023 18:41:45 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f595bfbecb37e114df202f90bab7195189bef04dda60cbede4979c09d3ba64b`  
		Last Modified: Fri, 05 May 2023 18:41:45 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a776250046198e86aba4237e6d8b9c415cbf67db951ceb13f5178ab58e805fb7`  
		Last Modified: Fri, 05 May 2023 18:41:51 GMT  
		Size: 119.4 MB (119387138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d40881fe3ef39538595f3f453d57d7ebea09a143e5d3df1907bf4b684921e1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344633450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe233903eaead3cbcb38fe3cac6c52ea831042611b133da2323a8add4015b81c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Fri, 05 May 2023 18:54:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:54:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:54:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:54:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:55:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:55:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:55:04 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:55:05 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:55:05 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:55:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:55:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa3476c1a9b5d9dca9b0f0758094b3ac19d32c73b84d54aff3fac3c7bec504`  
		Last Modified: Fri, 05 May 2023 18:55:37 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5cfa49c626a3633555164de938e107b78241081aac16df792096779feb2efb`  
		Last Modified: Fri, 05 May 2023 18:55:37 GMT  
		Size: 8.7 KB (8704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f9cbbfae074869c2dee87914fd1be657a8e842fd8bc1823fe4e87ea5bb195`  
		Last Modified: Fri, 05 May 2023 18:55:42 GMT  
		Size: 119.2 MB (119243920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:da1782778d027fe45bca234d76ff4fa11af1c49a2a26475efad6855602ca0abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:3af9527a85c3849c17a2998ceab6d254087389b47711854d47ef5ec4a201a100
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.7 MB (446655333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ef057c144e76908c40703f217a868fedbe7ee097703503a592c5a92b893557`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Fri, 05 May 2023 18:41:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d25329edbbf8a75e9e32d4d0c38fb817f155e171d4cf8b7509a7b50d35bb2549 NEO4J_TARBALL=neo4j-enterprise-4.4.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:41:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:41:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:41:13 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:41:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:41:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:41:27 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:41:27 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:41:27 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:41:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:41:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720502b535fb5be58bd7602dea308927cd1fd4080a054326e8a743accab22bca`  
		Last Modified: Fri, 05 May 2023 18:42:03 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f801877b7ef16ee8653948c8c1c410ce6c276d57543357492d9c4e33bc41f3a`  
		Last Modified: Fri, 05 May 2023 18:42:03 GMT  
		Size: 8.7 KB (8702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b872b2b1808c4596bfa44a00f8202bbf44841f32f4f3bf120b39592b2e22cb`  
		Last Modified: Fri, 05 May 2023 18:42:12 GMT  
		Size: 216.7 MB (216689749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fe5bd2b339c8b81777657fa0753db09fe45d1652269092523235ce338ebaa765
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.9 MB (441933203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d9e131e06753b9de820ed28ea2b8bca82a461bad0be453df7aa347da7500b5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Fri, 05 May 2023 18:55:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d25329edbbf8a75e9e32d4d0c38fb817f155e171d4cf8b7509a7b50d35bb2549 NEO4J_TARBALL=neo4j-enterprise-4.4.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:55:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:55:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:55:08 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:55:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:55:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:55:20 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:55:20 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:55:20 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:55:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:55:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be1c502952730214e6c290ee9b13f0018911d40e0a72c05535507b79a9ca642`  
		Last Modified: Fri, 05 May 2023 18:55:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfd4d5af0b7ce2cbabacd65efb6a6edc53adf348b69e3bd5cd2172e313f519f`  
		Last Modified: Fri, 05 May 2023 18:55:54 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f690115508090a789a2e096bfd38c34bc6c7bcb78c033ca20a4d4dc9f2425213`  
		Last Modified: Fri, 05 May 2023 18:56:03 GMT  
		Size: 216.5 MB (216543668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.20`

```console
$ docker pull neo4j@sha256:6fdc57dab05c4eacb3fa9eb45b2b3944f5e6245391a29dd425d712c619ace055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.20` - linux; amd64

```console
$ docker pull neo4j@sha256:3c1bc38b2ee107cfee02c25dbbfbf1d9d8da9f5d4039970cdecb44c123159832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349352723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22a33d77dddc481fba99555a4e7f6f151baafe444ff2d1a93cde7e2fbc8ae42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Fri, 05 May 2023 18:40:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:40:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:40:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:41:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:41:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:41:09 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:41:09 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:41:10 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:41:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:41:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdea0e5018e1e8cc2b331e1ed2c4f1da84af25221910a1de76e337fce3f545`  
		Last Modified: Fri, 05 May 2023 18:41:45 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f595bfbecb37e114df202f90bab7195189bef04dda60cbede4979c09d3ba64b`  
		Last Modified: Fri, 05 May 2023 18:41:45 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a776250046198e86aba4237e6d8b9c415cbf67db951ceb13f5178ab58e805fb7`  
		Last Modified: Fri, 05 May 2023 18:41:51 GMT  
		Size: 119.4 MB (119387138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.20` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d40881fe3ef39538595f3f453d57d7ebea09a143e5d3df1907bf4b684921e1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344633450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe233903eaead3cbcb38fe3cac6c52ea831042611b133da2323a8add4015b81c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Fri, 05 May 2023 18:54:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:54:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:54:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:54:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:55:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:55:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:55:04 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:55:05 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:55:05 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:55:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:55:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa3476c1a9b5d9dca9b0f0758094b3ac19d32c73b84d54aff3fac3c7bec504`  
		Last Modified: Fri, 05 May 2023 18:55:37 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5cfa49c626a3633555164de938e107b78241081aac16df792096779feb2efb`  
		Last Modified: Fri, 05 May 2023 18:55:37 GMT  
		Size: 8.7 KB (8704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f9cbbfae074869c2dee87914fd1be657a8e842fd8bc1823fe4e87ea5bb195`  
		Last Modified: Fri, 05 May 2023 18:55:42 GMT  
		Size: 119.2 MB (119243920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.20-community`

```console
$ docker pull neo4j@sha256:6fdc57dab05c4eacb3fa9eb45b2b3944f5e6245391a29dd425d712c619ace055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.20-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3c1bc38b2ee107cfee02c25dbbfbf1d9d8da9f5d4039970cdecb44c123159832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349352723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22a33d77dddc481fba99555a4e7f6f151baafe444ff2d1a93cde7e2fbc8ae42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Fri, 05 May 2023 18:40:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:40:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:40:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:40:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:41:09 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:41:09 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:41:09 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:41:09 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:41:10 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:41:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:41:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcdea0e5018e1e8cc2b331e1ed2c4f1da84af25221910a1de76e337fce3f545`  
		Last Modified: Fri, 05 May 2023 18:41:45 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f595bfbecb37e114df202f90bab7195189bef04dda60cbede4979c09d3ba64b`  
		Last Modified: Fri, 05 May 2023 18:41:45 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a776250046198e86aba4237e6d8b9c415cbf67db951ceb13f5178ab58e805fb7`  
		Last Modified: Fri, 05 May 2023 18:41:51 GMT  
		Size: 119.4 MB (119387138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.20-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2d40881fe3ef39538595f3f453d57d7ebea09a143e5d3df1907bf4b684921e1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.6 MB (344633450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe233903eaead3cbcb38fe3cac6c52ea831042611b133da2323a8add4015b81c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Fri, 05 May 2023 18:54:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9d0a96d724615f08934474687707a01afc454dfc09afc3e0ce99d741296d8cbf NEO4J_TARBALL=neo4j-community-4.4.20-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:54:54 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:54:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:54:54 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:55:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:55:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:55:04 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:55:05 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:55:05 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:55:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:55:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0aa3476c1a9b5d9dca9b0f0758094b3ac19d32c73b84d54aff3fac3c7bec504`  
		Last Modified: Fri, 05 May 2023 18:55:37 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad5cfa49c626a3633555164de938e107b78241081aac16df792096779feb2efb`  
		Last Modified: Fri, 05 May 2023 18:55:37 GMT  
		Size: 8.7 KB (8704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43f9cbbfae074869c2dee87914fd1be657a8e842fd8bc1823fe4e87ea5bb195`  
		Last Modified: Fri, 05 May 2023 18:55:42 GMT  
		Size: 119.2 MB (119243920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.20-enterprise`

```console
$ docker pull neo4j@sha256:da1782778d027fe45bca234d76ff4fa11af1c49a2a26475efad6855602ca0abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.20-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:3af9527a85c3849c17a2998ceab6d254087389b47711854d47ef5ec4a201a100
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.7 MB (446655333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ef057c144e76908c40703f217a868fedbe7ee097703503a592c5a92b893557`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:55:29 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Fri, 05 May 2023 18:41:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d25329edbbf8a75e9e32d4d0c38fb817f155e171d4cf8b7509a7b50d35bb2549 NEO4J_TARBALL=neo4j-enterprise-4.4.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:41:12 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:41:13 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:41:13 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:41:27 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:41:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:41:27 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:41:27 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:41:27 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:41:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:41:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c8debf5f3c7bd7d820f2797f8d4cfc95b7902d0071ca115228b3f6eb2d872a`  
		Last Modified: Thu, 04 May 2023 15:06:32 GMT  
		Size: 198.5 MB (198549506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720502b535fb5be58bd7602dea308927cd1fd4080a054326e8a743accab22bca`  
		Last Modified: Fri, 05 May 2023 18:42:03 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f801877b7ef16ee8653948c8c1c410ce6c276d57543357492d9c4e33bc41f3a`  
		Last Modified: Fri, 05 May 2023 18:42:03 GMT  
		Size: 8.7 KB (8702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b872b2b1808c4596bfa44a00f8202bbf44841f32f4f3bf120b39592b2e22cb`  
		Last Modified: Fri, 05 May 2023 18:42:12 GMT  
		Size: 216.7 MB (216689749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.20-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fe5bd2b339c8b81777657fa0753db09fe45d1652269092523235ce338ebaa765
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.9 MB (441933203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d9e131e06753b9de820ed28ea2b8bca82a461bad0be453df7aa347da7500b5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:37 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Fri, 05 May 2023 18:55:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d25329edbbf8a75e9e32d4d0c38fb817f155e171d4cf8b7509a7b50d35bb2549 NEO4J_TARBALL=neo4j-enterprise-4.4.20-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 05 May 2023 18:55:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
# Fri, 05 May 2023 18:55:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 05 May 2023 18:55:08 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 05 May 2023 18:55:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.20-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 05 May 2023 18:55:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 May 2023 18:55:20 GMT
WORKDIR /var/lib/neo4j
# Fri, 05 May 2023 18:55:20 GMT
VOLUME [/data /logs]
# Fri, 05 May 2023 18:55:20 GMT
EXPOSE 7473 7474 7687
# Fri, 05 May 2023 18:55:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 05 May 2023 18:55:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8372f00ab12bb739ea85b3b21db2dbe4809c7c3bd11102276ddbe52e3a864e`  
		Last Modified: Thu, 04 May 2023 10:20:09 GMT  
		Size: 195.3 MB (195324209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be1c502952730214e6c290ee9b13f0018911d40e0a72c05535507b79a9ca642`  
		Last Modified: Fri, 05 May 2023 18:55:54 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfd4d5af0b7ce2cbabacd65efb6a6edc53adf348b69e3bd5cd2172e313f519f`  
		Last Modified: Fri, 05 May 2023 18:55:54 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f690115508090a789a2e096bfd38c34bc6c7bcb78c033ca20a4d4dc9f2425213`  
		Last Modified: Fri, 05 May 2023 18:56:03 GMT  
		Size: 216.5 MB (216543668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:398dea0c984b6f0e6fa70fec7b41d29619674c17959a28ee67d49b9de743d7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:d50b0304fae3972801ff4ba5f2358b1c525f3511f0542186391a72dbfc27541b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b8b0dbf9214aa25d63dbfaee5cd828297c9e76967b664c561fda90bf2206aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:32 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:22:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:22:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:22:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:22:51 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:22:51 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:22:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:22:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69590da706e08dd085962a8111f446d7c2787f896815f1f4485577a36b6dfa30`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfe9b47d1116f45f71779ef0b30cc005f478773d8a396b39a71edb687fa9b4`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c26bc105224c701f63123e956286c0d3a23dbf9597bbf38f381dd7a1a2bbae`  
		Last Modified: Mon, 22 May 2023 20:23:49 GMT  
		Size: 114.7 MB (114688580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d6f8f10da6ea588793a3624a53e9a95ff5ab0b1b902a43dc07b47f62f390a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fc18b61f9247dbf45ab43c8583dd5ce00bf5a2dde0a466716979be6c18743`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:40 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:41:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:41:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:41:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:41:53 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:41:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:41:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:41:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24c0af0966f52b39ffed749fcc7ac480385ca848c515602292cf21b6ab5c57`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a72bb959c2fe7d17c8e12b8227f7c4f3e46bb8cef32b8873f9fea23020eef`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3627f314bc804b661f816d55e262a6896e8cc46a7eb0c712589103882b0ac`  
		Last Modified: Mon, 22 May 2023 20:42:37 GMT  
		Size: 114.5 MB (114545018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:398dea0c984b6f0e6fa70fec7b41d29619674c17959a28ee67d49b9de743d7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d50b0304fae3972801ff4ba5f2358b1c525f3511f0542186391a72dbfc27541b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b8b0dbf9214aa25d63dbfaee5cd828297c9e76967b664c561fda90bf2206aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:32 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:22:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:22:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:22:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:22:51 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:22:51 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:22:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:22:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69590da706e08dd085962a8111f446d7c2787f896815f1f4485577a36b6dfa30`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfe9b47d1116f45f71779ef0b30cc005f478773d8a396b39a71edb687fa9b4`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c26bc105224c701f63123e956286c0d3a23dbf9597bbf38f381dd7a1a2bbae`  
		Last Modified: Mon, 22 May 2023 20:23:49 GMT  
		Size: 114.7 MB (114688580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d6f8f10da6ea588793a3624a53e9a95ff5ab0b1b902a43dc07b47f62f390a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fc18b61f9247dbf45ab43c8583dd5ce00bf5a2dde0a466716979be6c18743`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:40 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:41:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:41:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:41:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:41:53 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:41:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:41:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:41:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24c0af0966f52b39ffed749fcc7ac480385ca848c515602292cf21b6ab5c57`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a72bb959c2fe7d17c8e12b8227f7c4f3e46bb8cef32b8873f9fea23020eef`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3627f314bc804b661f816d55e262a6896e8cc46a7eb0c712589103882b0ac`  
		Last Modified: Mon, 22 May 2023 20:42:37 GMT  
		Size: 114.5 MB (114545018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:09d842ce509af459ce2d32558631aaddd8e18292f6f9753c95d9cdd6ea87c9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c57c2776251a64bce3555a292a2aad01118e7f535057ca8ea2cff884a492d73d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ddc43a5df309d7e75b6a34328f7fde469dd70dde2769e4491dcfdc38a6421`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:56 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:23:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:23:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:23:24 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:23:24 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:23:24 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:23:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:23:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cffd1970e29a1d4398fab4d8828110950e17f9d4559cda0a7cd5bcb4c1a506a`  
		Last Modified: Mon, 22 May 2023 20:24:10 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb8ac9ab437ead168d08aaaf8b66155160fe616d3ca23c9d500a26f3cb38dfb`  
		Last Modified: Mon, 22 May 2023 20:24:10 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d024f530349cfa85a15bb555636fe8ea70bcc9570707cec98120eb99197814`  
		Last Modified: Mon, 22 May 2023 20:24:30 GMT  
		Size: 379.7 MB (379683268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:42ca8fe6b98045d5dc3b59c5d9c86472e5f16b6fefa886beb3831aae222b7164
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a22ce0b872f728daecdabba3c63197159ae65a527218cad450964f7533a06e7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:56 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:42:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:42:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:42:12 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:42:13 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:42:13 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:42:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:42:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a6cfeb8c521df684b8271ff58c0bfe0f59f607c604302cc73f02e1176de805`  
		Last Modified: Mon, 22 May 2023 20:42:57 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da7fc38501e198ef67781844a1edb68b49581a33db12bccd6164c014ef48cfe`  
		Last Modified: Mon, 22 May 2023 20:42:57 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850ea76f6227ff05c47e82a52d3561c2f1d5adadd6525cba8479903aeab75794`  
		Last Modified: Mon, 22 May 2023 20:43:09 GMT  
		Size: 379.5 MB (379541072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8`

```console
$ docker pull neo4j@sha256:398dea0c984b6f0e6fa70fec7b41d29619674c17959a28ee67d49b9de743d7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8` - linux; amd64

```console
$ docker pull neo4j@sha256:d50b0304fae3972801ff4ba5f2358b1c525f3511f0542186391a72dbfc27541b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b8b0dbf9214aa25d63dbfaee5cd828297c9e76967b664c561fda90bf2206aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:32 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:22:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:22:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:22:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:22:51 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:22:51 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:22:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:22:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69590da706e08dd085962a8111f446d7c2787f896815f1f4485577a36b6dfa30`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfe9b47d1116f45f71779ef0b30cc005f478773d8a396b39a71edb687fa9b4`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c26bc105224c701f63123e956286c0d3a23dbf9597bbf38f381dd7a1a2bbae`  
		Last Modified: Mon, 22 May 2023 20:23:49 GMT  
		Size: 114.7 MB (114688580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d6f8f10da6ea588793a3624a53e9a95ff5ab0b1b902a43dc07b47f62f390a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fc18b61f9247dbf45ab43c8583dd5ce00bf5a2dde0a466716979be6c18743`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:40 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:41:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:41:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:41:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:41:53 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:41:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:41:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:41:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24c0af0966f52b39ffed749fcc7ac480385ca848c515602292cf21b6ab5c57`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a72bb959c2fe7d17c8e12b8227f7c4f3e46bb8cef32b8873f9fea23020eef`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3627f314bc804b661f816d55e262a6896e8cc46a7eb0c712589103882b0ac`  
		Last Modified: Mon, 22 May 2023 20:42:37 GMT  
		Size: 114.5 MB (114545018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8-community`

```console
$ docker pull neo4j@sha256:398dea0c984b6f0e6fa70fec7b41d29619674c17959a28ee67d49b9de743d7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d50b0304fae3972801ff4ba5f2358b1c525f3511f0542186391a72dbfc27541b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b8b0dbf9214aa25d63dbfaee5cd828297c9e76967b664c561fda90bf2206aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:32 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:22:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:22:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:22:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:22:51 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:22:51 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:22:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:22:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69590da706e08dd085962a8111f446d7c2787f896815f1f4485577a36b6dfa30`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfe9b47d1116f45f71779ef0b30cc005f478773d8a396b39a71edb687fa9b4`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c26bc105224c701f63123e956286c0d3a23dbf9597bbf38f381dd7a1a2bbae`  
		Last Modified: Mon, 22 May 2023 20:23:49 GMT  
		Size: 114.7 MB (114688580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d6f8f10da6ea588793a3624a53e9a95ff5ab0b1b902a43dc07b47f62f390a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fc18b61f9247dbf45ab43c8583dd5ce00bf5a2dde0a466716979be6c18743`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:40 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:41:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:41:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:41:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:41:53 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:41:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:41:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:41:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24c0af0966f52b39ffed749fcc7ac480385ca848c515602292cf21b6ab5c57`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a72bb959c2fe7d17c8e12b8227f7c4f3e46bb8cef32b8873f9fea23020eef`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3627f314bc804b661f816d55e262a6896e8cc46a7eb0c712589103882b0ac`  
		Last Modified: Mon, 22 May 2023 20:42:37 GMT  
		Size: 114.5 MB (114545018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8-enterprise`

```console
$ docker pull neo4j@sha256:09d842ce509af459ce2d32558631aaddd8e18292f6f9753c95d9cdd6ea87c9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c57c2776251a64bce3555a292a2aad01118e7f535057ca8ea2cff884a492d73d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ddc43a5df309d7e75b6a34328f7fde469dd70dde2769e4491dcfdc38a6421`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:56 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:23:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:23:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:23:24 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:23:24 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:23:24 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:23:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:23:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cffd1970e29a1d4398fab4d8828110950e17f9d4559cda0a7cd5bcb4c1a506a`  
		Last Modified: Mon, 22 May 2023 20:24:10 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb8ac9ab437ead168d08aaaf8b66155160fe616d3ca23c9d500a26f3cb38dfb`  
		Last Modified: Mon, 22 May 2023 20:24:10 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d024f530349cfa85a15bb555636fe8ea70bcc9570707cec98120eb99197814`  
		Last Modified: Mon, 22 May 2023 20:24:30 GMT  
		Size: 379.7 MB (379683268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:42ca8fe6b98045d5dc3b59c5d9c86472e5f16b6fefa886beb3831aae222b7164
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a22ce0b872f728daecdabba3c63197159ae65a527218cad450964f7533a06e7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:56 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:42:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:42:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:42:12 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:42:13 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:42:13 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:42:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:42:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a6cfeb8c521df684b8271ff58c0bfe0f59f607c604302cc73f02e1176de805`  
		Last Modified: Mon, 22 May 2023 20:42:57 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da7fc38501e198ef67781844a1edb68b49581a33db12bccd6164c014ef48cfe`  
		Last Modified: Mon, 22 May 2023 20:42:57 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850ea76f6227ff05c47e82a52d3561c2f1d5adadd6525cba8479903aeab75794`  
		Last Modified: Mon, 22 May 2023 20:43:09 GMT  
		Size: 379.5 MB (379541072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0`

```console
$ docker pull neo4j@sha256:398dea0c984b6f0e6fa70fec7b41d29619674c17959a28ee67d49b9de743d7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0` - linux; amd64

```console
$ docker pull neo4j@sha256:d50b0304fae3972801ff4ba5f2358b1c525f3511f0542186391a72dbfc27541b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b8b0dbf9214aa25d63dbfaee5cd828297c9e76967b664c561fda90bf2206aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:32 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:22:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:22:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:22:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:22:51 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:22:51 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:22:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:22:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69590da706e08dd085962a8111f446d7c2787f896815f1f4485577a36b6dfa30`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfe9b47d1116f45f71779ef0b30cc005f478773d8a396b39a71edb687fa9b4`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c26bc105224c701f63123e956286c0d3a23dbf9597bbf38f381dd7a1a2bbae`  
		Last Modified: Mon, 22 May 2023 20:23:49 GMT  
		Size: 114.7 MB (114688580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d6f8f10da6ea588793a3624a53e9a95ff5ab0b1b902a43dc07b47f62f390a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fc18b61f9247dbf45ab43c8583dd5ce00bf5a2dde0a466716979be6c18743`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:40 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:41:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:41:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:41:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:41:53 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:41:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:41:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:41:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24c0af0966f52b39ffed749fcc7ac480385ca848c515602292cf21b6ab5c57`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a72bb959c2fe7d17c8e12b8227f7c4f3e46bb8cef32b8873f9fea23020eef`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3627f314bc804b661f816d55e262a6896e8cc46a7eb0c712589103882b0ac`  
		Last Modified: Mon, 22 May 2023 20:42:37 GMT  
		Size: 114.5 MB (114545018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0-community`

```console
$ docker pull neo4j@sha256:398dea0c984b6f0e6fa70fec7b41d29619674c17959a28ee67d49b9de743d7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d50b0304fae3972801ff4ba5f2358b1c525f3511f0542186391a72dbfc27541b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b8b0dbf9214aa25d63dbfaee5cd828297c9e76967b664c561fda90bf2206aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:32 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:22:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:22:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:22:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:22:51 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:22:51 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:22:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:22:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69590da706e08dd085962a8111f446d7c2787f896815f1f4485577a36b6dfa30`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfe9b47d1116f45f71779ef0b30cc005f478773d8a396b39a71edb687fa9b4`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c26bc105224c701f63123e956286c0d3a23dbf9597bbf38f381dd7a1a2bbae`  
		Last Modified: Mon, 22 May 2023 20:23:49 GMT  
		Size: 114.7 MB (114688580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d6f8f10da6ea588793a3624a53e9a95ff5ab0b1b902a43dc07b47f62f390a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fc18b61f9247dbf45ab43c8583dd5ce00bf5a2dde0a466716979be6c18743`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:40 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:41:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:41:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:41:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:41:53 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:41:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:41:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:41:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24c0af0966f52b39ffed749fcc7ac480385ca848c515602292cf21b6ab5c57`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a72bb959c2fe7d17c8e12b8227f7c4f3e46bb8cef32b8873f9fea23020eef`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3627f314bc804b661f816d55e262a6896e8cc46a7eb0c712589103882b0ac`  
		Last Modified: Mon, 22 May 2023 20:42:37 GMT  
		Size: 114.5 MB (114545018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0-enterprise`

```console
$ docker pull neo4j@sha256:09d842ce509af459ce2d32558631aaddd8e18292f6f9753c95d9cdd6ea87c9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c57c2776251a64bce3555a292a2aad01118e7f535057ca8ea2cff884a492d73d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ddc43a5df309d7e75b6a34328f7fde469dd70dde2769e4491dcfdc38a6421`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:56 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:23:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:23:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:23:24 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:23:24 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:23:24 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:23:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:23:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cffd1970e29a1d4398fab4d8828110950e17f9d4559cda0a7cd5bcb4c1a506a`  
		Last Modified: Mon, 22 May 2023 20:24:10 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb8ac9ab437ead168d08aaaf8b66155160fe616d3ca23c9d500a26f3cb38dfb`  
		Last Modified: Mon, 22 May 2023 20:24:10 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d024f530349cfa85a15bb555636fe8ea70bcc9570707cec98120eb99197814`  
		Last Modified: Mon, 22 May 2023 20:24:30 GMT  
		Size: 379.7 MB (379683268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:42ca8fe6b98045d5dc3b59c5d9c86472e5f16b6fefa886beb3831aae222b7164
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a22ce0b872f728daecdabba3c63197159ae65a527218cad450964f7533a06e7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:56 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:42:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:42:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:42:12 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:42:13 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:42:13 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:42:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:42:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a6cfeb8c521df684b8271ff58c0bfe0f59f607c604302cc73f02e1176de805`  
		Last Modified: Mon, 22 May 2023 20:42:57 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da7fc38501e198ef67781844a1edb68b49581a33db12bccd6164c014ef48cfe`  
		Last Modified: Mon, 22 May 2023 20:42:57 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850ea76f6227ff05c47e82a52d3561c2f1d5adadd6525cba8479903aeab75794`  
		Last Modified: Mon, 22 May 2023 20:43:09 GMT  
		Size: 379.5 MB (379541072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:398dea0c984b6f0e6fa70fec7b41d29619674c17959a28ee67d49b9de743d7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:d50b0304fae3972801ff4ba5f2358b1c525f3511f0542186391a72dbfc27541b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b8b0dbf9214aa25d63dbfaee5cd828297c9e76967b664c561fda90bf2206aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:32 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:22:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:22:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:22:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:22:51 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:22:51 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:22:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:22:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69590da706e08dd085962a8111f446d7c2787f896815f1f4485577a36b6dfa30`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfe9b47d1116f45f71779ef0b30cc005f478773d8a396b39a71edb687fa9b4`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c26bc105224c701f63123e956286c0d3a23dbf9597bbf38f381dd7a1a2bbae`  
		Last Modified: Mon, 22 May 2023 20:23:49 GMT  
		Size: 114.7 MB (114688580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d6f8f10da6ea588793a3624a53e9a95ff5ab0b1b902a43dc07b47f62f390a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fc18b61f9247dbf45ab43c8583dd5ce00bf5a2dde0a466716979be6c18743`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:40 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:41:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:41:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:41:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:41:53 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:41:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:41:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:41:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24c0af0966f52b39ffed749fcc7ac480385ca848c515602292cf21b6ab5c57`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a72bb959c2fe7d17c8e12b8227f7c4f3e46bb8cef32b8873f9fea23020eef`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3627f314bc804b661f816d55e262a6896e8cc46a7eb0c712589103882b0ac`  
		Last Modified: Mon, 22 May 2023 20:42:37 GMT  
		Size: 114.5 MB (114545018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:09d842ce509af459ce2d32558631aaddd8e18292f6f9753c95d9cdd6ea87c9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c57c2776251a64bce3555a292a2aad01118e7f535057ca8ea2cff884a492d73d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166ddc43a5df309d7e75b6a34328f7fde469dd70dde2769e4491dcfdc38a6421`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:56 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:23:23 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:23:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:23:24 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:23:24 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:23:24 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:23:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:23:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cffd1970e29a1d4398fab4d8828110950e17f9d4559cda0a7cd5bcb4c1a506a`  
		Last Modified: Mon, 22 May 2023 20:24:10 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb8ac9ab437ead168d08aaaf8b66155160fe616d3ca23c9d500a26f3cb38dfb`  
		Last Modified: Mon, 22 May 2023 20:24:10 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d024f530349cfa85a15bb555636fe8ea70bcc9570707cec98120eb99197814`  
		Last Modified: Mon, 22 May 2023 20:24:30 GMT  
		Size: 379.7 MB (379683268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:42ca8fe6b98045d5dc3b59c5d9c86472e5f16b6fefa886beb3831aae222b7164
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a22ce0b872f728daecdabba3c63197159ae65a527218cad450964f7533a06e7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:55 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:56 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:42:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:42:12 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:42:12 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:42:13 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:42:13 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:42:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:42:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a6cfeb8c521df684b8271ff58c0bfe0f59f607c604302cc73f02e1176de805`  
		Last Modified: Mon, 22 May 2023 20:42:57 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da7fc38501e198ef67781844a1edb68b49581a33db12bccd6164c014ef48cfe`  
		Last Modified: Mon, 22 May 2023 20:42:57 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850ea76f6227ff05c47e82a52d3561c2f1d5adadd6525cba8479903aeab75794`  
		Last Modified: Mon, 22 May 2023 20:43:09 GMT  
		Size: 379.5 MB (379541072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:398dea0c984b6f0e6fa70fec7b41d29619674c17959a28ee67d49b9de743d7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:d50b0304fae3972801ff4ba5f2358b1c525f3511f0542186391a72dbfc27541b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b8b0dbf9214aa25d63dbfaee5cd828297c9e76967b664c561fda90bf2206aa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 14:59:25 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Mon, 22 May 2023 20:22:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:22:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:22:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:22:32 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:22:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:22:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:22:51 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:22:51 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:22:51 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:22:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:22:51 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fd2caa057611d1671449088801d8f3e11973cc523e65f79f2b73f9189938c0`  
		Last Modified: Thu, 04 May 2023 15:09:34 GMT  
		Size: 192.6 MB (192580382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69590da706e08dd085962a8111f446d7c2787f896815f1f4485577a36b6dfa30`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abfe9b47d1116f45f71779ef0b30cc005f478773d8a396b39a71edb687fa9b4`  
		Last Modified: Mon, 22 May 2023 20:23:44 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c26bc105224c701f63123e956286c0d3a23dbf9597bbf38f381dd7a1a2bbae`  
		Last Modified: Mon, 22 May 2023 20:23:49 GMT  
		Size: 114.7 MB (114688580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4d6f8f10da6ea588793a3624a53e9a95ff5ab0b1b902a43dc07b47f62f390a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118fc18b61f9247dbf45ab43c8583dd5ce00bf5a2dde0a466716979be6c18743`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:14:13 GMT
COPY dir:1b2a87d4690d92c678e5e7380bdebd2fd0670a13533a2a897045c86dc03eb9f6 in /opt/java/openjdk 
# Mon, 22 May 2023 20:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 22 May 2023 20:41:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Mon, 22 May 2023 20:41:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 22 May 2023 20:41:40 GMT
COPY multi:b0adb110d92b4bcfe30cb0c0db43c522b6bd0c9497a88b7577c0c7f10bfdc932 in /startup/ 
# Mon, 22 May 2023 20:41:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 22 May 2023 20:41:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 May 2023 20:41:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 22 May 2023 20:41:53 GMT
VOLUME [/data /logs]
# Mon, 22 May 2023 20:41:53 GMT
EXPOSE 7473 7474 7687
# Mon, 22 May 2023 20:41:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 22 May 2023 20:41:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c575b486fb24233a04314b561ec4eeae43d749cd55a8b6194087d505365366b7`  
		Last Modified: Thu, 04 May 2023 10:22:21 GMT  
		Size: 191.4 MB (191387643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b24c0af0966f52b39ffed749fcc7ac480385ca848c515602292cf21b6ab5c57`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4a72bb959c2fe7d17c8e12b8227f7c4f3e46bb8cef32b8873f9fea23020eef`  
		Last Modified: Mon, 22 May 2023 20:42:33 GMT  
		Size: 8.8 KB (8766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b3627f314bc804b661f816d55e262a6896e8cc46a7eb0c712589103882b0ac`  
		Last Modified: Mon, 22 May 2023 20:42:37 GMT  
		Size: 114.5 MB (114545018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
