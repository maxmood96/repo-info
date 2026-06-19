## `neo4j:2026-trixie`

```console
$ docker pull neo4j@sha256:e1f6d09837ebfd2a2de2008f2f0d9d497e8d27c4286a5422a608303d7c7d8af7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:d19a1e2aafe4d8026ce98cce5a1a75fb893deaf1a8b4b45ea38402caf26180ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.2 MB (371213942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c294e1ac1bc99d7e9c1934104b2e4371f786d6592ddf0729b749d6f5e6a16e27`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:13:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=bb753b4e9bcc331e90b968edd8da445e974090867ca825cc672defdad6066f0e NEO4J_TARBALL=neo4j-community-2026.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 19 Jun 2026 02:13:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
# Fri, 19 Jun 2026 02:13:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 19 Jun 2026 02:13:44 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 19 Jun 2026 02:13:44 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:44 GMT
WORKDIR /var/lib/neo4j
# Fri, 19 Jun 2026 02:13:44 GMT
VOLUME [/data /logs]
# Fri, 19 Jun 2026 02:13:44 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 19 Jun 2026 02:13:44 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 19 Jun 2026 02:13:44 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85725b1a35dd5e3f16336928c1a1047acb11646928c9c69ed9656422172ada7d`  
		Last Modified: Fri, 19 Jun 2026 02:14:07 GMT  
		Size: 92.6 MB (92574597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3f0aaa5565c50dd2c31010c99e165055627ca5209578be8af5516572a2fa83`  
		Last Modified: Fri, 19 Jun 2026 02:14:03 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c348f088413c3fd36f2a30c26ddde3d58ade8ed2281b031aa9b5a7f53df18d1`  
		Last Modified: Fri, 19 Jun 2026 02:14:10 GMT  
		Size: 248.8 MB (248843879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:1410019eaab865a63cd9538a59e5945890b898dac9f9b9e8d6f2f56dd9f95f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4385210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241ba0df90c144c907bd91bdf61dc2fec3d71403e95349e01b45bb406df9d76a`

```dockerfile
```

-	Layers:
	-	`sha256:7b7604ba13f2b46d54ef45cba88bf1393cad7a21dc91c19a255c10cbd8643e35`  
		Last Modified: Fri, 19 Jun 2026 02:14:04 GMT  
		Size: 4.4 MB (4362701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebcd1c43e7c6cd884b48f143d791ca162ec2511a56f9192836fd2aa5b0cb212f`  
		Last Modified: Fri, 19 Jun 2026 02:14:04 GMT  
		Size: 22.5 KB (22509 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a3abfb0fa664779986d408ca22b8c091b899e2cd852e895df5e06f5a27f50b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369616676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535bb65c881e8e03594f79c2e362bc0b2792e69b66c0e6462db44a80a31718c8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:13:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:13:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=bb753b4e9bcc331e90b968edd8da445e974090867ca825cc672defdad6066f0e NEO4J_TARBALL=neo4j-community-2026.05.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 19 Jun 2026 02:13:31 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
# Fri, 19 Jun 2026 02:13:31 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 19 Jun 2026 02:13:55 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2026.05.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 19 Jun 2026 02:13:55 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:13:56 GMT
WORKDIR /var/lib/neo4j
# Fri, 19 Jun 2026 02:13:56 GMT
VOLUME [/data /logs]
# Fri, 19 Jun 2026 02:13:56 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 19 Jun 2026 02:13:56 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 19 Jun 2026 02:13:56 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c102375c3329d037387397462d4ec97276b9396e1ca3f05372f254bee32baedd`  
		Last Modified: Fri, 19 Jun 2026 02:14:22 GMT  
		Size: 91.5 MB (91542250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a310f72ed3cafe87861bd6bf93f767c448ce2b0e4ca39feab2ccdcf0edd65136`  
		Last Modified: Fri, 19 Jun 2026 02:14:18 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a227d74b2d3ad224506fee63eb169bf0632ab0cc5b411bb4b01b38a1a5dda7cc`  
		Last Modified: Fri, 19 Jun 2026 02:14:25 GMT  
		Size: 247.9 MB (247915843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a31a3918ebcdd5353cd7297262993a913525ffc255598704266d7632943357e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc3be793af0d1ff56a1b98a07f1cfd02c1dd0a14880263bc83dab7deb11d598`

```dockerfile
```

-	Layers:
	-	`sha256:4ec03ff9210eafe903fef186cd8dabdc47fd4268640bc5c7c4e4f4278dc120e3`  
		Last Modified: Fri, 19 Jun 2026 02:14:18 GMT  
		Size: 4.4 MB (4357264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0839b3ce4ed11c1471a70c76f170d5b8afeec4f73d05f85518b1320b7bdc463`  
		Last Modified: Fri, 19 Jun 2026 02:14:18 GMT  
		Size: 22.8 KB (22783 bytes)  
		MIME: application/vnd.in-toto+json
