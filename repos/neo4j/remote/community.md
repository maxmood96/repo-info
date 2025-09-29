## `neo4j:community`

```console
$ docker pull neo4j@sha256:66449b615931c0ab9a97711f3126e04d1079178093c6e73ab80cf6e777cbcc38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:5499835cc77a3f32f494f233ab2003d3c8de52c070cb2369ebc49ef8c5c69815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399316729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8152863011e344900af78c39ddd67f2204ad1da81a191cfd4f208d8b50d1ad74`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Wed, 24 Sep 2025 16:30:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Sep 2025 16:30:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=38e6828ba11a700c94e4a532a10e3481e94cfabc45f9b4819cafc4bdc105cba5 NEO4J_TARBALL=neo4j-community-2025.09.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Sep 2025 16:30:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 16:30:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Sep 2025 16:30:37 GMT
VOLUME [/data /logs]
# Wed, 24 Sep 2025 16:30:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Sep 2025 16:30:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 16:30:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d2eeb94c0199831fd2e5a03f54f7b106f4e58838115d73a2f5538a0522b394`  
		Last Modified: Mon, 29 Sep 2025 17:45:09 GMT  
		Size: 157.8 MB (157804727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe364a9b94cfd1d254e33bd7e2481085035304e720159576b968fd244d302d9`  
		Last Modified: Mon, 29 Sep 2025 17:37:06 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a4c13fe607ed3e99eab83da867686fe571a3704888e09a11a7f75ed02309c2`  
		Last Modified: Mon, 29 Sep 2025 17:37:06 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139fb017c4ebd675dac24c461acfb682a1dc14eba857aec89aac329df68bf21d`  
		Last Modified: Mon, 29 Sep 2025 17:36:40 GMT  
		Size: 211.2 MB (211242042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:34e81ded767d318cac335f3c2495d82cf30671746a6d3e2dd5f02d7285ef4bec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4627779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb3465f2d2ec9079eaf4b7944a5a958387ef9bb56a4c0c6b0588b2b1ee11f4f`

```dockerfile
```

-	Layers:
	-	`sha256:b2607a37983cfb0167234eb8d2f55d706856dbf2bcc2be7c72472fb76f0ee1a0`  
		Last Modified: Mon, 29 Sep 2025 17:43:27 GMT  
		Size: 4.6 MB (4603670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ab34a87957d47e598821d08a3a6bb85494d7e80761ad26d20b5fd8c9d4a1c7`  
		Last Modified: Mon, 29 Sep 2025 17:43:27 GMT  
		Size: 24.1 KB (24109 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:25940f94e515b886e7bd1061ab58dc5ee57ea22c08d2109d189dc467f41d7274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.3 MB (395330888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe39f26b4b6ec6d4eb78d44c123d42bd72ab53aff3c8bea64d1e213d268192c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Wed, 24 Sep 2025 16:30:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Sep 2025 16:30:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=38e6828ba11a700c94e4a532a10e3481e94cfabc45f9b4819cafc4bdc105cba5 NEO4J_TARBALL=neo4j-community-2025.09.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 24 Sep 2025 16:30:37 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.09.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 24 Sep 2025 16:30:37 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Sep 2025 16:30:37 GMT
WORKDIR /var/lib/neo4j
# Wed, 24 Sep 2025 16:30:37 GMT
VOLUME [/data /logs]
# Wed, 24 Sep 2025 16:30:37 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 24 Sep 2025 16:30:37 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 24 Sep 2025 16:30:37 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19043a45eda24b6e24e47d0a4a72aecced0238008e5c46ea8e716e0978489da`  
		Last Modified: Mon, 29 Sep 2025 17:45:37 GMT  
		Size: 156.1 MB (156081218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2ad18950644e2138f368e1f9469035e291f7b4f01cd3fff4a352bb872585f7`  
		Last Modified: Mon, 29 Sep 2025 17:38:15 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bf4f8cdeb53e4474127bc5a009bccf66decb7f1a63d08b43b36018c32134f4`  
		Last Modified: Mon, 29 Sep 2025 17:38:15 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3852661c47c3b0684231d9ff871452c1ab438ffae00ed8ab8b21a1bbe15db316`  
		Last Modified: Mon, 29 Sep 2025 17:37:52 GMT  
		Size: 210.5 MB (210485295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:28a5f2873ad59be481965a8c126dbe33920d29ca01bcbfb042b1a3bec0cf0e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4601992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c88eca307b24918db6794f553b2285dea48311d5012e59cce0f08ef7cf28a9`

```dockerfile
```

-	Layers:
	-	`sha256:07806e02bf0874e6200b608381c769e51ca4a7acfa9598d84dc3c754a1849838`  
		Last Modified: Mon, 29 Sep 2025 17:43:32 GMT  
		Size: 4.6 MB (4577595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3614f2a7fa84293e9d1bdfd9a55dbc7b01a445229648dd1247f9142a022fbc12`  
		Last Modified: Mon, 29 Sep 2025 17:43:33 GMT  
		Size: 24.4 KB (24397 bytes)  
		MIME: application/vnd.in-toto+json
