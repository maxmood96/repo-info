## `neo4j:5-enterprise-trixie`

```console
$ docker pull neo4j@sha256:de30cc7902775c842f0a7d0f40d89e09446268066af315be2900b7ed8be60299
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-trixie` - linux; amd64

```console
$ docker pull neo4j@sha256:1dd284a417de3d0688a7fe90967dfb4f0b796a58eb71184f34e0a96adebfebe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **699.1 MB (699071157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e132928b02019eca4e355100d7d6736eebabedf04641000e36a6f6fa055af0f3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:24:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=053f019a4a5854e7676b7339bfc0f554091bf35d6be9f74a79e503480b0b7bda NEO4J_TARBALL=neo4j-enterprise-5.26.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Feb 2026 21:24:33 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
# Tue, 17 Feb 2026 21:24:33 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Feb 2026 21:25:15 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Feb 2026 21:25:15 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:25:15 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Feb 2026 21:25:15 GMT
VOLUME [/data /logs]
# Tue, 17 Feb 2026 21:25:15 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Feb 2026 21:25:15 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:25:15 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0e066bb6a501f43dd47eb1e40be4e6e547868b0294b34dc8707dfe62e015bb`  
		Last Modified: Tue, 17 Feb 2026 21:25:50 GMT  
		Size: 157.9 MB (157857046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21b263de16e097800159cd28f17d793320ec084c942284c6a3775c453404a2e`  
		Last Modified: Tue, 17 Feb 2026 21:25:45 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628695988a7e3e546067dd08539cb3999d37847a87081ea3c7d4fe91903998e`  
		Last Modified: Tue, 17 Feb 2026 21:25:57 GMT  
		Size: 511.4 MB (511425421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:52c47d595861f42da134ab3aedc470fe84802ba0c65f523f6b98904a8f836f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4677400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a476523a3999f6e26f1c8bfb99395829fd7b7b70da51ae1de589ff52c0fd64`

```dockerfile
```

-	Layers:
	-	`sha256:2cfaeacfb05f314c22d9c75e1f31365dd286262e3a0338f4cd068e1f3a1bebf8`  
		Last Modified: Tue, 17 Feb 2026 21:25:45 GMT  
		Size: 4.7 MB (4658103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015831334afee6e5914f376a81740abc3e1b18c26ea0c0cc940937db6d213714`  
		Last Modified: Tue, 17 Feb 2026 21:25:45 GMT  
		Size: 19.3 KB (19297 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-trixie` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:044f37756f98652a006bf5498a751bfbab25c3d32650a023f9ec7e9805fbdf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **696.8 MB (696780004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70f5f36c27d6b215681511b35e06db94938a743663f5f42182a27137a4b5d59`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:24:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=053f019a4a5854e7676b7339bfc0f554091bf35d6be9f74a79e503480b0b7bda NEO4J_TARBALL=neo4j-enterprise-5.26.21-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Feb 2026 21:24:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
# Tue, 17 Feb 2026 21:24:45 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Feb 2026 21:25:16 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.21-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Feb 2026 21:25:16 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:25:16 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Feb 2026 21:25:16 GMT
VOLUME [/data /logs]
# Tue, 17 Feb 2026 21:25:16 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Feb 2026 21:25:16 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:25:16 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eb7e5a7c194125766bcc0bd87680cf1618cb36c0885b1534dbfa14b8e8c2f3`  
		Last Modified: Tue, 17 Feb 2026 21:25:33 GMT  
		Size: 156.1 MB (156133063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebae824c8fcee21a9736d668c99724fb332cc59555b3ccc2e73dd3591b38dc85`  
		Last Modified: Tue, 17 Feb 2026 21:25:47 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf4c3822450738574046827925b257646402719efbbb0c1e65bd9880dd86814`  
		Last Modified: Tue, 17 Feb 2026 21:25:58 GMT  
		Size: 510.5 MB (510496787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-trixie` - unknown; unknown

```console
$ docker pull neo4j@sha256:73c2a80f400abfcd49c759f4f8ace21296fcb6073dffb100a53ed1b835a7bf21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4672008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ac8fa6c8c89895a56107748671321cc17c0225db06f6badf4d193459090b31`

```dockerfile
```

-	Layers:
	-	`sha256:9f8f5f382a4fb5c09a2558121da65a9eca153d3d419b7762acee248a4e37103f`  
		Last Modified: Tue, 17 Feb 2026 21:25:47 GMT  
		Size: 4.7 MB (4652557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9b802d92dfaaf63fdd3f87a4080e46efdc8fbfeeaa95a98c4b51fc670250da1`  
		Last Modified: Tue, 17 Feb 2026 21:25:47 GMT  
		Size: 19.5 KB (19451 bytes)  
		MIME: application/vnd.in-toto+json
