## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:a75003730d84a6d885ec47fee0cc62d5d59626199d0884286bb535921f68a011
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:ee06d200277d78a03dfd9054ebaf55f7c977475d74f92aad7e7f96d445f83511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305701012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6ff0f1bc9d31b7ed68622dbae5a7dc5f124b639d3551c62486154c2fc945d9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 00:38:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 00:38:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 00:38:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da87ec6d1d5f348815589fe1becce86f1c097ed72d30487669c4bba01ed622a7 NEO4J_TARBALL=neo4j-community-5.26.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 00:38:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
# Fri, 16 Jan 2026 00:38:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 00:38:05 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 00:38:24 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 00:38:24 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 00:38:24 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 00:38:24 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 00:38:24 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 00:38:24 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:38:24 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43926e388053c0c2b5eae4fad128c0c25d3ff58fa47c9038f9a541bf27c5f4f1`  
		Last Modified: Fri, 16 Jan 2026 03:45:10 GMT  
		Size: 144.8 MB (144847942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebbc5d3a212f27814a95d58dc6968c6b2352891c0d810a440372ae16e0fc14f`  
		Last Modified: Fri, 16 Jan 2026 00:38:43 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dfb3378488464e52459bf42bbccc87d6341a28fe5ab7c8bff337d45296a16e`  
		Last Modified: Fri, 16 Jan 2026 00:38:55 GMT  
		Size: 10.1 KB (10059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c1b4f15b7a24af8ac25e2226f5adbc478c59ce0dcd9fa6ddca640eb13f6da6`  
		Last Modified: Fri, 16 Jan 2026 01:39:29 GMT  
		Size: 130.6 MB (130580645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4d7285293320d0a5c8b1d4b20162ad4b352a8e70622cc575e131271534f554b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4504499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf5310d63b2ecf26e9fbafcfe92da62e0604ca16456a502e182c9fed5b9e09c`

```dockerfile
```

-	Layers:
	-	`sha256:5b6f90e437f2e40ab2a0cbd5ad7a8d8396504fb1029251ff529fc960c7505ddf`  
		Last Modified: Fri, 16 Jan 2026 00:38:44 GMT  
		Size: 4.5 MB (4481733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba6239fa737ca6e0b6a4b81821bbf239489178f3ed8aff1a7a6c27cab417e69`  
		Last Modified: Fri, 16 Jan 2026 03:44:46 GMT  
		Size: 22.8 KB (22766 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e096b019c14c6a6e1851c6cf01e19b155c04eaba2727fc2f9b3aeac0ffe27178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302266795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4709afb9c6e667756eb662cd201b099b05beeae96d00c0cdc607e2c1398493`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 00:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 00:40:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 00:40:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=da87ec6d1d5f348815589fe1becce86f1c097ed72d30487669c4bba01ed622a7 NEO4J_TARBALL=neo4j-community-5.26.19-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 00:40:41 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
# Fri, 16 Jan 2026 00:40:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 00:40:41 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 00:40:58 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.19-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 00:40:58 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 00:40:58 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 00:40:58 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 00:40:58 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 00:40:58 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 00:40:58 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff821ccfabff8ceec3a82cc1336547124bf970d8cc3a153e8ec04910530c3474`  
		Last Modified: Fri, 16 Jan 2026 00:41:21 GMT  
		Size: 143.7 MB (143679919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d869f4a735cd32d60178b604a0ca35bf68255ec0cf03fe30ca4f1a12b726c34`  
		Last Modified: Fri, 16 Jan 2026 00:41:26 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc576e44744de761aba17c7eb4cc0cdbe56bbd44b95bd0a72e2a9089fc8e7db`  
		Last Modified: Fri, 16 Jan 2026 00:41:26 GMT  
		Size: 10.1 KB (10063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4965c3743e1d580b7fd94bc4fac5aec77764c7f2c9a9ee12b718db8dce3ba653`  
		Last Modified: Fri, 16 Jan 2026 00:41:21 GMT  
		Size: 129.8 MB (129824396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e03d1abfd8539bc0405202cf6f5470f90d27eb204eafb6c7df2dbecd4c040f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4478617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b81df58bd09ee06914dc9b602c947d7d4feb4561666be04b16e003c6ed085a`

```dockerfile
```

-	Layers:
	-	`sha256:46b7afdd85dcb65849c5175b474ca0e38d5497189ff82819cf6c3b3f5b5e674c`  
		Last Modified: Fri, 16 Jan 2026 00:41:16 GMT  
		Size: 4.5 MB (4455610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a43ecc3aa31ecf280aa27366a4b89c2221d6c5a92a852d0d948202827f2d0fc`  
		Last Modified: Fri, 16 Jan 2026 03:44:51 GMT  
		Size: 23.0 KB (23007 bytes)  
		MIME: application/vnd.in-toto+json
