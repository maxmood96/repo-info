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
