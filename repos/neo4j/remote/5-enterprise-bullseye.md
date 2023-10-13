## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:928846ce083e266195c89ca03f200f3124b60c20ac7ee105ee859d3335d72ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:efdb7e094806d7135fb84e424a49b4518e86c757845b763320b47d937ffbfa3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.2 MB (566223359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dbfa7fb954b775fe4c5b1be1ec5d4d9050b47b0ad4fe03565a6a44969c2d51`
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
# Fri, 13 Oct 2023 13:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=282c8601cbcc04fc49dfefec305c1f3d824ba2cd16ea3d30721051bfcea05239 NEO4J_TARBALL=neo4j-enterprise-5.12.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 13:42:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.12.0-unix.tar.gz
# Fri, 13 Oct 2023 13:42:11 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.12.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 13:42:11 GMT
COPY multi:f4e8828c26bc3c80f7c5af331adb809a61a5b929b6f67c8cd774aa23152e75a5 in /startup/ 
# Fri, 13 Oct 2023 13:42:29 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.12.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 13:42:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 13:42:30 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 13:42:30 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 13:42:30 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 13:42:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 13:42:30 GMT
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
	-	`sha256:e279bea2bb333a2bd52e8bdfdc7265378ea2214f649c0558f1116cb77f6bcccf`  
		Last Modified: Fri, 13 Oct 2023 13:44:52 GMT  
		Size: 3.9 KB (3863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1866c12118bc2cf15faf9629da5fd9726620295db252bdc393b4da0c4fcc97f2`  
		Last Modified: Fri, 13 Oct 2023 13:44:52 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a18642114bf99a67c8a889c4ee9a615add659bd55e612da6c5885f62ff5385`  
		Last Modified: Fri, 13 Oct 2023 13:45:24 GMT  
		Size: 390.0 MB (390016493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:46b6ec989b05e4be1799a071a896f9ef19882aa8bfc50a49094c778dbaa13863
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.5 MB (563530269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863461614e03a5fcbf2c326ded45d525c07424eaa5749961fe25db1de2936658`
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
# Fri, 13 Oct 2023 08:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=282c8601cbcc04fc49dfefec305c1f3d824ba2cd16ea3d30721051bfcea05239 NEO4J_TARBALL=neo4j-enterprise-5.12.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 08:25:06 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.12.0-unix.tar.gz
# Fri, 13 Oct 2023 08:25:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.12.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 08:25:07 GMT
COPY multi:f4e8828c26bc3c80f7c5af331adb809a61a5b929b6f67c8cd774aa23152e75a5 in /startup/ 
# Fri, 13 Oct 2023 08:25:22 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.12.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:25:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:25:25 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 08:25:25 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 08:25:25 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 08:25:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 08:25:25 GMT
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
	-	`sha256:b5336e2c38c3c25c6b09915c5dfd7baa34bc307401799dde670af32877a6bbef`  
		Last Modified: Fri, 13 Oct 2023 08:27:54 GMT  
		Size: 3.9 KB (3884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147ab2079415ea92f65056ce4bf748f2176f94c0d9500771a58ff77b548199ea`  
		Last Modified: Fri, 13 Oct 2023 08:27:54 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3239a260b23f3eda03adcc21344fa2dcc0974e367838a07e3625c165937c3c`  
		Last Modified: Fri, 13 Oct 2023 08:28:14 GMT  
		Size: 389.9 MB (389909347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
