## `neo4j:2025-community-bullseye`

```console
$ docker pull neo4j@sha256:5f13ef4de359fe6b40c1cd91d92e569762526db191d8e39db5442ae89cdb58be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:afebfc4e269ff940ccaf1597a80ae42f3eb44d2e473f4b00387f0f7b2e457350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.2 MB (404211181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2994d6fad6455bf62dfff119458c0280fb1e060afce7a08029c335ba17247e8d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 21:47:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 21:47:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 21:47:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=06c3d7b6cb9532e3ec2c03f24d076e3acac5abfe6d7394f855910d2c12f7c542 NEO4J_TARBALL=neo4j-community-2025.12.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 21:47:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
# Fri, 16 Jan 2026 21:47:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 21:47:15 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 21:47:34 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 21:47:34 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:47:34 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 21:47:34 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 21:47:34 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 21:47:34 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:47:34 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afeb8acade1189693a142c6e4dda362d6aa761b8ee0dc71b481272f87ff6793e`  
		Last Modified: Fri, 16 Jan 2026 21:47:59 GMT  
		Size: 157.8 MB (157826000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd65f839d7e9935f16d069e685e65e026efc19f51900395655c1c918d905c832`  
		Last Modified: Fri, 16 Jan 2026 21:48:09 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa8ed108e8f6183f3ae20ae6c7b50e76ff8dd0e7b822ac6a75ccd90ea248de6`  
		Last Modified: Fri, 16 Jan 2026 21:47:53 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0208c609eb21c77f3db441b89e5e09f548252b03762b2a1001101853ab7cf5bc`  
		Last Modified: Fri, 16 Jan 2026 21:48:02 GMT  
		Size: 216.1 MB (216112792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5589c92a0fb5f7691a4d452e4ac6ec4b56c2e9d9bc3404aa8d6e2afb10dc6cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4631249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bc52bc4104474dd060a22c728da36553a0aad1c036f89ab0523ce4c1e557ec`

```dockerfile
```

-	Layers:
	-	`sha256:0bbc0461957b0a78b3bcda68470020058bfc9259de2365d8adf8df8d40cd5ec9`  
		Last Modified: Fri, 16 Jan 2026 21:47:54 GMT  
		Size: 4.6 MB (4607183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117fffe39b6228afcd99d3c82b097a9a4f8804b66bbd669e80fef168d91bf2ff`  
		Last Modified: Fri, 16 Jan 2026 21:47:53 GMT  
		Size: 24.1 KB (24066 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f17cddb88d16352b46962a488a4f1a791990943df1d4bbe8fc6b1b8abff09571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.2 MB (400227199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2bc8dc78021ac4ba803d03e578b6b7eaf85dd5abd913b09cb9124ee30a6f78`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 21:47:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 21:47:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 21:47:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=06c3d7b6cb9532e3ec2c03f24d076e3acac5abfe6d7394f855910d2c12f7c542 NEO4J_TARBALL=neo4j-community-2025.12.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 16 Jan 2026 21:47:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
# Fri, 16 Jan 2026 21:47:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 16 Jan 2026 21:47:11 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 16 Jan 2026 21:47:30 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.12.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 16 Jan 2026 21:47:30 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 21:47:30 GMT
WORKDIR /var/lib/neo4j
# Fri, 16 Jan 2026 21:47:30 GMT
VOLUME [/data /logs]
# Fri, 16 Jan 2026 21:47:30 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 16 Jan 2026 21:47:30 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 16 Jan 2026 21:47:30 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0aaa68c1b9402dc36c13f5bc0e83cf3978a49eefb1df182364025ca54c3889`  
		Last Modified: Fri, 16 Jan 2026 21:47:58 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8af9f5554c25d8581edd844d622051bf67b889c2b0eaabdf3dd09965ed92f23`  
		Last Modified: Fri, 16 Jan 2026 21:48:05 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2172b3cbc09d866ad2b07bb1b84775d125b83a8c62371315cc66b1ce9faf0b5a`  
		Last Modified: Fri, 16 Jan 2026 21:47:53 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1669f242a83a5d70bccfe103b69bd6df0ad5368017437cd849ee18b4c4e1fc`  
		Last Modified: Fri, 16 Jan 2026 21:47:59 GMT  
		Size: 215.4 MB (215357127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d303d13649efdff37958f958f9a7c1bc2b54980b918fed64be875513f0c75127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4605463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a55db981ea6d3f1138494b2f637946929d6ecb042634bbe66bbfbabf1023721`

```dockerfile
```

-	Layers:
	-	`sha256:58509c28bdec07806394ac89d9012baaa61213abcfa86c23d3bb09730d282694`  
		Last Modified: Sat, 17 Jan 2026 00:43:29 GMT  
		Size: 4.6 MB (4581108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4db6ed8e15e4baa4b4c8d506a0aafaadbb72b4d0e9d28fcf5a57bda00736582f`  
		Last Modified: Fri, 16 Jan 2026 21:47:53 GMT  
		Size: 24.4 KB (24355 bytes)  
		MIME: application/vnd.in-toto+json
