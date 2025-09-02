## `neo4j:latest`

```console
$ docker pull neo4j@sha256:64b59f71e14268f576715e5f62efe3266914e52bdc903f87988cc9710ab114c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:b2aea2f6e0533560bddc0d93efd6d20ba86959f1aa55ea9e72da7bf5dba833c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 MB (391693187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccfd1cdeb92432aced5e935a5178da03e53293676ba1dcc28012cf6e685217a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Wed, 27 Aug 2025 14:31:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Aug 2025 14:31:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cce5d0d88c05635692a8db86cde299861ff8fd71271e034fc633080bb09d9c59 NEO4J_TARBALL=neo4j-community-2025.08.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356d4fe5aab9b9d835174f32c4f64c7ec314c13977195a6f6f3934623ace26c1`  
		Last Modified: Tue, 02 Sep 2025 02:43:30 GMT  
		Size: 157.8 MB (157804794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6776aa2bd4bdb271fb828ca8a82ead04fed13bf9dfae151a279138c3e3d2e0`  
		Last Modified: Tue, 02 Sep 2025 00:51:53 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6906bbee1f3ab13267ceee7bcb51f4ed9ca73bb7e9c517e1cbfc3582edec5211`  
		Last Modified: Tue, 02 Sep 2025 00:51:59 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993f00c15a66dbc20206a9f3b17d39ebb788c0fa8df84af6f6e02b446a3f66f0`  
		Last Modified: Tue, 02 Sep 2025 02:43:40 GMT  
		Size: 203.6 MB (203618386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:43e4f7508d2cf2602d9911e26bb060b69c7267a7195031e554d45cce07a64d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4624930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348c0237ac9415540dad97dfbbb52f8ffc70503728a4081b952970d80819456e`

```dockerfile
```

-	Layers:
	-	`sha256:53870e49104932f5ba6eecbb030c112ff0d4d0b8af79536ebd86a396fa87918d`  
		Last Modified: Tue, 02 Sep 2025 02:43:17 GMT  
		Size: 4.6 MB (4600822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5daeb97cfd20b7131bc8d5a44f24bbfe9c0c37ae540a364323e8a9f0921f9419`  
		Last Modified: Tue, 02 Sep 2025 02:43:18 GMT  
		Size: 24.1 KB (24108 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:71a3b3296f019e92698ab9d65349dac10e8c0dbcfecf665357f5cc12f7fff305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387708013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb7c789da0455ada0d191cb1b315511bd820ad062da37c215a97508308a900a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Wed, 27 Aug 2025 14:31:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 Aug 2025 14:31:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cce5d0d88c05635692a8db86cde299861ff8fd71271e034fc633080bb09d9c59 NEO4J_TARBALL=neo4j-community-2025.08.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 27 Aug 2025 14:31:02 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-2025.08.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 27 Aug 2025 14:31:02 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Aug 2025 14:31:02 GMT
WORKDIR /var/lib/neo4j
# Wed, 27 Aug 2025 14:31:02 GMT
VOLUME [/data /logs]
# Wed, 27 Aug 2025 14:31:02 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 27 Aug 2025 14:31:02 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 27 Aug 2025 14:31:02 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a88517b6197f7a20d6e986cf50966f045ceffa14e5503380ee7bc964424c74`  
		Last Modified: Tue, 02 Sep 2025 05:13:22 GMT  
		Size: 156.1 MB (156081197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069f6aec2e1e9b70a2d44070a115505387bb228649665b5ebb5ecbb8e7916982`  
		Last Modified: Tue, 02 Sep 2025 05:00:47 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca2488a5fd8c44fe4f5ccbfc6db886d7aa28d02b7ee253a489e33672d083e41`  
		Last Modified: Tue, 02 Sep 2025 05:00:47 GMT  
		Size: 10.0 KB (10019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4887d31b1c2d233ecd808c162693c886c2b1e5e3a8629747d16685cec61807`  
		Last Modified: Tue, 02 Sep 2025 05:13:46 GMT  
		Size: 202.9 MB (202862405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:69a34a3a84bd115e6a0ce15351a398f018afc2c0f4fcec5c05d44d6aa10923d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4599145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453356d17821b085f86695f326230e3106d97d4163c906874a4a390fd627e5ac`

```dockerfile
```

-	Layers:
	-	`sha256:d3b87501a736a6e8e55fe3345c748148f4cce88b78d033881cfd0d9c98b9254c`  
		Last Modified: Tue, 02 Sep 2025 05:43:21 GMT  
		Size: 4.6 MB (4574747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da1cd21cc1bc4506f1b64c401b73d8b07393c2e4002861658ce5f7e28fe050fb`  
		Last Modified: Tue, 02 Sep 2025 05:43:22 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json
