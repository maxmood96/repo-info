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
$ docker pull neo4j@sha256:c9f3343a0862f7bc22a0049d5063ccb073237fbb6ada28bb052f8f57fb05923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:e4891c015c172e807e55d5d74412e0379b2148df49a79c7aa60e5ecc015aff9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366801221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689e14f3a2234f097ee5ffabf2838ab78fd2cc05b5e8d5245d1ffc8517a9e2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:42 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:01:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:01:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 10:01:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:01:20 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 10:01:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:31 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:32 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:32 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe464df9e08939be8903d77d5ed79aa7c6bab63ba7dd463f4b456b4fcdb5306`  
		Last Modified: Thu, 02 Mar 2023 09:12:53 GMT  
		Size: 198.5 MB (198475456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79681f3dc915bdfd35cd9f526a8f5b43c534dd94ad5f44d248fc9a3a605c8412`  
		Last Modified: Thu, 02 Mar 2023 10:03:06 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c337d142cea00214194a723c86d3d216b0b89651fd60c064faa167ff9eeae25f`  
		Last Modified: Thu, 02 Mar 2023 10:03:06 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef303c2d45d5edb1812b35f034107106876e3dae565ec2368008981e8ba0cf7e`  
		Last Modified: Thu, 02 Mar 2023 10:03:13 GMT  
		Size: 136.9 MB (136902075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d567ce48ba88cbc62c299bebec99fb32954db7e32df4e2a4724f91664cd73f93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362073528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955ccee95b7e9a2eaf239123d21dcef286f4a5dad1f74714d022fce42a46dfe0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:02:38 GMT
COPY dir:10bda54a6f055ef6cbbc2c7efdd1ef99bb798b3ae26972613c5ee4e57e620aeb in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:37:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:37:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 07:37:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:37:26 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 07:37:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:36 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:36 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594d0c25b8198dd3c5842d1aeb5b5630309d3dc5160dd9849d5f1ba6b3b6b55`  
		Last Modified: Thu, 02 Mar 2023 07:17:16 GMT  
		Size: 195.2 MB (195240256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c28c2e173af5deee10aecc18a493f0ab08b9f21b504d74edfa20bb44d9ba40`  
		Last Modified: Thu, 02 Mar 2023 07:39:04 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfab0449bb52a49adf91e72eab36963b2cc19616573c1a3061a006abb3b39004`  
		Last Modified: Thu, 02 Mar 2023 07:39:04 GMT  
		Size: 8.4 KB (8425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46adef28c3f6c79ba582504ac9e56671af0c15a21e91ecf8c6d1df40098bf037`  
		Last Modified: Thu, 02 Mar 2023 07:39:11 GMT  
		Size: 136.8 MB (136758147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:c9f3343a0862f7bc22a0049d5063ccb073237fbb6ada28bb052f8f57fb05923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:e4891c015c172e807e55d5d74412e0379b2148df49a79c7aa60e5ecc015aff9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366801221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689e14f3a2234f097ee5ffabf2838ab78fd2cc05b5e8d5245d1ffc8517a9e2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:42 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:01:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:01:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 10:01:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:01:20 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 10:01:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:31 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:32 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:32 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe464df9e08939be8903d77d5ed79aa7c6bab63ba7dd463f4b456b4fcdb5306`  
		Last Modified: Thu, 02 Mar 2023 09:12:53 GMT  
		Size: 198.5 MB (198475456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79681f3dc915bdfd35cd9f526a8f5b43c534dd94ad5f44d248fc9a3a605c8412`  
		Last Modified: Thu, 02 Mar 2023 10:03:06 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c337d142cea00214194a723c86d3d216b0b89651fd60c064faa167ff9eeae25f`  
		Last Modified: Thu, 02 Mar 2023 10:03:06 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef303c2d45d5edb1812b35f034107106876e3dae565ec2368008981e8ba0cf7e`  
		Last Modified: Thu, 02 Mar 2023 10:03:13 GMT  
		Size: 136.9 MB (136902075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d567ce48ba88cbc62c299bebec99fb32954db7e32df4e2a4724f91664cd73f93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362073528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955ccee95b7e9a2eaf239123d21dcef286f4a5dad1f74714d022fce42a46dfe0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:02:38 GMT
COPY dir:10bda54a6f055ef6cbbc2c7efdd1ef99bb798b3ae26972613c5ee4e57e620aeb in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:37:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:37:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 07:37:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:37:26 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 07:37:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:36 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:36 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594d0c25b8198dd3c5842d1aeb5b5630309d3dc5160dd9849d5f1ba6b3b6b55`  
		Last Modified: Thu, 02 Mar 2023 07:17:16 GMT  
		Size: 195.2 MB (195240256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c28c2e173af5deee10aecc18a493f0ab08b9f21b504d74edfa20bb44d9ba40`  
		Last Modified: Thu, 02 Mar 2023 07:39:04 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfab0449bb52a49adf91e72eab36963b2cc19616573c1a3061a006abb3b39004`  
		Last Modified: Thu, 02 Mar 2023 07:39:04 GMT  
		Size: 8.4 KB (8425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46adef28c3f6c79ba582504ac9e56671af0c15a21e91ecf8c6d1df40098bf037`  
		Last Modified: Thu, 02 Mar 2023 07:39:11 GMT  
		Size: 136.8 MB (136758147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:2ee46e61611424a35ff72b2d76d4b14710b2a6ea4388172b32eb745d9f1a376c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:467404a0cf39bfd5ea014a9d625dda8369f717cd8d6dd8d0286c591aecbb6280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.2 MB (463204868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50370c33d189e8719e570752408837eeb4d0dbacbf558c6dd0de51ee54e62591`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:42 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:01:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79d7283199af9e4830dbf79ff36b98d8851b342724edd741785b91bad33f7d73 NEO4J_TARBALL=neo4j-enterprise-4.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:01:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 10:01:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:01:37 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 10:01:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:52 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:52 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe464df9e08939be8903d77d5ed79aa7c6bab63ba7dd463f4b456b4fcdb5306`  
		Last Modified: Thu, 02 Mar 2023 09:12:53 GMT  
		Size: 198.5 MB (198475456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1006900153d946b255f6aa9ef89ee55708d92f3f0e724990fd0189d33b1f08fb`  
		Last Modified: Thu, 02 Mar 2023 10:03:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117a80e2593750bc9900d79b9362f9fc26dd34c11a3fc08dddb04c83ecdfd187`  
		Last Modified: Thu, 02 Mar 2023 10:03:26 GMT  
		Size: 8.4 KB (8429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c166e769e2028b3f9d949581020c0224877f21b6c9cba86457e3cd2efc3d16`  
		Last Modified: Thu, 02 Mar 2023 10:03:36 GMT  
		Size: 233.3 MB (233305724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1d391bc0d97d760340c9e1d334432478e437b9deb4452f323a427654462b98a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.5 MB (458479335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269cdaf0c2471f888a201d46e727c3dc4a82649100234a68406b935cf42d677f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:02:38 GMT
COPY dir:10bda54a6f055ef6cbbc2c7efdd1ef99bb798b3ae26972613c5ee4e57e620aeb in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:37:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79d7283199af9e4830dbf79ff36b98d8851b342724edd741785b91bad33f7d73 NEO4J_TARBALL=neo4j-enterprise-4.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:37:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 07:37:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:37:40 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 07:37:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:53 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:53 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:53 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594d0c25b8198dd3c5842d1aeb5b5630309d3dc5160dd9849d5f1ba6b3b6b55`  
		Last Modified: Thu, 02 Mar 2023 07:17:16 GMT  
		Size: 195.2 MB (195240256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b69429139d802bc77701f6dc61572d37b75459e09207496f696851a7f2ff87a`  
		Last Modified: Thu, 02 Mar 2023 07:39:23 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a1390cadede723a55a282a7feb8c700c049eb93919b99b24d06c703f658dc`  
		Last Modified: Thu, 02 Mar 2023 07:39:23 GMT  
		Size: 8.4 KB (8424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e897845db2d78a1461fe025711fb9b982787f1dbf0be14e5481f137b09e6e4b0`  
		Last Modified: Thu, 02 Mar 2023 07:39:32 GMT  
		Size: 233.2 MB (233163954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.18`

```console
$ docker pull neo4j@sha256:c9f3343a0862f7bc22a0049d5063ccb073237fbb6ada28bb052f8f57fb05923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.18` - linux; amd64

```console
$ docker pull neo4j@sha256:e4891c015c172e807e55d5d74412e0379b2148df49a79c7aa60e5ecc015aff9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366801221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689e14f3a2234f097ee5ffabf2838ab78fd2cc05b5e8d5245d1ffc8517a9e2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:42 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:01:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:01:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 10:01:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:01:20 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 10:01:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:31 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:32 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:32 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe464df9e08939be8903d77d5ed79aa7c6bab63ba7dd463f4b456b4fcdb5306`  
		Last Modified: Thu, 02 Mar 2023 09:12:53 GMT  
		Size: 198.5 MB (198475456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79681f3dc915bdfd35cd9f526a8f5b43c534dd94ad5f44d248fc9a3a605c8412`  
		Last Modified: Thu, 02 Mar 2023 10:03:06 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c337d142cea00214194a723c86d3d216b0b89651fd60c064faa167ff9eeae25f`  
		Last Modified: Thu, 02 Mar 2023 10:03:06 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef303c2d45d5edb1812b35f034107106876e3dae565ec2368008981e8ba0cf7e`  
		Last Modified: Thu, 02 Mar 2023 10:03:13 GMT  
		Size: 136.9 MB (136902075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.18` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d567ce48ba88cbc62c299bebec99fb32954db7e32df4e2a4724f91664cd73f93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362073528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955ccee95b7e9a2eaf239123d21dcef286f4a5dad1f74714d022fce42a46dfe0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:02:38 GMT
COPY dir:10bda54a6f055ef6cbbc2c7efdd1ef99bb798b3ae26972613c5ee4e57e620aeb in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:37:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:37:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 07:37:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:37:26 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 07:37:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:36 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:36 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594d0c25b8198dd3c5842d1aeb5b5630309d3dc5160dd9849d5f1ba6b3b6b55`  
		Last Modified: Thu, 02 Mar 2023 07:17:16 GMT  
		Size: 195.2 MB (195240256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c28c2e173af5deee10aecc18a493f0ab08b9f21b504d74edfa20bb44d9ba40`  
		Last Modified: Thu, 02 Mar 2023 07:39:04 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfab0449bb52a49adf91e72eab36963b2cc19616573c1a3061a006abb3b39004`  
		Last Modified: Thu, 02 Mar 2023 07:39:04 GMT  
		Size: 8.4 KB (8425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46adef28c3f6c79ba582504ac9e56671af0c15a21e91ecf8c6d1df40098bf037`  
		Last Modified: Thu, 02 Mar 2023 07:39:11 GMT  
		Size: 136.8 MB (136758147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.18-community`

```console
$ docker pull neo4j@sha256:c9f3343a0862f7bc22a0049d5063ccb073237fbb6ada28bb052f8f57fb05923c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.18-community` - linux; amd64

```console
$ docker pull neo4j@sha256:e4891c015c172e807e55d5d74412e0379b2148df49a79c7aa60e5ecc015aff9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366801221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689e14f3a2234f097ee5ffabf2838ab78fd2cc05b5e8d5245d1ffc8517a9e2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:42 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:01:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:01:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 10:01:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:01:20 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 10:01:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:31 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:32 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:32 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe464df9e08939be8903d77d5ed79aa7c6bab63ba7dd463f4b456b4fcdb5306`  
		Last Modified: Thu, 02 Mar 2023 09:12:53 GMT  
		Size: 198.5 MB (198475456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79681f3dc915bdfd35cd9f526a8f5b43c534dd94ad5f44d248fc9a3a605c8412`  
		Last Modified: Thu, 02 Mar 2023 10:03:06 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c337d142cea00214194a723c86d3d216b0b89651fd60c064faa167ff9eeae25f`  
		Last Modified: Thu, 02 Mar 2023 10:03:06 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef303c2d45d5edb1812b35f034107106876e3dae565ec2368008981e8ba0cf7e`  
		Last Modified: Thu, 02 Mar 2023 10:03:13 GMT  
		Size: 136.9 MB (136902075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.18-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d567ce48ba88cbc62c299bebec99fb32954db7e32df4e2a4724f91664cd73f93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.1 MB (362073528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955ccee95b7e9a2eaf239123d21dcef286f4a5dad1f74714d022fce42a46dfe0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:02:38 GMT
COPY dir:10bda54a6f055ef6cbbc2c7efdd1ef99bb798b3ae26972613c5ee4e57e620aeb in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:37:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a57309da7081c89969d8763d6f41353ede93cc7fa3f65bf7b240571e13757c7e NEO4J_TARBALL=neo4j-community-4.4.18-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:37:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 07:37:26 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:37:26 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 07:37:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:36 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:36 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:36 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594d0c25b8198dd3c5842d1aeb5b5630309d3dc5160dd9849d5f1ba6b3b6b55`  
		Last Modified: Thu, 02 Mar 2023 07:17:16 GMT  
		Size: 195.2 MB (195240256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c28c2e173af5deee10aecc18a493f0ab08b9f21b504d74edfa20bb44d9ba40`  
		Last Modified: Thu, 02 Mar 2023 07:39:04 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfab0449bb52a49adf91e72eab36963b2cc19616573c1a3061a006abb3b39004`  
		Last Modified: Thu, 02 Mar 2023 07:39:04 GMT  
		Size: 8.4 KB (8425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46adef28c3f6c79ba582504ac9e56671af0c15a21e91ecf8c6d1df40098bf037`  
		Last Modified: Thu, 02 Mar 2023 07:39:11 GMT  
		Size: 136.8 MB (136758147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.18-enterprise`

```console
$ docker pull neo4j@sha256:2ee46e61611424a35ff72b2d76d4b14710b2a6ea4388172b32eb745d9f1a376c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.18-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:467404a0cf39bfd5ea014a9d625dda8369f717cd8d6dd8d0286c591aecbb6280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.2 MB (463204868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50370c33d189e8719e570752408837eeb4d0dbacbf558c6dd0de51ee54e62591`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 08:55:42 GMT
COPY dir:00b91555b346efd0ed206d19de82e3af67e3591603a223e1eef0aee2c231a058 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:01:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79d7283199af9e4830dbf79ff36b98d8851b342724edd741785b91bad33f7d73 NEO4J_TARBALL=neo4j-enterprise-4.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:01:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 10:01:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:01:37 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 10:01:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:52 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:52 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:52 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:52 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe464df9e08939be8903d77d5ed79aa7c6bab63ba7dd463f4b456b4fcdb5306`  
		Last Modified: Thu, 02 Mar 2023 09:12:53 GMT  
		Size: 198.5 MB (198475456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1006900153d946b255f6aa9ef89ee55708d92f3f0e724990fd0189d33b1f08fb`  
		Last Modified: Thu, 02 Mar 2023 10:03:26 GMT  
		Size: 3.9 KB (3856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117a80e2593750bc9900d79b9362f9fc26dd34c11a3fc08dddb04c83ecdfd187`  
		Last Modified: Thu, 02 Mar 2023 10:03:26 GMT  
		Size: 8.4 KB (8429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c166e769e2028b3f9d949581020c0224877f21b6c9cba86457e3cd2efc3d16`  
		Last Modified: Thu, 02 Mar 2023 10:03:36 GMT  
		Size: 233.3 MB (233305724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.18-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1d391bc0d97d760340c9e1d334432478e437b9deb4452f323a427654462b98a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.5 MB (458479335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269cdaf0c2471f888a201d46e727c3dc4a82649100234a68406b935cf42d677f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:02:38 GMT
COPY dir:10bda54a6f055ef6cbbc2c7efdd1ef99bb798b3ae26972613c5ee4e57e620aeb in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:37:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79d7283199af9e4830dbf79ff36b98d8851b342724edd741785b91bad33f7d73 NEO4J_TARBALL=neo4j-enterprise-4.4.18-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:37:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
# Thu, 02 Mar 2023 07:37:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:37:40 GMT
COPY multi:04123c94ab9ad8cef3e56e409d388ad61ce6394c2b8e0f4e659e18f898d77e6b in /startup/ 
# Thu, 02 Mar 2023 07:37:51 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.18-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:53 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:53 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:53 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4594d0c25b8198dd3c5842d1aeb5b5630309d3dc5160dd9849d5f1ba6b3b6b55`  
		Last Modified: Thu, 02 Mar 2023 07:17:16 GMT  
		Size: 195.2 MB (195240256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b69429139d802bc77701f6dc61572d37b75459e09207496f696851a7f2ff87a`  
		Last Modified: Thu, 02 Mar 2023 07:39:23 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a1390cadede723a55a282a7feb8c700c049eb93919b99b24d06c703f658dc`  
		Last Modified: Thu, 02 Mar 2023 07:39:23 GMT  
		Size: 8.4 KB (8424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e897845db2d78a1461fe025711fb9b982787f1dbf0be14e5481f137b09e6e4b0`  
		Last Modified: Thu, 02 Mar 2023 07:39:32 GMT  
		Size: 233.2 MB (233163954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:8ce64b419712ffde6540457bc689db6b3b0490c8181719183693421b87a8b053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:a9229cc31018c53d3fe7bb6d61723c2df50d7a81176722405adb54ea62781c65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a856d660b7eb78bfc8ff8440d1313a80b8754f09c8f33717732732a1d77aeda`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:39 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:00:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:00:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:00:53 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:00:53 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:00:54 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:00:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:00:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8035abbeafe764bf626a88951af419f66543beb1fdca2e21a8bc813233bf0722`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f507dd7037e462494f7e92ff5f6f2b6fe172b8a49c5e174b09b14986cd0e3`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a33c3e8a4092fde738023c7028eadde2c63aaf7ec763b76492eec2776030a6d`  
		Last Modified: Thu, 02 Mar 2023 10:02:19 GMT  
		Size: 115.2 MB (115196107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:72d6325c0d6601283c27c40ae3c13294073bee70d71c8042f49a0a492f1ec624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354da8b4ed8ec16ec88326e6de40d64674a252e13ffd6d9406973639820f73cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:35 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:36:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:36:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:36:47 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:36:47 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:36:47 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:36:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:36:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818b02e934fe24a985972eec0c2fff40a667e3ee49d1c25cde836dca2be07cf`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e884a6459a84c8d9ec181eb931feae2853c28fb2a165811fbcb3d33a9ca4ab0`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 8.4 KB (8423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f59750abf14b5acbedee984371b6e0edcb920352fd8633bb7c81ca6fcbbcf`  
		Last Modified: Thu, 02 Mar 2023 07:38:20 GMT  
		Size: 115.1 MB (115051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:8ce64b419712ffde6540457bc689db6b3b0490c8181719183693421b87a8b053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a9229cc31018c53d3fe7bb6d61723c2df50d7a81176722405adb54ea62781c65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a856d660b7eb78bfc8ff8440d1313a80b8754f09c8f33717732732a1d77aeda`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:39 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:00:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:00:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:00:53 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:00:53 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:00:54 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:00:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:00:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8035abbeafe764bf626a88951af419f66543beb1fdca2e21a8bc813233bf0722`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f507dd7037e462494f7e92ff5f6f2b6fe172b8a49c5e174b09b14986cd0e3`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a33c3e8a4092fde738023c7028eadde2c63aaf7ec763b76492eec2776030a6d`  
		Last Modified: Thu, 02 Mar 2023 10:02:19 GMT  
		Size: 115.2 MB (115196107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:72d6325c0d6601283c27c40ae3c13294073bee70d71c8042f49a0a492f1ec624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354da8b4ed8ec16ec88326e6de40d64674a252e13ffd6d9406973639820f73cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:35 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:36:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:36:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:36:47 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:36:47 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:36:47 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:36:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:36:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818b02e934fe24a985972eec0c2fff40a667e3ee49d1c25cde836dca2be07cf`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e884a6459a84c8d9ec181eb931feae2853c28fb2a165811fbcb3d33a9ca4ab0`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 8.4 KB (8423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f59750abf14b5acbedee984371b6e0edcb920352fd8633bb7c81ca6fcbbcf`  
		Last Modified: Thu, 02 Mar 2023 07:38:20 GMT  
		Size: 115.1 MB (115051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:99b5a2b5d2e18178fdbbb76d581f59d7ad9942d5e0d3d33ad9369a992eb0c5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:3c4b6ff757af0150f7633d6071830274bf44dba1a2761e048ad933f294113af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.0 MB (543986466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2c8de2eca7f4dcf77ec19df279f7edc21681782af93972591b03b889d116f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:59 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:01:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:16 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:16 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a134df60b1a1a5cab9f66081b40bb30fdd5a95887ceb76c51e97cf5254d699`  
		Last Modified: Thu, 02 Mar 2023 10:02:36 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4d3dd0a7fd30e76d65e49ac99622673782e32a34c1d04b3b7b906ec34b368a`  
		Last Modified: Thu, 02 Mar 2023 10:02:37 GMT  
		Size: 8.4 KB (8419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa7bf53d99f43f081283e07e457d8279863bf7a857b4b1abf38e8524ea9cf67`  
		Last Modified: Thu, 02 Mar 2023 10:02:54 GMT  
		Size: 320.1 MB (320124567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1c72e0fd371f9c714089012adcf6c98ed8080f4deff364d7a44de73ff3461adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.3 MB (541317672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a8986d4118bbbad30dc006f061f1a1a5b0a87432c21eec2616480cf9d2d62c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:52 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:37:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:17 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:17 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:17 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e67562eaa79cf5c3d0c20d52a796769a8e752042a88822c034467fde45f9f`  
		Last Modified: Thu, 02 Mar 2023 07:38:39 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b373918e7ca45f4b0a3e6774b789a7119c3b3f11bf8a31a4bffb5eedd5ba0983`  
		Last Modified: Thu, 02 Mar 2023 07:38:39 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f830c2b3bca661c9eb4fa6b1c768bc4c8a9c06f9edfdc18d2c1efa5f7ebf6f`  
		Last Modified: Thu, 02 Mar 2023 07:38:51 GMT  
		Size: 320.0 MB (319982101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5`

```console
$ docker pull neo4j@sha256:8ce64b419712ffde6540457bc689db6b3b0490c8181719183693421b87a8b053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5` - linux; amd64

```console
$ docker pull neo4j@sha256:a9229cc31018c53d3fe7bb6d61723c2df50d7a81176722405adb54ea62781c65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a856d660b7eb78bfc8ff8440d1313a80b8754f09c8f33717732732a1d77aeda`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:39 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:00:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:00:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:00:53 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:00:53 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:00:54 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:00:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:00:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8035abbeafe764bf626a88951af419f66543beb1fdca2e21a8bc813233bf0722`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f507dd7037e462494f7e92ff5f6f2b6fe172b8a49c5e174b09b14986cd0e3`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a33c3e8a4092fde738023c7028eadde2c63aaf7ec763b76492eec2776030a6d`  
		Last Modified: Thu, 02 Mar 2023 10:02:19 GMT  
		Size: 115.2 MB (115196107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:72d6325c0d6601283c27c40ae3c13294073bee70d71c8042f49a0a492f1ec624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354da8b4ed8ec16ec88326e6de40d64674a252e13ffd6d9406973639820f73cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:35 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:36:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:36:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:36:47 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:36:47 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:36:47 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:36:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:36:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818b02e934fe24a985972eec0c2fff40a667e3ee49d1c25cde836dca2be07cf`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e884a6459a84c8d9ec181eb931feae2853c28fb2a165811fbcb3d33a9ca4ab0`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 8.4 KB (8423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f59750abf14b5acbedee984371b6e0edcb920352fd8633bb7c81ca6fcbbcf`  
		Last Modified: Thu, 02 Mar 2023 07:38:20 GMT  
		Size: 115.1 MB (115051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5-enterprise`

```console
$ docker pull neo4j@sha256:99b5a2b5d2e18178fdbbb76d581f59d7ad9942d5e0d3d33ad9369a992eb0c5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:3c4b6ff757af0150f7633d6071830274bf44dba1a2761e048ad933f294113af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.0 MB (543986466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2c8de2eca7f4dcf77ec19df279f7edc21681782af93972591b03b889d116f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:59 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:01:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:16 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:16 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a134df60b1a1a5cab9f66081b40bb30fdd5a95887ceb76c51e97cf5254d699`  
		Last Modified: Thu, 02 Mar 2023 10:02:36 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4d3dd0a7fd30e76d65e49ac99622673782e32a34c1d04b3b7b906ec34b368a`  
		Last Modified: Thu, 02 Mar 2023 10:02:37 GMT  
		Size: 8.4 KB (8419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa7bf53d99f43f081283e07e457d8279863bf7a857b4b1abf38e8524ea9cf67`  
		Last Modified: Thu, 02 Mar 2023 10:02:54 GMT  
		Size: 320.1 MB (320124567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1c72e0fd371f9c714089012adcf6c98ed8080f4deff364d7a44de73ff3461adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.3 MB (541317672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a8986d4118bbbad30dc006f061f1a1a5b0a87432c21eec2616480cf9d2d62c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:52 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:37:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:17 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:17 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:17 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e67562eaa79cf5c3d0c20d52a796769a8e752042a88822c034467fde45f9f`  
		Last Modified: Thu, 02 Mar 2023 07:38:39 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b373918e7ca45f4b0a3e6774b789a7119c3b3f11bf8a31a4bffb5eedd5ba0983`  
		Last Modified: Thu, 02 Mar 2023 07:38:39 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f830c2b3bca661c9eb4fa6b1c768bc4c8a9c06f9edfdc18d2c1efa5f7ebf6f`  
		Last Modified: Thu, 02 Mar 2023 07:38:51 GMT  
		Size: 320.0 MB (319982101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5.0`

```console
$ docker pull neo4j@sha256:8ce64b419712ffde6540457bc689db6b3b0490c8181719183693421b87a8b053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5.0` - linux; amd64

```console
$ docker pull neo4j@sha256:a9229cc31018c53d3fe7bb6d61723c2df50d7a81176722405adb54ea62781c65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a856d660b7eb78bfc8ff8440d1313a80b8754f09c8f33717732732a1d77aeda`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:39 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:00:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:00:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:00:53 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:00:53 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:00:54 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:00:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:00:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8035abbeafe764bf626a88951af419f66543beb1fdca2e21a8bc813233bf0722`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f507dd7037e462494f7e92ff5f6f2b6fe172b8a49c5e174b09b14986cd0e3`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a33c3e8a4092fde738023c7028eadde2c63aaf7ec763b76492eec2776030a6d`  
		Last Modified: Thu, 02 Mar 2023 10:02:19 GMT  
		Size: 115.2 MB (115196107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:72d6325c0d6601283c27c40ae3c13294073bee70d71c8042f49a0a492f1ec624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354da8b4ed8ec16ec88326e6de40d64674a252e13ffd6d9406973639820f73cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:35 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:36:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:36:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:36:47 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:36:47 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:36:47 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:36:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:36:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818b02e934fe24a985972eec0c2fff40a667e3ee49d1c25cde836dca2be07cf`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e884a6459a84c8d9ec181eb931feae2853c28fb2a165811fbcb3d33a9ca4ab0`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 8.4 KB (8423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f59750abf14b5acbedee984371b6e0edcb920352fd8633bb7c81ca6fcbbcf`  
		Last Modified: Thu, 02 Mar 2023 07:38:20 GMT  
		Size: 115.1 MB (115051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5.0-community`

```console
$ docker pull neo4j@sha256:8ce64b419712ffde6540457bc689db6b3b0490c8181719183693421b87a8b053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a9229cc31018c53d3fe7bb6d61723c2df50d7a81176722405adb54ea62781c65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a856d660b7eb78bfc8ff8440d1313a80b8754f09c8f33717732732a1d77aeda`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:39 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:00:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:00:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:00:53 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:00:53 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:00:54 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:00:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:00:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8035abbeafe764bf626a88951af419f66543beb1fdca2e21a8bc813233bf0722`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f507dd7037e462494f7e92ff5f6f2b6fe172b8a49c5e174b09b14986cd0e3`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a33c3e8a4092fde738023c7028eadde2c63aaf7ec763b76492eec2776030a6d`  
		Last Modified: Thu, 02 Mar 2023 10:02:19 GMT  
		Size: 115.2 MB (115196107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:72d6325c0d6601283c27c40ae3c13294073bee70d71c8042f49a0a492f1ec624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354da8b4ed8ec16ec88326e6de40d64674a252e13ffd6d9406973639820f73cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:35 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:36:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:36:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:36:47 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:36:47 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:36:47 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:36:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:36:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818b02e934fe24a985972eec0c2fff40a667e3ee49d1c25cde836dca2be07cf`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e884a6459a84c8d9ec181eb931feae2853c28fb2a165811fbcb3d33a9ca4ab0`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 8.4 KB (8423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f59750abf14b5acbedee984371b6e0edcb920352fd8633bb7c81ca6fcbbcf`  
		Last Modified: Thu, 02 Mar 2023 07:38:20 GMT  
		Size: 115.1 MB (115051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.5.0-enterprise`

```console
$ docker pull neo4j@sha256:99b5a2b5d2e18178fdbbb76d581f59d7ad9942d5e0d3d33ad9369a992eb0c5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.5.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:3c4b6ff757af0150f7633d6071830274bf44dba1a2761e048ad933f294113af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.0 MB (543986466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2c8de2eca7f4dcf77ec19df279f7edc21681782af93972591b03b889d116f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:59 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:01:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:16 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:16 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a134df60b1a1a5cab9f66081b40bb30fdd5a95887ceb76c51e97cf5254d699`  
		Last Modified: Thu, 02 Mar 2023 10:02:36 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4d3dd0a7fd30e76d65e49ac99622673782e32a34c1d04b3b7b906ec34b368a`  
		Last Modified: Thu, 02 Mar 2023 10:02:37 GMT  
		Size: 8.4 KB (8419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa7bf53d99f43f081283e07e457d8279863bf7a857b4b1abf38e8524ea9cf67`  
		Last Modified: Thu, 02 Mar 2023 10:02:54 GMT  
		Size: 320.1 MB (320124567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.5.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1c72e0fd371f9c714089012adcf6c98ed8080f4deff364d7a44de73ff3461adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.3 MB (541317672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a8986d4118bbbad30dc006f061f1a1a5b0a87432c21eec2616480cf9d2d62c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:52 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:37:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:17 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:17 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:17 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e67562eaa79cf5c3d0c20d52a796769a8e752042a88822c034467fde45f9f`  
		Last Modified: Thu, 02 Mar 2023 07:38:39 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b373918e7ca45f4b0a3e6774b789a7119c3b3f11bf8a31a4bffb5eedd5ba0983`  
		Last Modified: Thu, 02 Mar 2023 07:38:39 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f830c2b3bca661c9eb4fa6b1c768bc4c8a9c06f9edfdc18d2c1efa5f7ebf6f`  
		Last Modified: Thu, 02 Mar 2023 07:38:51 GMT  
		Size: 320.0 MB (319982101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:8ce64b419712ffde6540457bc689db6b3b0490c8181719183693421b87a8b053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:a9229cc31018c53d3fe7bb6d61723c2df50d7a81176722405adb54ea62781c65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a856d660b7eb78bfc8ff8440d1313a80b8754f09c8f33717732732a1d77aeda`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:39 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:00:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:00:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:00:53 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:00:53 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:00:54 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:00:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:00:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8035abbeafe764bf626a88951af419f66543beb1fdca2e21a8bc813233bf0722`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f507dd7037e462494f7e92ff5f6f2b6fe172b8a49c5e174b09b14986cd0e3`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a33c3e8a4092fde738023c7028eadde2c63aaf7ec763b76492eec2776030a6d`  
		Last Modified: Thu, 02 Mar 2023 10:02:19 GMT  
		Size: 115.2 MB (115196107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:72d6325c0d6601283c27c40ae3c13294073bee70d71c8042f49a0a492f1ec624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354da8b4ed8ec16ec88326e6de40d64674a252e13ffd6d9406973639820f73cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:35 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:36:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:36:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:36:47 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:36:47 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:36:47 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:36:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:36:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818b02e934fe24a985972eec0c2fff40a667e3ee49d1c25cde836dca2be07cf`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e884a6459a84c8d9ec181eb931feae2853c28fb2a165811fbcb3d33a9ca4ab0`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 8.4 KB (8423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f59750abf14b5acbedee984371b6e0edcb920352fd8633bb7c81ca6fcbbcf`  
		Last Modified: Thu, 02 Mar 2023 07:38:20 GMT  
		Size: 115.1 MB (115051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:99b5a2b5d2e18178fdbbb76d581f59d7ad9942d5e0d3d33ad9369a992eb0c5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:3c4b6ff757af0150f7633d6071830274bf44dba1a2761e048ad933f294113af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.0 MB (543986466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f2c8de2eca7f4dcf77ec19df279f7edc21681782af93972591b03b889d116f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:58 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:59 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:01:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:01:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:01:16 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:01:16 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:01:16 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:01:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:01:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a134df60b1a1a5cab9f66081b40bb30fdd5a95887ceb76c51e97cf5254d699`  
		Last Modified: Thu, 02 Mar 2023 10:02:36 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4d3dd0a7fd30e76d65e49ac99622673782e32a34c1d04b3b7b906ec34b368a`  
		Last Modified: Thu, 02 Mar 2023 10:02:37 GMT  
		Size: 8.4 KB (8419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa7bf53d99f43f081283e07e457d8279863bf7a857b4b1abf38e8524ea9cf67`  
		Last Modified: Thu, 02 Mar 2023 10:02:54 GMT  
		Size: 320.1 MB (320124567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1c72e0fd371f9c714089012adcf6c98ed8080f4deff364d7a44de73ff3461adf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.3 MB (541317672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a8986d4118bbbad30dc006f061f1a1a5b0a87432c21eec2616480cf9d2d62c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4e7a26d5ed0a89fce2c7f94dc756586f0e666f7d756e3fd1c4a0fddea98bfa46 NEO4J_TARBALL=neo4j-enterprise-5.5.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:51 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:52 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:37:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:37:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:37:17 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:37:17 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:37:17 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:37:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:37:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e67562eaa79cf5c3d0c20d52a796769a8e752042a88822c034467fde45f9f`  
		Last Modified: Thu, 02 Mar 2023 07:38:39 GMT  
		Size: 3.9 KB (3887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b373918e7ca45f4b0a3e6774b789a7119c3b3f11bf8a31a4bffb5eedd5ba0983`  
		Last Modified: Thu, 02 Mar 2023 07:38:39 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f830c2b3bca661c9eb4fa6b1c768bc4c8a9c06f9edfdc18d2c1efa5f7ebf6f`  
		Last Modified: Thu, 02 Mar 2023 07:38:51 GMT  
		Size: 320.0 MB (319982101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:8ce64b419712ffde6540457bc689db6b3b0490c8181719183693421b87a8b053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:a9229cc31018c53d3fe7bb6d61723c2df50d7a81176722405adb54ea62781c65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339058009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a856d660b7eb78bfc8ff8440d1313a80b8754f09c8f33717732732a1d77aeda`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 10:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 10:00:38 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 10:00:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 10:00:39 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 10:00:53 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 10:00:53 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 10:00:53 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 10:00:53 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 10:00:54 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 10:00:54 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 10:00:54 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8035abbeafe764bf626a88951af419f66543beb1fdca2e21a8bc813233bf0722`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 3.9 KB (3861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f507dd7037e462494f7e92ff5f6f2b6fe172b8a49c5e174b09b14986cd0e3`  
		Last Modified: Thu, 02 Mar 2023 10:02:13 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a33c3e8a4092fde738023c7028eadde2c63aaf7ec763b76492eec2776030a6d`  
		Last Modified: Thu, 02 Mar 2023 10:02:19 GMT  
		Size: 115.2 MB (115196107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:72d6325c0d6601283c27c40ae3c13294073bee70d71c8042f49a0a492f1ec624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336386877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354da8b4ed8ec16ec88326e6de40d64674a252e13ffd6d9406973639820f73cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 07:07:04 GMT
COPY dir:47c117bbc947c5c1164b5a20eeec0ba16c306f5991a85f22c54db31ca24ce4a8 in /opt/java/openjdk 
# Thu, 02 Mar 2023 07:36:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3834cf8393f11d02e96e37b15ceeb4319f56cf1d323076ca242a35750c94bd99 NEO4J_TARBALL=neo4j-community-5.5.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 02 Mar 2023 07:36:34 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
# Thu, 02 Mar 2023 07:36:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Thu, 02 Mar 2023 07:36:35 GMT
COPY multi:0673d6d1ec30168cf718a05272e8f73bf29e38f3da625fb17d18eb955eb48a71 in /startup/ 
# Thu, 02 Mar 2023 07:36:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.5.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 07:36:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 07:36:47 GMT
WORKDIR /var/lib/neo4j
# Thu, 02 Mar 2023 07:36:47 GMT
VOLUME [/data /logs]
# Thu, 02 Mar 2023 07:36:47 GMT
EXPOSE 7473 7474 7687
# Thu, 02 Mar 2023 07:36:47 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 07:36:47 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee2a535b626ac45b3b701a33ede28cb7ec44388615e651313d6818cbca5d626`  
		Last Modified: Thu, 02 Mar 2023 07:20:21 GMT  
		Size: 191.3 MB (191260449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d818b02e934fe24a985972eec0c2fff40a667e3ee49d1c25cde836dca2be07cf`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e884a6459a84c8d9ec181eb931feae2853c28fb2a165811fbcb3d33a9ca4ab0`  
		Last Modified: Thu, 02 Mar 2023 07:38:15 GMT  
		Size: 8.4 KB (8423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902f59750abf14b5acbedee984371b6e0edcb920352fd8633bb7c81ca6fcbbcf`  
		Last Modified: Thu, 02 Mar 2023 07:38:20 GMT  
		Size: 115.1 MB (115051303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
