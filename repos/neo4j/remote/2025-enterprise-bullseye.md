## `neo4j:2025-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:319c2437828aaa806fb4ca13c39fc35a8b164e0b89f2a0ccee12b1d207d3f150
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:2025-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:34a8351ea27ee3168904db496f16a9a4c9dafb10e9f839ec3261afd83cb901c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.9 MB (528916042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799b1e3b003c43c661962491a945a4ad758a0ae2ee0dfd2dd05ab354e0b5de42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Tue, 01 Jul 2025 15:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Jul 2025 15:46:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0dfbe622a001005873bf90fd06b7fedcf4415f6dc9ec31cb35d223304f614f22 NEO4J_TARBALL=neo4j-enterprise-2025.06.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 01 Jul 2025 15:46:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.06.0-unix.tar.gz
# Tue, 01 Jul 2025 15:46:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.06.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.06.0-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 01 Jul 2025 15:46:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jul 2025 15:46:08 GMT
WORKDIR /var/lib/neo4j
# Tue, 01 Jul 2025 15:46:08 GMT
VOLUME [/data /logs]
# Tue, 01 Jul 2025 15:46:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 01 Jul 2025 15:46:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 01 Jul 2025 15:46:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5288f00f230c4b7650b835b832308bda8151b2ed0da3427bad12b86c20bab9`  
		Last Modified: Wed, 02 Jul 2025 08:46:15 GMT  
		Size: 157.6 MB (157634482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7252c1b92c3fe2531eabf4d21aae93efa7160d3668a498bc4ba8a478d8510779`  
		Last Modified: Wed, 02 Jul 2025 05:45:16 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ee84cac81746adb1fce1404f05574254c3e8fa448ab4b4cb3df6996c1deace`  
		Last Modified: Wed, 02 Jul 2025 05:45:19 GMT  
		Size: 10.0 KB (9976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525cd630cc621d9982e1031037f1efb70b5132953de48b2cf92952f3f588900c`  
		Last Modified: Wed, 02 Jul 2025 06:17:27 GMT  
		Size: 341.0 MB (341011665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:941e6545e3ae70c3f44c4cd326295f35c77bb8db5611d8efdf8117b80582bec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4859970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c28df5b05beb2e7c4a9aea09ce4f5ea1b8c92b74ddce69ce8a132c951739308`

```dockerfile
```

-	Layers:
	-	`sha256:7a88862323b347c1fec09edb5c4e9f41d84755ab51070f5cb349c9f1771f750d`  
		Last Modified: Wed, 02 Jul 2025 05:43:41 GMT  
		Size: 4.8 MB (4838269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:185abe8c5e95349100f616e9c0bc908b7e5bcc02708c71f9b7441820c94cc1b1`  
		Last Modified: Wed, 02 Jul 2025 05:43:41 GMT  
		Size: 21.7 KB (21701 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:2025-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7290df69e692803b5b10b6a9638adef4d3ccaa579ea121636cd08c9e1cf48c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.0 MB (525025678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b95feb62b9dcecb9afb5eb55aee165a555a566d5abb486cd9600c0b3dcde89`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 19 Jun 2025 13:23:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Thu, 19 Jun 2025 13:23:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Jun 2025 13:23:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=836097f43a9d33f986620f5ff6d7862f83623f6a74d7d828dbe2d694c39f98cd NEO4J_TARBALL=neo4j-enterprise-2025.05.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 19 Jun 2025 13:23:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-2025.05.1-unix.tar.gz
RUN apt-get update     && apt-get install --no-install-recommends -o Acquire::Retries=10 -y       curl ca-certificates gcc libc-dev git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make libc-dev     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 19 Jun 2025 13:23:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Jun 2025 13:23:43 GMT
WORKDIR /var/lib/neo4j
# Thu, 19 Jun 2025 13:23:43 GMT
VOLUME [/data /logs]
# Thu, 19 Jun 2025 13:23:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 19 Jun 2025 13:23:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 19 Jun 2025 13:23:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f209ff44f683a19134a65d227eda78e676586776061dfd6857f025b7df4f82e`  
		Last Modified: Tue, 01 Jul 2025 08:48:37 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6d7365b6eb3b464d495a247c76708922b0d4d89a972f2a9834fe3ec3f491f2`  
		Last Modified: Tue, 01 Jul 2025 07:18:58 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee0a64b3673c90279322a4b8bf6f53a01f266a7425c60f4cc620f6d16874fc5`  
		Last Modified: Tue, 01 Jul 2025 07:18:58 GMT  
		Size: 10.0 KB (9979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598de060f404a5f7c11f194aa27799802c568dc79cd8548d74612d00d6754e8`  
		Last Modified: Tue, 01 Jul 2025 08:58:50 GMT  
		Size: 340.3 MB (340338834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:2025-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8f54c34016f6b45594261243f352620ed80273b43a448b1c27a255a45411616e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4835224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce619ecb896e0463df7d99e90f51cf41013a0fffe963d6f451b782a8d78b145`

```dockerfile
```

-	Layers:
	-	`sha256:b54703476c8a93773a4d20aead73005afe2dfa129681369cd5e59b14a8595d8e`  
		Last Modified: Tue, 01 Jul 2025 08:43:31 GMT  
		Size: 4.8 MB (4813330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d41af2af18d75054bd21fea8866e49eeb610fb282a6b212de904f75eb8b9030b`  
		Last Modified: Tue, 01 Jul 2025 08:43:31 GMT  
		Size: 21.9 KB (21894 bytes)  
		MIME: application/vnd.in-toto+json
