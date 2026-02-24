## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:d277d007c8660c74c0ac588a8ef68bbd6476f12f1f7ce41e7bafc08f1a840aaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:c209dec01dd84ffb604ea584dbb08c7e3bcf14e30e7e7e36edc1993408ac9b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404720410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e10d711141371523e096879b672ec73fd8a1683ba9132e0fc776794d5c5ee09`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:25:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:25:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:25:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f026977b1559a9a5e796faf6b0d3da3ecf8fae4d2bfb3a3c01ce9980f8010de2 NEO4J_TARBALL=neo4j-community-2026.01.4-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 24 Feb 2026 19:25:07 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
# Tue, 24 Feb 2026 19:25:07 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 24 Feb 2026 19:25:07 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 24 Feb 2026 19:25:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 24 Feb 2026 19:25:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:25:28 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Feb 2026 19:25:28 GMT
VOLUME [/data /logs]
# Tue, 24 Feb 2026 19:25:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 24 Feb 2026 19:25:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:25:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186dbcb50ba7e0fa60e9a0f13eb080786239dfa3b4b978b5b0acab1b03d309a1`  
		Last Modified: Tue, 24 Feb 2026 19:25:54 GMT  
		Size: 157.9 MB (157857099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6e8a4a576a64eea783455f04ad22252061e87e1f405e54babfb28c90e137b3`  
		Last Modified: Tue, 24 Feb 2026 19:25:48 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456633b4d8670681438def06b5c100af4ce5773cf2cb86c994d3dfdf7aacc37b`  
		Last Modified: Tue, 24 Feb 2026 19:25:48 GMT  
		Size: 10.2 KB (10191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3251493413bada87eaa3b74e0d5b9bbd1bb81d00900c5aecdfb4ef64a43fb53`  
		Last Modified: Tue, 24 Feb 2026 19:25:55 GMT  
		Size: 216.6 MB (216590867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ce27172a1e13ac578f41d3124bb85a07698206177d0d174f6b4998ecf3bdea11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6571e28830b993ed4bb6eaa70bb340c0761af8a4d6c4fe8130db97c3864f96`

```dockerfile
```

-	Layers:
	-	`sha256:182351c1ff729a40a4d33f32fd3d571aca2c1079a2a9678746fbe9d6095a7079`  
		Last Modified: Tue, 24 Feb 2026 19:25:48 GMT  
		Size: 4.6 MB (4621699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfbf4c9abf188f7c55531b41cf670e8464d32568ccfb4676f26c43ffbdee750d`  
		Last Modified: Tue, 24 Feb 2026 19:25:48 GMT  
		Size: 21.6 KB (21624 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ae2361be1e925dc2bb5cbd2fc2462de3d6d3efcc5c1ebeb84bb397ec8fca26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400729404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41326433158732cd13ee5a5ba45fdf324ecb74974d3a69753ade964276eb6a9e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:29:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:29:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:29:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=f026977b1559a9a5e796faf6b0d3da3ecf8fae4d2bfb3a3c01ce9980f8010de2 NEO4J_TARBALL=neo4j-community-2026.01.4-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 24 Feb 2026 19:29:48 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
# Tue, 24 Feb 2026 19:29:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 24 Feb 2026 19:29:48 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 24 Feb 2026 19:30:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 24 Feb 2026 19:30:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:30:08 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Feb 2026 19:30:08 GMT
VOLUME [/data /logs]
# Tue, 24 Feb 2026 19:30:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 24 Feb 2026 19:30:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:30:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6adae4bc35152abd7082e0419e00dd61bd4338f21e9f040114b1ac5fe21a9e2`  
		Last Modified: Tue, 24 Feb 2026 19:30:35 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96959de38cbdcaeac36d55b6636e466a7fe4987426344527d35b55f16fc3bed`  
		Last Modified: Tue, 24 Feb 2026 19:30:30 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307e21451fbcf3b6a90a89c4c37d668fad0ac24ff96f59eb9122cd959d83c8d3`  
		Last Modified: Tue, 24 Feb 2026 19:30:30 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335c1e433c731e42fc209fc6b71528b931584a9da575d5f01325aebb683207cb`  
		Last Modified: Tue, 24 Feb 2026 19:30:36 GMT  
		Size: 215.8 MB (215837754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ae418e888042a9066539a7ee25f2f60973cb4dfcfd1b867351b192c7aa3eb18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4617345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b7057638aa2f217411601e6683e51e3120e86c7366616f52a781992348d4e5`

```dockerfile
```

-	Layers:
	-	`sha256:55c7c01f067f344e439f8cf87c5160151c2ad2e9392a9001223dc09ed4da438c`  
		Last Modified: Tue, 24 Feb 2026 19:30:30 GMT  
		Size: 4.6 MB (4595528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9242a7736aa67d37f3d8aafef98403418d3307fa2d1ae1abef7b70a84f231e6`  
		Last Modified: Tue, 24 Feb 2026 19:30:30 GMT  
		Size: 21.8 KB (21817 bytes)  
		MIME: application/vnd.in-toto+json
