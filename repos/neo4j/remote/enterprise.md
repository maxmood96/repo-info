## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:598479babc48baf43a51463780781034d95c8861de69de6384119984a66800fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b43013f0cd7d74e1e4497d3756cdb7ccb1b8b219bad3407c58956e215ef3a56f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432869622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f110c02412218cfb5462456b109fbccc713f6be834eb4eff160dcc02a1037b63`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:05:21 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 21 Nov 2022 19:25:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 21 Nov 2022 19:25:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Mon, 21 Nov 2022 19:25:32 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Mon, 21 Nov 2022 19:25:32 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Mon, 21 Nov 2022 19:25:52 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Mon, 21 Nov 2022 19:25:52 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Nov 2022 19:25:52 GMT
WORKDIR /var/lib/neo4j
# Mon, 21 Nov 2022 19:25:52 GMT
VOLUME [/data /logs]
# Mon, 21 Nov 2022 19:25:53 GMT
EXPOSE 7473 7474 7687
# Mon, 21 Nov 2022 19:25:53 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 21 Nov 2022 19:25:53 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e2f15985394be21a4e4a010fbea73bcb4ac9c162a40582171119a45451824`  
		Last Modified: Tue, 15 Nov 2022 13:08:12 GMT  
		Size: 192.4 MB (192431277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3472f19c8a5a24c108dc649a7497094ed5be4db2d33246bb3b0405224ac6bfc2`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 3.9 KB (3855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4e10d12e10c3659084ea62f78809a048ce5b0e3607f6cfff686434d0332bcd`  
		Last Modified: Mon, 21 Nov 2022 19:26:56 GMT  
		Size: 8.2 KB (8166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f71541831b0253791f32bf49c5dd3d9c3a0794bf23ea63b8584caa7fbe2bcf7`  
		Last Modified: Mon, 21 Nov 2022 19:27:06 GMT  
		Size: 209.0 MB (209013694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:90f8871f5adcc5ed41020731e3b7cd55e9dfcd9de2b31439ba4fc7e379f1af12
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430158153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05a45fbc4c5d91679ccfcca0f863645d1317c21c76c08137670f66a74a685e2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:17:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 06 Dec 2022 02:22:53 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Tue, 06 Dec 2022 04:03:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=4a32f8a2800b00f690e4fcca670d268d40b8080c55796de1e6c92e39589026eb NEO4J_TARBALL=neo4j-enterprise-5.2.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
# Tue, 06 Dec 2022 04:03:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j
# Tue, 06 Dec 2022 04:03:14 GMT
COPY multi:4c38b038fb207d3b3e018c6de201a35723320a0beef5d4b7a28a0fdf507334bd in /startup/ 
# Tue, 06 Dec 2022 04:03:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.2.0-unix.tar.gz
RUN apt update     && apt install -y curl gosu jq tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && apt-get -y purge --auto-remove curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:03:27 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 04:03:27 GMT
WORKDIR /var/lib/neo4j
# Tue, 06 Dec 2022 04:03:27 GMT
VOLUME [/data /logs]
# Tue, 06 Dec 2022 04:03:27 GMT
EXPOSE 7473 7474 7687
# Tue, 06 Dec 2022 04:03:27 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 06 Dec 2022 04:03:27 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838b5f3398d789eb4642eff775295a017b51ac8034f8a4c2f4ed800e7a30d07`  
		Last Modified: Tue, 06 Dec 2022 02:33:34 GMT  
		Size: 191.2 MB (191215233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1128db2f4b08bc6f628623eac1f80cc5279c0cdcd21f45b8739eb59a680c34c`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 3.9 KB (3883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0951e28fc5d1a0ac9065b81777666b227d565470fa92e3004b8cc1094beb4701`  
		Last Modified: Tue, 06 Dec 2022 04:04:54 GMT  
		Size: 8.2 KB (8165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8b160227ed7d13a3c1655a1fac0ee736792ee4d20a71884670c1dcd791b10c`  
		Last Modified: Tue, 06 Dec 2022 04:05:04 GMT  
		Size: 208.9 MB (208870552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
