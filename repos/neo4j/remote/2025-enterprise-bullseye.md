## `neo4j:2025-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:a26511c6920517a5378daea9f7c674d5b81bde775aed8cda9123a0049eaadab7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0abe935cebb6c105d680f80ada100c9f8746b3dd0acfb95bdce86dc6a7afcf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.3 MB (544274277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d01b915c696e02594b6c30f5ef02a6371752e20c45f5f3ecb40d1838e7fa8f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:30:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:30:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:30:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6ddde9170f21067bde1dbb3f910d6f5faddf48026177e3c43d1410d4b5cd3b76 NEO4J_TARBALL=neo4j-enterprise-2025.10.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 14 Nov 2025 00:30:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
# Fri, 14 Nov 2025 00:30:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 14 Nov 2025 00:30:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 14 Nov 2025 00:30:36 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 14 Nov 2025 00:30:36 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:30:36 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Nov 2025 00:30:36 GMT
VOLUME [/data /logs]
# Fri, 14 Nov 2025 00:30:36 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 14 Nov 2025 00:30:36 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:36 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef55f998d9f2b0db7f7468f50eafb240e34afac5496eab941be6f5495833f495`  
		Last Modified: Fri, 14 Nov 2025 03:44:38 GMT  
		Size: 157.8 MB (157825955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb74d88565be14eef24d757019dcc4c460e3a23413f410a2a675e0c86b3baebd`  
		Last Modified: Fri, 14 Nov 2025 00:31:18 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19c7a4e483872bc32df64724fe60cec01fed401aed0c18cb69fba2ccd6d867`  
		Last Modified: Fri, 14 Nov 2025 00:31:17 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9435022e1b709663d60ab3b55680b537f6ef7e25faea9df1b818f92e2db7c5b1`  
		Last Modified: Fri, 14 Nov 2025 03:44:55 GMT  
		Size: 356.2 MB (356175835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ec1a07e2cf0f8759901414d61e2c31bc3004faa7777e4f715ecf5169b6594897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4873185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b41a91478d8d3006d95a53e30bbff09f83198e466626b26fdfa1a5fc6cfd00`

```dockerfile
```

-	Layers:
	-	`sha256:6f55591f1f71c9dd4ccc293185a9265e3f28ea18114209b204fb4e0cd9c4f855`  
		Last Modified: Fri, 14 Nov 2025 03:43:45 GMT  
		Size: 4.9 MB (4851525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17ffe689339d90f2fb4c8dbdb8a6492b004f4094bbc2ca2a6cf7d6e8a60e13be`  
		Last Modified: Fri, 14 Nov 2025 03:43:46 GMT  
		Size: 21.7 KB (21660 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d7c20d1d8a4b46b63cadc1a2dcbe39973d24fb46a3dc53cb5cc36d3261b9ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.3 MB (540288970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5762087b818c69e22381fefec3f26978efe44d10ec5efe2308c040a48a227c87`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:30:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6ddde9170f21067bde1dbb3f910d6f5faddf48026177e3c43d1410d4b5cd3b76 NEO4J_TARBALL=neo4j-enterprise-2025.10.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 14 Nov 2025 00:30:16 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
# Fri, 14 Nov 2025 00:30:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 14 Nov 2025 00:30:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 14 Nov 2025 00:30:39 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 14 Nov 2025 00:30:39 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:30:39 GMT
WORKDIR /var/lib/neo4j
# Fri, 14 Nov 2025 00:30:39 GMT
VOLUME [/data /logs]
# Fri, 14 Nov 2025 00:30:39 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 14 Nov 2025 00:30:39 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:30:39 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7e8ac80f1c9eb3ea2323889a22a736c82e20222db21c045bd106f00d318c63`  
		Last Modified: Fri, 14 Nov 2025 00:31:11 GMT  
		Size: 156.1 MB (156107671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108e7732fbaa621083fd8c6eb967dc69116d542ed1904156bca887689618cab2`  
		Last Modified: Fri, 14 Nov 2025 00:31:20 GMT  
		Size: 3.9 KB (3876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd21ea09c477df0ba4a117fb4fdac3f137b6fabd233d6c66bceb0ec0c216063`  
		Last Modified: Fri, 14 Nov 2025 00:31:20 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2398fccabdb711c9e335e60bc8171c7bfbd08f0dfd24e77f8cfeea08c33f9c7`  
		Last Modified: Fri, 14 Nov 2025 00:31:15 GMT  
		Size: 355.4 MB (355418818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab5016ff43f03a189682ba149fd221ee74367bbd65c2dd5144b6a6db34c58883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4847208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76df97cfbfa8e5f178ec8f7cab7aff4d616107061205178a9987fd174b6eb228`

```dockerfile
```

-	Layers:
	-	`sha256:6c019deb822820bf46873e58e2b79a6ed1ea1a62a0411ce4b7e34f879a6b0924`  
		Last Modified: Fri, 14 Nov 2025 03:43:53 GMT  
		Size: 4.8 MB (4825354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c280b0006d2465d3247aa1f7f32ea285066485d3ed6deeab2e8e6a184660c7`  
		Last Modified: Fri, 14 Nov 2025 03:43:54 GMT  
		Size: 21.9 KB (21854 bytes)  
		MIME: application/vnd.in-toto+json
