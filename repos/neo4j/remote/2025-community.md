## `neo4j:2025-community`

```console
$ docker pull neo4j@sha256:59cd732e9c6eb4a3a6e1bf77c1c55234e4712366c5aa2c5a963f68b3eba1846f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-community` - linux; amd64

```console
$ docker pull neo4j@sha256:559b947ab6e101ad8685d48cbaec726177d87c9052e7171afb7b003d8941cae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401733032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a75538cebf6b7b7cc2a4e1ddf4351f3628d8549ce2b6a620c92fa462f1673f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:31:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:31:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:31:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=69ade165e3347a132dea6664fce7fda86f391a7aefb1ab00f21ce940ea692f09 NEO4J_TARBALL=neo4j-community-2025.10.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Sat, 08 Nov 2025 18:31:27 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
# Sat, 08 Nov 2025 18:31:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Sat, 08 Nov 2025 18:31:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Sat, 08 Nov 2025 18:31:48 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:31:48 GMT
WORKDIR /var/lib/neo4j
# Sat, 08 Nov 2025 18:31:48 GMT
VOLUME [/data /logs]
# Sat, 08 Nov 2025 18:31:48 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Sat, 08 Nov 2025 18:31:48 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:31:48 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b9a7b1cfffaf8e61fd6d16e25791e0365145426ca0170b78f7eb319c4ee983`  
		Last Modified: Sat, 08 Nov 2025 21:45:29 GMT  
		Size: 157.8 MB (157825975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9033f62a34a35260d80ad873e24af59eefb263f4113e36e22a08227abab1cb00`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 3.8 KB (3847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d39790eb196fbdbd3ff93b698a14cbf92a8d7532ab303cc2ad9b2b5b46c081`  
		Last Modified: Sat, 08 Nov 2025 18:32:36 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74076ca7441fbe5c828ade0c06b1448ba1dc6ba92ee54b3ca402ea172fd60fa6`  
		Last Modified: Sat, 08 Nov 2025 21:46:15 GMT  
		Size: 213.6 MB (213634563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8efc85602b58ca39c0a90f1b26e77d123753231deaeb9b58ff73067074cbb3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4630358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e9534d181394250bccc65c8cc216d12c6fb5163c42c58fa3b5adbd52216ea9`

```dockerfile
```

-	Layers:
	-	`sha256:cded5eaa4d6a845b97626a53656c3487f479948c4ef8942f052b26d69f02174d`  
		Last Modified: Sat, 08 Nov 2025 21:43:18 GMT  
		Size: 4.6 MB (4606293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfab16391a7beab1881a8031809db296c27c7d5b56fe5ac84eb9efe07937160f`  
		Last Modified: Sat, 08 Nov 2025 21:43:19 GMT  
		Size: 24.1 KB (24065 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d59aec5f8723c4b2bf6a911102614332b5e5dd5d32234ceccd2d97784397103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.7 MB (397746574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c1bca4107dc757023483b7bc86b0b58330837274899eee9dfae552e3e8f417`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:29:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:29:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:29:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=69ade165e3347a132dea6664fce7fda86f391a7aefb1ab00f21ce940ea692f09 NEO4J_TARBALL=neo4j-community-2025.10.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Sat, 08 Nov 2025 18:29:59 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
# Sat, 08 Nov 2025 18:29:59 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Sat, 08 Nov 2025 18:30:00 GMT
COPY ./local-package/* /startup/ # buildkit
# Sat, 08 Nov 2025 18:30:19 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.10.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Sat, 08 Nov 2025 18:30:19 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:30:19 GMT
WORKDIR /var/lib/neo4j
# Sat, 08 Nov 2025 18:30:19 GMT
VOLUME [/data /logs]
# Sat, 08 Nov 2025 18:30:19 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Sat, 08 Nov 2025 18:30:19 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Sat, 08 Nov 2025 18:30:19 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39ad4862e4150ac5692cfc8359fc246289e12b9732fd8b6b38cc7a72a215e8`  
		Last Modified: Sat, 08 Nov 2025 21:46:07 GMT  
		Size: 156.1 MB (156107661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3fc262435be9a13e34dd99fe1486368bdf08c11c44ad352773ed38d273f668`  
		Last Modified: Sat, 08 Nov 2025 18:31:13 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b9811722cff8e5331b2b25831532bb7e507fea5276ecbfdfb88ec024d2bbf3`  
		Last Modified: Sat, 08 Nov 2025 18:31:13 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e005cc427480360f7b7c2ab0b44202c63fef1fec9440486c1d9c0111e2fb424`  
		Last Modified: Sat, 08 Nov 2025 21:46:20 GMT  
		Size: 212.9 MB (212876441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8bd2986aea625cfb87abc2050c92a08c45eb6973935533c6dc7cd9e0db333d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4604573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2eb3a2cebda929ac1371a88b2f89227efca1922a69c7d86fc3a930a1061d901`

```dockerfile
```

-	Layers:
	-	`sha256:aad1a41a34ed6eef49b7afc41872b4e19d9d6a01957e9d8ebf6c2f38a255843d`  
		Last Modified: Sat, 08 Nov 2025 21:43:24 GMT  
		Size: 4.6 MB (4580218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ca339d9eac514c8642196be4c73cd2001834e9e92d9afae9d284fac59f5601`  
		Last Modified: Sat, 08 Nov 2025 21:43:25 GMT  
		Size: 24.4 KB (24355 bytes)  
		MIME: application/vnd.in-toto+json
