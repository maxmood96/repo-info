## `neo4j:latest`

```console
$ docker pull neo4j@sha256:211c4afab9a7b082980ab1eb9001361715f77ee178f7f090714422a4becb3c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:56182061dba6477e38b38fab9228a8d8b3fd379bb54e9000924285aaa15f1ae2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292667360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f7a2ea94a8fcefe9bba2810c226c0b16746112357ce44fce18c7971afee2e6`
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
# Fri, 13 Oct 2023 13:41:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=adf9e7915f5c10dfa4daf9eab79852660887eac3c3e165741fce48415c0b6f34 NEO4J_TARBALL=neo4j-community-5.12.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 13:41:53 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
# Fri, 13 Oct 2023 13:41:54 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 13:41:54 GMT
COPY multi:f4e8828c26bc3c80f7c5af331adb809a61a5b929b6f67c8cd774aa23152e75a5 in /startup/ 
# Fri, 13 Oct 2023 13:42:06 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 13:42:06 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 13:42:07 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 13:42:07 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 13:42:07 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 13:42:07 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 13:42:07 GMT
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
	-	`sha256:c914fe955feeeab83f55468268488827160e81da12f49208aee1c10064f71ebb`  
		Last Modified: Fri, 13 Oct 2023 13:44:11 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecab2cd70e508cfc34c9bf99b59c814ee8127a30b8859830997e3f90d5a71ef0`  
		Last Modified: Fri, 13 Oct 2023 13:44:11 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e9d048cd1fed8a8982ba408690188da0f5aebba9edb7be559935ba736326507`  
		Last Modified: Fri, 13 Oct 2023 13:44:17 GMT  
		Size: 116.5 MB (116460495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5d55b6539d384a59cd3d360cd82c0ed685d27778cdb67091298411d4edd2b94b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (289975112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbe398484d671b3ff1f33f30ab944d3582fe901cd3183ffe12d13fcfaa76541`
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
# Fri, 13 Oct 2023 08:24:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=adf9e7915f5c10dfa4daf9eab79852660887eac3c3e165741fce48415c0b6f34 NEO4J_TARBALL=neo4j-community-5.12.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 13 Oct 2023 08:24:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
# Fri, 13 Oct 2023 08:24:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Fri, 13 Oct 2023 08:24:44 GMT
COPY multi:f4e8828c26bc3c80f7c5af331adb809a61a5b929b6f67c8cd774aa23152e75a5 in /startup/ 
# Fri, 13 Oct 2023 08:25:00 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.12.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:25:00 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:25:01 GMT
WORKDIR /var/lib/neo4j
# Fri, 13 Oct 2023 08:25:01 GMT
VOLUME [/data /logs]
# Fri, 13 Oct 2023 08:25:01 GMT
EXPOSE 7473 7474 7687
# Fri, 13 Oct 2023 08:25:01 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 13 Oct 2023 08:25:01 GMT
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
	-	`sha256:ba338634711f1809a35e510b957cca4dcca371e43f2ee5348d966dc9c0e296e7`  
		Last Modified: Fri, 13 Oct 2023 08:27:11 GMT  
		Size: 3.9 KB (3885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daae60f36315c44a5b4d868ebde65c3cd6d5fef09bbc080e33afc80617ee7e6b`  
		Last Modified: Fri, 13 Oct 2023 08:27:11 GMT  
		Size: 9.4 KB (9433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1919500396f351b7f65ca9c6137dc7d40139e33c1a0f221268b934a5f5fe88ed`  
		Last Modified: Fri, 13 Oct 2023 08:27:18 GMT  
		Size: 116.4 MB (116354187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
