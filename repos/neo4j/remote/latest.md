## `neo4j:latest`

```console
$ docker pull neo4j@sha256:17073aaf68a7a48332ebd8de2e9de9833ba58f8301542b8a0b7d27a861a0c2dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:92c78bc1fb0ede58dcd0bd7707d8222de50ebf02b76a9c2a274e64d78d5cd43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368611410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f9c534ffcdb2085e63e96976c5a50a789d52127e2a196103b15774600fc22f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 19:42:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 19:42:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820 NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 19:42:32 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 19:42:32 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 19:42:56 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 08 May 2026 19:42:56 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:42:56 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 19:42:56 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 19:42:56 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 19:42:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:42:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c932e6872b37fb626b9c05f0eddc412f9c275d7aa4f870bb5f174f0aaae9873`  
		Last Modified: Fri, 08 May 2026 19:43:20 GMT  
		Size: 92.6 MB (92574597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d762d1e7f090cb0bf40d55506760f4311a7a4c3ab766e710fb50391aae899c6c`  
		Last Modified: Fri, 08 May 2026 19:43:16 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c358cd3a9b4035d65e6eeec7792e4b1f73c9383d5b2b272ce05368c1e43039fc`  
		Last Modified: Fri, 08 May 2026 19:43:22 GMT  
		Size: 246.2 MB (246246533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:2d80067e37b6cdbb4944848ee13e8e95c5a5de17b81fd2005bb0deec88a57c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4382468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e194934bcf467bf3cbc17d3d8389432e4dec32203fa2f105dd11ae066eb556f5`

```dockerfile
```

-	Layers:
	-	`sha256:1a5e2da9cbcdd8e9e795a3d21e4932ab3b33d638c3681eb40832ba5780924f42`  
		Last Modified: Fri, 08 May 2026 19:43:17 GMT  
		Size: 4.4 MB (4359959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:049ffb801f7082880882b3789c1c09c76a7860581a953fafae8c54e7f08318b8`  
		Last Modified: Fri, 08 May 2026 19:43:16 GMT  
		Size: 22.5 KB (22509 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e0782dface6d02e668d8ed03e9f464a6a71dec51dc1ae74b7c525741d8936e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (367009699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4bee5718828ef14cd555479761f3127f08a3a85ffe0f524b98e4dcacd27a2a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 19:44:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 19:44:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=fd750466b1247c0d1ef09a84c614f7e045793b30dfa277148e8da71646598820 NEO4J_TARBALL=neo4j-community-2026.04.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 08 May 2026 19:44:24 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
# Fri, 08 May 2026 19:44:24 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 08 May 2026 19:44:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.04.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 08 May 2026 19:44:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 19:44:48 GMT
WORKDIR /var/lib/neo4j
# Fri, 08 May 2026 19:44:48 GMT
VOLUME [/data /logs]
# Fri, 08 May 2026 19:44:48 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 08 May 2026 19:44:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:44:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56773b23bca52a56da64a33aa56f2cff55dda1429453079fd182f9eab97055d4`  
		Last Modified: Fri, 08 May 2026 19:45:14 GMT  
		Size: 91.5 MB (91542245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732a6bf296c27a30bc2ef3e8b97bc375b0e5eb93f4173209847b515360edb213`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e804ea3cc2390bfb637b64390c7afb011f9f48b5bcb38b53893b697e783561`  
		Last Modified: Fri, 08 May 2026 19:45:16 GMT  
		Size: 245.3 MB (245313758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:84fa9f5847ed5a7271b21effbde9ea98f6a1916e882efe5a1d58a3e5a3f60549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4377313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45fdf57a2e2bec04090fbd2612c904a72e210fe76003e39cda7b693c52eaacb`

```dockerfile
```

-	Layers:
	-	`sha256:cad25747e39723a3f6cab5e2fea716e56fc9235f84de69e709c5be1127747725`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 4.4 MB (4354530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d55612f83a521e0c6e87c0365b1681e5cf6c466944bef7a9526a294efe36f8`  
		Last Modified: Fri, 08 May 2026 19:45:10 GMT  
		Size: 22.8 KB (22783 bytes)  
		MIME: application/vnd.in-toto+json
