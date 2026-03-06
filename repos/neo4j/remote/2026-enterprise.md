## `neo4j:2026-enterprise`

```console
$ docker pull neo4j@sha256:99154ce8377f3b604562ef145bfbfd8fb5302affb0ceaff8abcce5a5ce9394d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:45310b3c1ed007b342d6fa96c104c2c86ea21f3a613dbf0ac4e991b321012bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.2 MB (511212633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b454a8f591e7442cde7221a6d07627265e59049f244094d1ddd5f7ec7e0334fa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 18:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Mar 2026 18:22:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Mar 2026 18:22:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3edc16e54b70b190f460fed9a5eb31e7e4e8c6a52aa823bff6b18dd2d2183c8a NEO4J_TARBALL=neo4j-enterprise-2026.02.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 06 Mar 2026 18:22:05 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.2-unix.tar.gz
# Fri, 06 Mar 2026 18:22:05 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 06 Mar 2026 18:22:41 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 06 Mar 2026 18:22:41 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:22:41 GMT
WORKDIR /var/lib/neo4j
# Fri, 06 Mar 2026 18:22:41 GMT
VOLUME [/data /logs]
# Fri, 06 Mar 2026 18:22:41 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 06 Mar 2026 18:22:41 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:22:41 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96588ace7b472f1bae0a868e2e1a2898d3bf54d6ff5502099f393d9a4b2f573`  
		Last Modified: Fri, 06 Mar 2026 18:23:08 GMT  
		Size: 92.3 MB (92256291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e5d3d9f1f7731d3d584dc0d6eef9e31e8bbce342422ad84b8a3a4974bfc3f9`  
		Last Modified: Fri, 06 Mar 2026 18:23:04 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9578f09131cef43b91cc480fae0ab014721fa7774b4df602479b2582cc3a17`  
		Last Modified: Fri, 06 Mar 2026 18:23:14 GMT  
		Size: 389.2 MB (389167657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0251c0d5ac74355584e06c50a863905996866df93096bffe452ae60e4c3ea412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da807a1d3e90b3030b999efcee68beda4c81a7b562047f52386752832eb73668`

```dockerfile
```

-	Layers:
	-	`sha256:70e07b450b5299169f3a4a7558e62da777523cb09c49196f2e634be6452eedd0`  
		Last Modified: Fri, 06 Mar 2026 18:23:05 GMT  
		Size: 4.6 MB (4647141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27093dc0016c5d613c0c08db78d8ce189cc3a2c58b3445e8627828cc485cbb54`  
		Last Modified: Fri, 06 Mar 2026 18:23:04 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ca4950bfa80135d8f96071d7b2e135eb6d8c41f0deb12e0f01551ef6c63fa912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.7 MB (509673751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5df699e184386f05d3210c4dda417cfa0d2bf04ffe178cb76621e98136d957`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Fri, 06 Mar 2026 18:25:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Mar 2026 18:25:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Mar 2026 18:25:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3edc16e54b70b190f460fed9a5eb31e7e4e8c6a52aa823bff6b18dd2d2183c8a NEO4J_TARBALL=neo4j-enterprise-2026.02.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 06 Mar 2026 18:25:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.2-unix.tar.gz
# Fri, 06 Mar 2026 18:25:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 06 Mar 2026 18:25:31 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.02.2-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && groupadd --gid 7474 --system neo4j     && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker trixie/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 06 Mar 2026 18:25:31 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 18:25:31 GMT
WORKDIR /var/lib/neo4j
# Fri, 06 Mar 2026 18:25:31 GMT
VOLUME [/data /logs]
# Fri, 06 Mar 2026 18:25:31 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 06 Mar 2026 18:25:31 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 06 Mar 2026 18:25:31 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2d420dc839c4ac3b7a04177dfd877d8710595c0d07988d98c8190997ba5907`  
		Last Modified: Fri, 06 Mar 2026 18:26:01 GMT  
		Size: 91.3 MB (91288304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfa6d9438d42e324b04574821d2756a097472d5d7b44a0e8f86d0101f0b20cf`  
		Last Modified: Fri, 06 Mar 2026 18:25:57 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29480f25754a7fe32e2fff777cd36b82d31f8d58058e4cfef46e152ee5f6394`  
		Last Modified: Fri, 06 Mar 2026 18:26:06 GMT  
		Size: 388.2 MB (388235297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:216e4b16d147cfb3240f6203017953ef9b05458c14509e0a0deb318037e20cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4661757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3626f756d68c2b245097dfc2f7e507c9900efe2e8beaf44907961f76fac27fb`

```dockerfile
```

-	Layers:
	-	`sha256:d8ba452ff359f6cd531c51c4a0036d9505286ffa714c438c784517725919e811`  
		Last Modified: Fri, 06 Mar 2026 18:25:58 GMT  
		Size: 4.6 MB (4641616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7a89dfc6a043307e42d1a0c2e98797c5f2f5a02d99d14035e9a64d911ca5bbd`  
		Last Modified: Fri, 06 Mar 2026 18:25:58 GMT  
		Size: 20.1 KB (20141 bytes)  
		MIME: application/vnd.in-toto+json
