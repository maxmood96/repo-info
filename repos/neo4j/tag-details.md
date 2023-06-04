<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.21`](#neo4j4421)
-	[`neo4j:4.4.21-community`](#neo4j4421-community)
-	[`neo4j:4.4.21-enterprise`](#neo4j4421-enterprise)
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
$ docker pull neo4j@sha256:32de52398381672ab5b7912241cb03e1fdd0ea5b09b701a13931e09d93749823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:80df631fa3424ea09ea6e41f2378c4c3e9455510e4b2fefe0fa08bec14b15c23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347510915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b81646db386d8cbc450a7153019f2e309da88f16627c846113c47557f6fd79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:47:00 GMT
COPY dir:99fc054d8f67589023f9478fc6ae691114aff76e696d34d4988a30c767727d32 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:47:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:47:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Sun, 04 Jun 2023 15:47:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:47:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Sun, 04 Jun 2023 15:47:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:47:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:47:13 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:47:13 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:47:13 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:47:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:47:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b15966c6e6f35dd8e58820ec8f308c3885c7f159b583feaea99f8df7696d22`  
		Last Modified: Sun, 04 Jun 2023 15:48:58 GMT  
		Size: 198.5 MB (198549755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faa17a2ec7616c0c51e5e8d7d70696ef8483a2d433cf6ae12205a1092addb89`  
		Last Modified: Sun, 04 Jun 2023 15:48:44 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0bb4bf1b1fce2b58be94e3320fcd97164af4aaf039181b74a2d7957c25700c`  
		Last Modified: Sun, 04 Jun 2023 15:48:44 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e029a9c01a1493bc59f376e27020d5851a307c0beeaeaca6257cb5f0ab848`  
		Last Modified: Sun, 04 Jun 2023 15:48:51 GMT  
		Size: 117.5 MB (117545011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4b37645e26dfc8aac6852a22685ae98ef638a2b562ccbb88a27e46ad71efcf1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342791699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ff0882b7e434afdf253834c48043986047cdcb1efae2c67da5675b583a5f4d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:13 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:13 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d74853288fb9d3db14568370550a2ecfed9ecea2d47eb2c8b3dc7104e543e`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0976adc224137844c0460002fcd029bd93300b5cd0ea684f85769bd1cb853`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267da01b61f5b481ce02f9ad2cfcf05186f68e008bfdc9bc7b653f183594a98`  
		Last Modified: Fri, 02 Jun 2023 01:46:44 GMT  
		Size: 117.4 MB (117402148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:32de52398381672ab5b7912241cb03e1fdd0ea5b09b701a13931e09d93749823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:80df631fa3424ea09ea6e41f2378c4c3e9455510e4b2fefe0fa08bec14b15c23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347510915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b81646db386d8cbc450a7153019f2e309da88f16627c846113c47557f6fd79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:47:00 GMT
COPY dir:99fc054d8f67589023f9478fc6ae691114aff76e696d34d4988a30c767727d32 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:47:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:47:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Sun, 04 Jun 2023 15:47:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:47:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Sun, 04 Jun 2023 15:47:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:47:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:47:13 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:47:13 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:47:13 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:47:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:47:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b15966c6e6f35dd8e58820ec8f308c3885c7f159b583feaea99f8df7696d22`  
		Last Modified: Sun, 04 Jun 2023 15:48:58 GMT  
		Size: 198.5 MB (198549755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faa17a2ec7616c0c51e5e8d7d70696ef8483a2d433cf6ae12205a1092addb89`  
		Last Modified: Sun, 04 Jun 2023 15:48:44 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0bb4bf1b1fce2b58be94e3320fcd97164af4aaf039181b74a2d7957c25700c`  
		Last Modified: Sun, 04 Jun 2023 15:48:44 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e029a9c01a1493bc59f376e27020d5851a307c0beeaeaca6257cb5f0ab848`  
		Last Modified: Sun, 04 Jun 2023 15:48:51 GMT  
		Size: 117.5 MB (117545011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4b37645e26dfc8aac6852a22685ae98ef638a2b562ccbb88a27e46ad71efcf1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342791699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ff0882b7e434afdf253834c48043986047cdcb1efae2c67da5675b583a5f4d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:13 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:13 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d74853288fb9d3db14568370550a2ecfed9ecea2d47eb2c8b3dc7104e543e`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0976adc224137844c0460002fcd029bd93300b5cd0ea684f85769bd1cb853`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267da01b61f5b481ce02f9ad2cfcf05186f68e008bfdc9bc7b653f183594a98`  
		Last Modified: Fri, 02 Jun 2023 01:46:44 GMT  
		Size: 117.4 MB (117402148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:5fd3afd8caf0fa558879aa952e0a6bd7a3673b9d15fa0c8c362a4a8c3c7d3d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:853d807998d8fdcb9902dd6e514f19d359c1d0f3ccbce33f010121f82a55bbb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.2 MB (447177027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a925bf37e42dd9b7b62bb3450c3127ada46230e159bc78e1e4a0f1e88ba79b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:47:00 GMT
COPY dir:99fc054d8f67589023f9478fc6ae691114aff76e696d34d4988a30c767727d32 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Sun, 04 Jun 2023 15:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:47:18 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Sun, 04 Jun 2023 15:47:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:47:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:47:31 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:47:31 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:47:31 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:47:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:47:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b15966c6e6f35dd8e58820ec8f308c3885c7f159b583feaea99f8df7696d22`  
		Last Modified: Sun, 04 Jun 2023 15:48:58 GMT  
		Size: 198.5 MB (198549755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0323f8b8c6b99867d38ccca46c21d9ad442234117c4cf25cd11e429fadd453a1`  
		Last Modified: Sun, 04 Jun 2023 15:49:09 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3940f4bdeba7011a03f51b43a49b26376b5eabf3a7ea74ccfef8b4e8efe76c7`  
		Last Modified: Sun, 04 Jun 2023 15:49:09 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbf1994ff8c59960c952d89671bad42401c3e8690b075f8eae815d8ec7ad4f8`  
		Last Modified: Sun, 04 Jun 2023 15:49:19 GMT  
		Size: 217.2 MB (217211125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:dcc4d672b419d757c6306e5dec6183736a570538b426db2f2218d73a29fb4ea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.5 MB (442457305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff27e143becfe2604ca3962b963209ccc6245e7374343a7e4deec8da1bc5c568`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:17 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dfbd0d60b628088706570a5418eac35a21a37bac09c9c191bf016e33ddafc6`  
		Last Modified: Fri, 02 Jun 2023 01:46:56 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185a593214eaf66f24ba4304503486e7b38f41aee427196b1075c22e540533d3`  
		Last Modified: Fri, 02 Jun 2023 01:46:55 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068e7342b690ce5986d46141bf21ae24b1be0c005c3956a171848bb603ac5be`  
		Last Modified: Fri, 02 Jun 2023 01:47:03 GMT  
		Size: 217.1 MB (217067754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.21`

```console
$ docker pull neo4j@sha256:32de52398381672ab5b7912241cb03e1fdd0ea5b09b701a13931e09d93749823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.21` - linux; amd64

```console
$ docker pull neo4j@sha256:80df631fa3424ea09ea6e41f2378c4c3e9455510e4b2fefe0fa08bec14b15c23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347510915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b81646db386d8cbc450a7153019f2e309da88f16627c846113c47557f6fd79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:47:00 GMT
COPY dir:99fc054d8f67589023f9478fc6ae691114aff76e696d34d4988a30c767727d32 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:47:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:47:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Sun, 04 Jun 2023 15:47:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:47:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Sun, 04 Jun 2023 15:47:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:47:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:47:13 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:47:13 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:47:13 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:47:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:47:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b15966c6e6f35dd8e58820ec8f308c3885c7f159b583feaea99f8df7696d22`  
		Last Modified: Sun, 04 Jun 2023 15:48:58 GMT  
		Size: 198.5 MB (198549755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faa17a2ec7616c0c51e5e8d7d70696ef8483a2d433cf6ae12205a1092addb89`  
		Last Modified: Sun, 04 Jun 2023 15:48:44 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0bb4bf1b1fce2b58be94e3320fcd97164af4aaf039181b74a2d7957c25700c`  
		Last Modified: Sun, 04 Jun 2023 15:48:44 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e029a9c01a1493bc59f376e27020d5851a307c0beeaeaca6257cb5f0ab848`  
		Last Modified: Sun, 04 Jun 2023 15:48:51 GMT  
		Size: 117.5 MB (117545011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.21` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4b37645e26dfc8aac6852a22685ae98ef638a2b562ccbb88a27e46ad71efcf1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342791699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ff0882b7e434afdf253834c48043986047cdcb1efae2c67da5675b583a5f4d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:13 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:13 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d74853288fb9d3db14568370550a2ecfed9ecea2d47eb2c8b3dc7104e543e`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0976adc224137844c0460002fcd029bd93300b5cd0ea684f85769bd1cb853`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267da01b61f5b481ce02f9ad2cfcf05186f68e008bfdc9bc7b653f183594a98`  
		Last Modified: Fri, 02 Jun 2023 01:46:44 GMT  
		Size: 117.4 MB (117402148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.21-community`

```console
$ docker pull neo4j@sha256:32de52398381672ab5b7912241cb03e1fdd0ea5b09b701a13931e09d93749823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.21-community` - linux; amd64

```console
$ docker pull neo4j@sha256:80df631fa3424ea09ea6e41f2378c4c3e9455510e4b2fefe0fa08bec14b15c23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347510915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b81646db386d8cbc450a7153019f2e309da88f16627c846113c47557f6fd79`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:47:00 GMT
COPY dir:99fc054d8f67589023f9478fc6ae691114aff76e696d34d4988a30c767727d32 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:47:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:47:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Sun, 04 Jun 2023 15:47:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:47:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Sun, 04 Jun 2023 15:47:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:47:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:47:13 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:47:13 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:47:13 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:47:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:47:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b15966c6e6f35dd8e58820ec8f308c3885c7f159b583feaea99f8df7696d22`  
		Last Modified: Sun, 04 Jun 2023 15:48:58 GMT  
		Size: 198.5 MB (198549755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8faa17a2ec7616c0c51e5e8d7d70696ef8483a2d433cf6ae12205a1092addb89`  
		Last Modified: Sun, 04 Jun 2023 15:48:44 GMT  
		Size: 3.9 KB (3860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0bb4bf1b1fce2b58be94e3320fcd97164af4aaf039181b74a2d7957c25700c`  
		Last Modified: Sun, 04 Jun 2023 15:48:44 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e029a9c01a1493bc59f376e27020d5851a307c0beeaeaca6257cb5f0ab848`  
		Last Modified: Sun, 04 Jun 2023 15:48:51 GMT  
		Size: 117.5 MB (117545011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.21-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4b37645e26dfc8aac6852a22685ae98ef638a2b562ccbb88a27e46ad71efcf1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342791699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ff0882b7e434afdf253834c48043986047cdcb1efae2c67da5675b583a5f4d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba7cef86b9b2f0743f3855f4543f81fa46d07c5c724a56e5f4e0f437e20cc3a5 NEO4J_TARBALL=neo4j-community-4.4.21-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:03 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:12 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:13 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:13 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:13 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:13 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:13 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:13 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573d74853288fb9d3db14568370550a2ecfed9ecea2d47eb2c8b3dc7104e543e`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 3.9 KB (3886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b0976adc224137844c0460002fcd029bd93300b5cd0ea684f85769bd1cb853`  
		Last Modified: Fri, 02 Jun 2023 01:46:39 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7267da01b61f5b481ce02f9ad2cfcf05186f68e008bfdc9bc7b653f183594a98`  
		Last Modified: Fri, 02 Jun 2023 01:46:44 GMT  
		Size: 117.4 MB (117402148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:4.4.21-enterprise`

```console
$ docker pull neo4j@sha256:5fd3afd8caf0fa558879aa952e0a6bd7a3673b9d15fa0c8c362a4a8c3c7d3d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:4.4.21-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:853d807998d8fdcb9902dd6e514f19d359c1d0f3ccbce33f010121f82a55bbb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.2 MB (447177027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a925bf37e42dd9b7b62bb3450c3127ada46230e159bc78e1e4a0f1e88ba79b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:47:00 GMT
COPY dir:99fc054d8f67589023f9478fc6ae691114aff76e696d34d4988a30c767727d32 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:47:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:47:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Sun, 04 Jun 2023 15:47:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:47:18 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Sun, 04 Jun 2023 15:47:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:47:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:47:31 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:47:31 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:47:31 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:47:32 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:47:32 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b15966c6e6f35dd8e58820ec8f308c3885c7f159b583feaea99f8df7696d22`  
		Last Modified: Sun, 04 Jun 2023 15:48:58 GMT  
		Size: 198.5 MB (198549755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0323f8b8c6b99867d38ccca46c21d9ad442234117c4cf25cd11e429fadd453a1`  
		Last Modified: Sun, 04 Jun 2023 15:49:09 GMT  
		Size: 3.9 KB (3858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3940f4bdeba7011a03f51b43a49b26376b5eabf3a7ea74ccfef8b4e8efe76c7`  
		Last Modified: Sun, 04 Jun 2023 15:49:09 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbf1994ff8c59960c952d89671bad42401c3e8690b075f8eae815d8ec7ad4f8`  
		Last Modified: Sun, 04 Jun 2023 15:49:19 GMT  
		Size: 217.2 MB (217211125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:4.4.21-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:dcc4d672b419d757c6306e5dec6183736a570538b426db2f2218d73a29fb4ea7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.5 MB (442457305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff27e143becfe2604ca3962b963209ccc6245e7374343a7e4deec8da1bc5c568`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0305b7bdefa4efae16d0a72e19bda6e79150b7423e739d789dd945e355a389f4 NEO4J_TARBALL=neo4j-enterprise-4.4.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:45:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
# Fri, 02 Jun 2023 01:45:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:45:17 GMT
COPY multi:444df161c1a5ee60f2235df18d0f75c88fbf992084b1774572a5350de0772b1f in /startup/ 
# Fri, 02 Jun 2023 01:45:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.21-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:45:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:45:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:45:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:45:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:45:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:45:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8dfbd0d60b628088706570a5418eac35a21a37bac09c9c191bf016e33ddafc6`  
		Last Modified: Fri, 02 Jun 2023 01:46:56 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185a593214eaf66f24ba4304503486e7b38f41aee427196b1075c22e540533d3`  
		Last Modified: Fri, 02 Jun 2023 01:46:55 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2068e7342b690ce5986d46141bf21ae24b1be0c005c3956a171848bb603ac5be`  
		Last Modified: Fri, 02 Jun 2023 01:47:03 GMT  
		Size: 217.1 MB (217067754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5`

```console
$ docker pull neo4j@sha256:c7e1ac5f324b53f4350028e7dd592a5fee4e05cfd2331d592eee5fd9be2230bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:b24262a37be8b8164fa5267ea0a99d7df079305433dcb9514aeaca2732333fe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b829fca46b401da6536094ffccfbb4606cadea80b57239d8cdde029ba41f3e40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:28 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:29 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:29 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb418fbc2f88d8589a01694879fafadb25e7ca97906422a111a713218727da91`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85da60185c79dfcd1d4aa2720a748f419850b68bde070ca9dca8423b6ac6e7ef`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498509078bd9af94c253845b28c8d0b42644601e76ce1bca961bbf5bf731516a`  
		Last Modified: Sun, 04 Jun 2023 15:47:51 GMT  
		Size: 114.7 MB (114688518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:c7e1ac5f324b53f4350028e7dd592a5fee4e05cfd2331d592eee5fd9be2230bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b24262a37be8b8164fa5267ea0a99d7df079305433dcb9514aeaca2732333fe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b829fca46b401da6536094ffccfbb4606cadea80b57239d8cdde029ba41f3e40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:28 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:29 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:29 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb418fbc2f88d8589a01694879fafadb25e7ca97906422a111a713218727da91`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85da60185c79dfcd1d4aa2720a748f419850b68bde070ca9dca8423b6ac6e7ef`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498509078bd9af94c253845b28c8d0b42644601e76ce1bca961bbf5bf731516a`  
		Last Modified: Sun, 04 Jun 2023 15:47:51 GMT  
		Size: 114.7 MB (114688518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:ed2eea7ca3e4617d8f5316864cf63cff8df944940f7c7f3fc97c550be93f7a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:60c6d96ce58cd168b3b0ebe7555b1cf0401015dead12424dde9314893d535600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d474349738994bc3ffde434841a77c86316b1333cf9fbebf8021c0151244389`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:34 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:51 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:51 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:51 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb79857bcff3fc082a69e5a92e057d73f43395cf486d90aa28db5bfd3b8f39c`  
		Last Modified: Sun, 04 Jun 2023 15:48:17 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04121cb607176a5548278819f1c2ea65378e4129616eed44432d26033bb22c07`  
		Last Modified: Sun, 04 Jun 2023 15:48:17 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1e47071fadbf0ddde1390f7395f9f7eb44f9e7443d669aa479eb092586b7`  
		Last Modified: Sun, 04 Jun 2023 15:48:32 GMT  
		Size: 379.7 MB (379683346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cee38c97292f52ea37daabbecb008f2b4c49f428f95ea9f38caf94427362dd2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2121f2b76488aa36e163ff2bc0bcdf65a5a73a08d6ed8510bf4eac9c3237358`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:40 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:57 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:57 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:58 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac10763bf8b8833986f70a55f383df991114bfbe6839f9904f06468f0d0f80a8`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009719f6debaabbf1870471b661a8390e01b458827a6114d1027064a867d80`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183826f6c0789438a8b134ed5bd2d1249d148c71659c553e53bfc0a0c96db33d`  
		Last Modified: Fri, 02 Jun 2023 01:46:27 GMT  
		Size: 379.5 MB (379541395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8`

```console
$ docker pull neo4j@sha256:c7e1ac5f324b53f4350028e7dd592a5fee4e05cfd2331d592eee5fd9be2230bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8` - linux; amd64

```console
$ docker pull neo4j@sha256:b24262a37be8b8164fa5267ea0a99d7df079305433dcb9514aeaca2732333fe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b829fca46b401da6536094ffccfbb4606cadea80b57239d8cdde029ba41f3e40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:28 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:29 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:29 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb418fbc2f88d8589a01694879fafadb25e7ca97906422a111a713218727da91`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85da60185c79dfcd1d4aa2720a748f419850b68bde070ca9dca8423b6ac6e7ef`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498509078bd9af94c253845b28c8d0b42644601e76ce1bca961bbf5bf731516a`  
		Last Modified: Sun, 04 Jun 2023 15:47:51 GMT  
		Size: 114.7 MB (114688518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8-community`

```console
$ docker pull neo4j@sha256:c7e1ac5f324b53f4350028e7dd592a5fee4e05cfd2331d592eee5fd9be2230bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b24262a37be8b8164fa5267ea0a99d7df079305433dcb9514aeaca2732333fe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b829fca46b401da6536094ffccfbb4606cadea80b57239d8cdde029ba41f3e40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:28 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:29 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:29 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb418fbc2f88d8589a01694879fafadb25e7ca97906422a111a713218727da91`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85da60185c79dfcd1d4aa2720a748f419850b68bde070ca9dca8423b6ac6e7ef`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498509078bd9af94c253845b28c8d0b42644601e76ce1bca961bbf5bf731516a`  
		Last Modified: Sun, 04 Jun 2023 15:47:51 GMT  
		Size: 114.7 MB (114688518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8-enterprise`

```console
$ docker pull neo4j@sha256:ed2eea7ca3e4617d8f5316864cf63cff8df944940f7c7f3fc97c550be93f7a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:60c6d96ce58cd168b3b0ebe7555b1cf0401015dead12424dde9314893d535600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d474349738994bc3ffde434841a77c86316b1333cf9fbebf8021c0151244389`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:34 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:51 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:51 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:51 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb79857bcff3fc082a69e5a92e057d73f43395cf486d90aa28db5bfd3b8f39c`  
		Last Modified: Sun, 04 Jun 2023 15:48:17 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04121cb607176a5548278819f1c2ea65378e4129616eed44432d26033bb22c07`  
		Last Modified: Sun, 04 Jun 2023 15:48:17 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1e47071fadbf0ddde1390f7395f9f7eb44f9e7443d669aa479eb092586b7`  
		Last Modified: Sun, 04 Jun 2023 15:48:32 GMT  
		Size: 379.7 MB (379683346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cee38c97292f52ea37daabbecb008f2b4c49f428f95ea9f38caf94427362dd2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2121f2b76488aa36e163ff2bc0bcdf65a5a73a08d6ed8510bf4eac9c3237358`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:40 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:57 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:57 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:58 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac10763bf8b8833986f70a55f383df991114bfbe6839f9904f06468f0d0f80a8`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009719f6debaabbf1870471b661a8390e01b458827a6114d1027064a867d80`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183826f6c0789438a8b134ed5bd2d1249d148c71659c553e53bfc0a0c96db33d`  
		Last Modified: Fri, 02 Jun 2023 01:46:27 GMT  
		Size: 379.5 MB (379541395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0`

```console
$ docker pull neo4j@sha256:c7e1ac5f324b53f4350028e7dd592a5fee4e05cfd2331d592eee5fd9be2230bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0` - linux; amd64

```console
$ docker pull neo4j@sha256:b24262a37be8b8164fa5267ea0a99d7df079305433dcb9514aeaca2732333fe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b829fca46b401da6536094ffccfbb4606cadea80b57239d8cdde029ba41f3e40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:28 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:29 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:29 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb418fbc2f88d8589a01694879fafadb25e7ca97906422a111a713218727da91`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85da60185c79dfcd1d4aa2720a748f419850b68bde070ca9dca8423b6ac6e7ef`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498509078bd9af94c253845b28c8d0b42644601e76ce1bca961bbf5bf731516a`  
		Last Modified: Sun, 04 Jun 2023 15:47:51 GMT  
		Size: 114.7 MB (114688518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0-community`

```console
$ docker pull neo4j@sha256:c7e1ac5f324b53f4350028e7dd592a5fee4e05cfd2331d592eee5fd9be2230bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b24262a37be8b8164fa5267ea0a99d7df079305433dcb9514aeaca2732333fe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b829fca46b401da6536094ffccfbb4606cadea80b57239d8cdde029ba41f3e40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:28 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:29 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:29 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb418fbc2f88d8589a01694879fafadb25e7ca97906422a111a713218727da91`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85da60185c79dfcd1d4aa2720a748f419850b68bde070ca9dca8423b6ac6e7ef`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498509078bd9af94c253845b28c8d0b42644601e76ce1bca961bbf5bf731516a`  
		Last Modified: Sun, 04 Jun 2023 15:47:51 GMT  
		Size: 114.7 MB (114688518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:5.8.0-enterprise`

```console
$ docker pull neo4j@sha256:ed2eea7ca3e4617d8f5316864cf63cff8df944940f7c7f3fc97c550be93f7a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5.8.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:60c6d96ce58cd168b3b0ebe7555b1cf0401015dead12424dde9314893d535600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d474349738994bc3ffde434841a77c86316b1333cf9fbebf8021c0151244389`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:34 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:51 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:51 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:51 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb79857bcff3fc082a69e5a92e057d73f43395cf486d90aa28db5bfd3b8f39c`  
		Last Modified: Sun, 04 Jun 2023 15:48:17 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04121cb607176a5548278819f1c2ea65378e4129616eed44432d26033bb22c07`  
		Last Modified: Sun, 04 Jun 2023 15:48:17 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1e47071fadbf0ddde1390f7395f9f7eb44f9e7443d669aa479eb092586b7`  
		Last Modified: Sun, 04 Jun 2023 15:48:32 GMT  
		Size: 379.7 MB (379683346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5.8.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cee38c97292f52ea37daabbecb008f2b4c49f428f95ea9f38caf94427362dd2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2121f2b76488aa36e163ff2bc0bcdf65a5a73a08d6ed8510bf4eac9c3237358`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:40 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:57 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:57 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:58 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac10763bf8b8833986f70a55f383df991114bfbe6839f9904f06468f0d0f80a8`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009719f6debaabbf1870471b661a8390e01b458827a6114d1027064a867d80`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183826f6c0789438a8b134ed5bd2d1249d148c71659c553e53bfc0a0c96db33d`  
		Last Modified: Fri, 02 Jun 2023 01:46:27 GMT  
		Size: 379.5 MB (379541395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:community`

```console
$ docker pull neo4j@sha256:c7e1ac5f324b53f4350028e7dd592a5fee4e05cfd2331d592eee5fd9be2230bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:b24262a37be8b8164fa5267ea0a99d7df079305433dcb9514aeaca2732333fe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b829fca46b401da6536094ffccfbb4606cadea80b57239d8cdde029ba41f3e40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:28 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:29 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:29 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb418fbc2f88d8589a01694879fafadb25e7ca97906422a111a713218727da91`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85da60185c79dfcd1d4aa2720a748f419850b68bde070ca9dca8423b6ac6e7ef`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498509078bd9af94c253845b28c8d0b42644601e76ce1bca961bbf5bf731516a`  
		Last Modified: Sun, 04 Jun 2023 15:47:51 GMT  
		Size: 114.7 MB (114688518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:ed2eea7ca3e4617d8f5316864cf63cff8df944940f7c7f3fc97c550be93f7a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:60c6d96ce58cd168b3b0ebe7555b1cf0401015dead12424dde9314893d535600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.7 MB (603679975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d474349738994bc3ffde434841a77c86316b1333cf9fbebf8021c0151244389`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:34 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:50 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:51 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:51 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:51 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:51 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:51 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:52 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb79857bcff3fc082a69e5a92e057d73f43395cf486d90aa28db5bfd3b8f39c`  
		Last Modified: Sun, 04 Jun 2023 15:48:17 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04121cb607176a5548278819f1c2ea65378e4129616eed44432d26033bb22c07`  
		Last Modified: Sun, 04 Jun 2023 15:48:17 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406b1e47071fadbf0ddde1390f7395f9f7eb44f9e7443d669aa479eb092586b7`  
		Last Modified: Sun, 04 Jun 2023 15:48:32 GMT  
		Size: 379.7 MB (379683346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cee38c97292f52ea37daabbecb008f2b4c49f428f95ea9f38caf94427362dd2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 MB (600994454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2121f2b76488aa36e163ff2bc0bcdf65a5a73a08d6ed8510bf4eac9c3237358`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=851d82c37c2d90784a5a2382880935d09b0784a6d2ea16c1062a6191ccd34c98 NEO4J_TARBALL=neo4j-enterprise-5.8.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:39 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:40 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:57 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:57 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:57 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:58 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac10763bf8b8833986f70a55f383df991114bfbe6839f9904f06468f0d0f80a8`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 3.9 KB (3889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009719f6debaabbf1870471b661a8390e01b458827a6114d1027064a867d80`  
		Last Modified: Fri, 02 Jun 2023 01:46:12 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183826f6c0789438a8b134ed5bd2d1249d148c71659c553e53bfc0a0c96db33d`  
		Last Modified: Fri, 02 Jun 2023 01:46:27 GMT  
		Size: 379.5 MB (379541395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:c7e1ac5f324b53f4350028e7dd592a5fee4e05cfd2331d592eee5fd9be2230bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:b24262a37be8b8164fa5267ea0a99d7df079305433dcb9514aeaca2732333fe5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338685139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b829fca46b401da6536094ffccfbb4606cadea80b57239d8cdde029ba41f3e40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 04 Jun 2023 15:46:08 GMT
COPY dir:3373f6afb162f98a7f4cbaf8f00acdb618287ff4fa7a1aab9b85d36a1c441565 in /opt/java/openjdk 
# Sun, 04 Jun 2023 15:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Sun, 04 Jun 2023 15:46:09 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Sun, 04 Jun 2023 15:46:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Sun, 04 Jun 2023 15:46:10 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Sun, 04 Jun 2023 15:46:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Sun, 04 Jun 2023 15:46:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 04 Jun 2023 15:46:28 GMT
WORKDIR /var/lib/neo4j
# Sun, 04 Jun 2023 15:46:29 GMT
VOLUME [/data /logs]
# Sun, 04 Jun 2023 15:46:29 GMT
EXPOSE 7473 7474 7687
# Sun, 04 Jun 2023 15:46:29 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sun, 04 Jun 2023 15:46:29 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbea4c47d2874ef2a6db3eefb275207fba2e91d942a6eec0d61092c061f352`  
		Last Modified: Sun, 04 Jun 2023 15:47:59 GMT  
		Size: 192.6 MB (192580407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb418fbc2f88d8589a01694879fafadb25e7ca97906422a111a713218727da91`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 3.9 KB (3859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85da60185c79dfcd1d4aa2720a748f419850b68bde070ca9dca8423b6ac6e7ef`  
		Last Modified: Sun, 04 Jun 2023 15:47:45 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498509078bd9af94c253845b28c8d0b42644601e76ce1bca961bbf5bf731516a`  
		Last Modified: Sun, 04 Jun 2023 15:47:51 GMT  
		Size: 114.7 MB (114688518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e254d2f63d360dc7de966beb0e0f8bb7564fca6773de5454f3059361b885c6e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.0 MB (335998072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5f55d4d1d0e427517d2422053d0a0245539054bac2cc0278537e36fce06d09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=96d728c337804a255151c23ced29994a890ee4d4015fa3916e34a358f0d1cbd6 NEO4J_TARBALL=neo4j-community-5.8.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 02 Jun 2023 01:44:19 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
# Fri, 02 Jun 2023 01:44:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 02 Jun 2023 01:44:20 GMT
COPY multi:3bc0fa696e81224d7ba1974735ef93fe90797d02a5971b859ddbbdf878ae6a57 in /startup/ 
# Fri, 02 Jun 2023 01:44:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.8.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 01:44:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:44:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 02 Jun 2023 01:44:36 GMT
VOLUME [/data /logs]
# Fri, 02 Jun 2023 01:44:36 GMT
EXPOSE 7473 7474 7687
# Fri, 02 Jun 2023 01:44:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 02 Jun 2023 01:44:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c9f065f34a3ecb2f81e1f7625edafba53b45b0cdfb79bbaca94bac469740b`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 3.9 KB (3888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f423f3032e6b2093ccf1f8f4112dbcae5697c39abbdc311b98aba5bdaf8951`  
		Last Modified: Fri, 02 Jun 2023 01:45:50 GMT  
		Size: 8.8 KB (8767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b58ef591401cbb242046aa6af75c14588190bd09beae24be607cb315d22fd1c`  
		Last Modified: Fri, 02 Jun 2023 01:45:54 GMT  
		Size: 114.5 MB (114545014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
