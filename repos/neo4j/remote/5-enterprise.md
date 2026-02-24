## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:5c0b71de4204d93a49ab840cf61c0aeee3559969d81e410ae84a1bca90320c45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:6390b75a1dcb3800a09f0a1cd44d80f62730f7c1564c245820a8668815feb0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.1 MB (699074428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a22d5a365c37948853bb3342b4c16e6f09dfc5d7ab792207546ef6c3cd94d75`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:25:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:25:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:25:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=053f019a4a5854e7676b7339bfc0f554091bf35d6be9f74a79e503480b0b7bda NEO4J_TARBALL=neo4j-enterprise-5.26.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 24 Feb 2026 19:25:36 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
# Tue, 24 Feb 2026 19:25:36 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 24 Feb 2026 19:26:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 24 Feb 2026 19:26:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:26:20 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Feb 2026 19:26:20 GMT
VOLUME [/data /logs]
# Tue, 24 Feb 2026 19:26:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 24 Feb 2026 19:26:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:26:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4af1b4ef45cb7decca2c0ada56e8e29c3c50eba0526398c050ea9cb3f30b9e`  
		Last Modified: Tue, 24 Feb 2026 19:26:57 GMT  
		Size: 157.9 MB (157857067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37833cb62ee2d7dc698d5e80b97e6f7d2b32e405865ef745dbcb9ee14ca7d2e0`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdef6dc50c9bed5b817b64b5870ae8356674be8555a697563f2a2c14616c86e`  
		Last Modified: Tue, 24 Feb 2026 19:27:16 GMT  
		Size: 511.4 MB (511428635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:43ffd9a37b58d98d185f069af14fa2034b99e9a24716612ab1ef48575b22818b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4677400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b794ac9375505ec6dc45114200e118f0aacc0c191572ec22e14e651e78b252`

```dockerfile
```

-	Layers:
	-	`sha256:2f64653556214b6f0b45e28dbd0d7d597fac78b48decb892fb5d34f83fe4540f`  
		Last Modified: Tue, 24 Feb 2026 19:26:51 GMT  
		Size: 4.7 MB (4658103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a50733e106077f499ed75bbefa6bb4fd3d9c7320eb5cd8e5016b77d21b93a3f0`  
		Last Modified: Tue, 24 Feb 2026 19:26:50 GMT  
		Size: 19.3 KB (19297 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:fc0f94bdbfa45f28d921d29092f3c60cc7d2236be79edc428143727e041a954a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.8 MB (696781193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b463a61dca200fa111c2aaf4fb5d9dfeff8082d75d2ebaaa4d1186078b33c0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:30:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:30:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:30:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=053f019a4a5854e7676b7339bfc0f554091bf35d6be9f74a79e503480b0b7bda NEO4J_TARBALL=neo4j-enterprise-5.26.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 24 Feb 2026 19:30:15 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
# Tue, 24 Feb 2026 19:30:15 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 24 Feb 2026 19:30:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 24 Feb 2026 19:30:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:30:46 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Feb 2026 19:30:46 GMT
VOLUME [/data /logs]
# Tue, 24 Feb 2026 19:30:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 24 Feb 2026 19:30:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:30:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c4b6e7fb0f050ef49246ff2a2a086263ae5b78d2cf5c3b335c840658feded2`  
		Last Modified: Tue, 24 Feb 2026 19:31:25 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0272a85e44ae49d529265c2be6f65f6ad11b1a232a3ce202435be2ee9853688`  
		Last Modified: Tue, 24 Feb 2026 19:31:19 GMT  
		Size: 10.1 KB (10064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb269a01a08ee167740e9f21d374425862009827e8053800028a6e9d2d481b19`  
		Last Modified: Tue, 24 Feb 2026 19:31:31 GMT  
		Size: 510.5 MB (510497907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:64752a5c81b4eef7f7d2890ac29c5e9d3df1d1e185a2dafe49ab9729371bfd00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4672008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7eb35b080070a455cb456a33cfbdaade9ac0d1edcd5e15060e8992b751df34`

```dockerfile
```

-	Layers:
	-	`sha256:a8d7aa7f594d4b5a447567c8bcfc19e217e4ec2d0858a38e900aae6de0bc62c3`  
		Last Modified: Tue, 24 Feb 2026 19:31:19 GMT  
		Size: 4.7 MB (4652557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:464189e90b050763370b659b8735d85617e0f8b3d261f47fa1aa51e676004343`  
		Last Modified: Tue, 24 Feb 2026 19:31:19 GMT  
		Size: 19.5 KB (19451 bytes)  
		MIME: application/vnd.in-toto+json
