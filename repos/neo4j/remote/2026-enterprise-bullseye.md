## `neo4j:2026-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:89e1550014487d7ddc0df3e258c595e4ba30529238ffb141fc916990224fb6ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2026-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8569bdb49657d4e22bf05640b14e7dd5c61ae1e36895f89890d72d4cbdfa18bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.6 MB (553557984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bb796d1aec665e35cff052c51488d967dce4deb93bc0e3fd2e4a2f21b64d11`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:24:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:24:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:24:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a2435d9ec6f9a18eb9616c1a1319caa8b7040f38b8c20c73ef3467e607d06bf NEO4J_TARBALL=neo4j-enterprise-2026.01.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Feb 2026 21:24:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
# Tue, 17 Feb 2026 21:24:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 17 Feb 2026 21:24:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Feb 2026 21:25:05 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Feb 2026 21:25:05 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:25:05 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Feb 2026 21:25:05 GMT
VOLUME [/data /logs]
# Tue, 17 Feb 2026 21:25:05 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Feb 2026 21:25:05 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 21:25:05 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f2fb46faaa0edeb1c1581d89b630ce76d3453c689c308e72afea0ad9f05dc6`  
		Last Modified: Tue, 17 Feb 2026 21:25:27 GMT  
		Size: 157.9 MB (157857046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9826a58336e407d230a1a40302c1fa7ce6cf7d9023094c741210a5cd4838c8ce`  
		Last Modified: Tue, 17 Feb 2026 21:25:30 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759a34e9fc076920fb4a4cd1c59d033aec3f5ebe3b30832bbc3f3c5e5a8fb883`  
		Last Modified: Tue, 17 Feb 2026 21:25:30 GMT  
		Size: 10.2 KB (10190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25baad4738d860431c02475330f5d28db2ac1ee100d68568642dd3995b0827eb`  
		Last Modified: Tue, 17 Feb 2026 21:25:38 GMT  
		Size: 365.4 MB (365428589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ee92eecf0759830012aab8d27df1d35f5b195bf21985361abd2820ec4104be6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4875924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d6f4b504bcb2ffdf9e98add232f56dbe85bff897781a40cd1327c0ac2f63f3`

```dockerfile
```

-	Layers:
	-	`sha256:2f4da0916fdfdb7acbb19845dadd6269ba561154b319c69fbccac10d47d262eb`  
		Last Modified: Tue, 17 Feb 2026 21:25:30 GMT  
		Size: 4.9 MB (4855525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b4d5b8442fce936f144c1a43a55a7d8626bf7b85e6d05886515581da21b36de`  
		Last Modified: Tue, 17 Feb 2026 21:25:30 GMT  
		Size: 20.4 KB (20399 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2026-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:bae9f935fba490ce1679510fe55e76e004c58942408485fbe51d852a8b16e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.6 MB (549580683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f13254717c032793f722c09a5dae96cc6dd28a3cd3562cb7e7015ebb708ff91`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:01:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:01:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:01:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3a2435d9ec6f9a18eb9616c1a1319caa8b7040f38b8c20c73ef3467e607d06bf NEO4J_TARBALL=neo4j-enterprise-2026.01.4-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 24 Feb 2026 19:01:45 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
# Tue, 24 Feb 2026 19:01:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 24 Feb 2026 19:01:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 24 Feb 2026 19:02:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2026.01.4-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 24 Feb 2026 19:02:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:02:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 24 Feb 2026 19:02:18 GMT
VOLUME [/data /logs]
# Tue, 24 Feb 2026 19:02:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 24 Feb 2026 19:02:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:02:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de508996391266b691f0955ac40a98541131133cf9bce33befce9ac2372085b8`  
		Last Modified: Tue, 24 Feb 2026 19:02:49 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd77958d98a7b2d503c5cf213943b2c8bf9430fcb21bf158084a9e87fb8120a3`  
		Last Modified: Tue, 24 Feb 2026 19:02:44 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21a2164619b99d89605cd7c02fb42a88de4a936215df9225f6b9b2013328611`  
		Last Modified: Tue, 24 Feb 2026 19:02:44 GMT  
		Size: 10.2 KB (10191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239ba122217995f73a36731767ff2d2c7ddb8b3e3b00cb6928eb3e9c960bc21f`  
		Last Modified: Tue, 24 Feb 2026 19:02:54 GMT  
		Size: 364.7 MB (364689024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2026-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ec168ca75e4170997d882865711918e658658f4d98e6f07236afcefa28305a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4859894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a41324467753933176b8fba77802ff0fef452128627b1d6b9638f2893304a2`

```dockerfile
```

-	Layers:
	-	`sha256:cac7b317e5f34417def42326625f85b7cb87858bb3c2e00f083441bb974a1c7b`  
		Last Modified: Tue, 24 Feb 2026 19:02:44 GMT  
		Size: 4.8 MB (4839350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa8c06352d4f2e0199d088025ec5ec18d7540e456bb9d04bd1fb321aeb4e36f`  
		Last Modified: Tue, 24 Feb 2026 19:02:44 GMT  
		Size: 20.5 KB (20544 bytes)  
		MIME: application/vnd.in-toto+json
