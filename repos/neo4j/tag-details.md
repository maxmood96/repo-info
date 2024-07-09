<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.35`](#neo4j4435)
-	[`neo4j:4.4.35-community`](#neo4j4435-community)
-	[`neo4j:4.4.35-enterprise`](#neo4j4435-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi9`](#neo4j5-community-ubi9)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi9`](#neo4j5-enterprise-ubi9)
-	[`neo4j:5-ubi9`](#neo4j5-ubi9)
-	[`neo4j:5.21`](#neo4j521)
-	[`neo4j:5.21-bullseye`](#neo4j521-bullseye)
-	[`neo4j:5.21-community`](#neo4j521-community)
-	[`neo4j:5.21-community-bullseye`](#neo4j521-community-bullseye)
-	[`neo4j:5.21-community-ubi9`](#neo4j521-community-ubi9)
-	[`neo4j:5.21-enterprise`](#neo4j521-enterprise)
-	[`neo4j:5.21-enterprise-bullseye`](#neo4j521-enterprise-bullseye)
-	[`neo4j:5.21-enterprise-ubi9`](#neo4j521-enterprise-ubi9)
-	[`neo4j:5.21-ubi9`](#neo4j521-ubi9)
-	[`neo4j:5.21.2`](#neo4j5212)
-	[`neo4j:5.21.2-bullseye`](#neo4j5212-bullseye)
-	[`neo4j:5.21.2-community`](#neo4j5212-community)
-	[`neo4j:5.21.2-community-bullseye`](#neo4j5212-community-bullseye)
-	[`neo4j:5.21.2-community-ubi9`](#neo4j5212-community-ubi9)
-	[`neo4j:5.21.2-enterprise`](#neo4j5212-enterprise)
-	[`neo4j:5.21.2-enterprise-bullseye`](#neo4j5212-enterprise-bullseye)
-	[`neo4j:5.21.2-enterprise-ubi9`](#neo4j5212-enterprise-ubi9)
-	[`neo4j:5.21.2-ubi9`](#neo4j5212-ubi9)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi9`](#neo4jcommunity-ubi9)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi9`](#neo4jenterprise-ubi9)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi9`](#neo4jubi9)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:548050168bc1c408bd6e5c6250ca2e1776db50555ab4a5f756ff0d94c98e1a8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:eb0b59d533f5c2c0faea4a98c74ddd6ee83f959f6fc8ab58023a2c883a657f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302610541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8d892cffe97d2c97903c6798120641c1bf166f101596f8c152d013dc4d9715`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a31d88a599c7581da325b7768830898dcc2c454af4a8ebb52d52b170a366ada3 NEO4J_TARBALL=neo4j-community-4.4.35-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b56c05cd79b071b1e40539cedd0baf182c14d6c16a247169a002417b5f4561`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 145.5 MB (145504813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c359f4e30f16df7457aa0997b77660d1ee0dc632e4796e674483db8fd258797`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f61beef8f5d224007037dbd7ca8aab66208a525e9a8f40f12bc5e8d4ce2c3b`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739f5e0a9cb12578c2568586af418870f949e842781897b46a6a99d329b50027`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 125.7 MB (125670053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:6cc65f0ace94beeb96c14a3f5921566b2709bf781c2234651ffe1130645bc5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86067969c5c8cf215bfe25d00607b3e242f2e0ee27282acd0c11394860a6b81b`

```dockerfile
```

-	Layers:
	-	`sha256:4c95ad4a9c692762169fabdb7e804ef305c05c82c6595124b49337f9eb20e6e4`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 2.9 MB (2940156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410257678d97922ca12533a81a7e653163352bb7bad268c74fbbd7640e763c0a`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 19.5 KB (19536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2aec184877b1df04f1a50ab6dd1015ba0c39867d8459cb568538e6fb4ea70998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298027554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c64298d88fb4822eeccef06c2760cb3f1d7287baef6dab40b254c7a70f8fb47`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a31d88a599c7581da325b7768830898dcc2c454af4a8ebb52d52b170a366ada3 NEO4J_TARBALL=neo4j-community-4.4.35-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127528c2a0803689f9e03ed144eb7051ec9b9953d24de2a7af6ce6248cafcdf`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 142.3 MB (142304056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c96cc03b5f5919fe4467177d168fd852c1b82da7ec70ab639a149b717b97d2`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2e5898f12c60503bf06d979edccadbe44b2e42a57c71fc47efe0ef67c7a17e`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cefe94d2cbc1c85f2fe1e11fbf9872c0e19db7a69db7a63686ba7fa3f4ab809`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 125.6 MB (125640460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:12a145ef60203d0e36c394778492d3bbc48508c821ef6f4d614d0015f16c37ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac74334ba12bc95262c523e40b796fe3e6c8b8c668e1e5511773efca455fb0c`

```dockerfile
```

-	Layers:
	-	`sha256:fd55ae996591627e85c914d35cb9c17faa505088172fa6bffa55bf4fdd3d6c1f`  
		Last Modified: Fri, 05 Jul 2024 01:55:39 GMT  
		Size: 2.9 MB (2940419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5b3dda8426e01553e693c09e081aec55fe38668327b8111049db0fc6f5c7640`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 20.1 KB (20089 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:548050168bc1c408bd6e5c6250ca2e1776db50555ab4a5f756ff0d94c98e1a8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:eb0b59d533f5c2c0faea4a98c74ddd6ee83f959f6fc8ab58023a2c883a657f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302610541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8d892cffe97d2c97903c6798120641c1bf166f101596f8c152d013dc4d9715`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a31d88a599c7581da325b7768830898dcc2c454af4a8ebb52d52b170a366ada3 NEO4J_TARBALL=neo4j-community-4.4.35-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b56c05cd79b071b1e40539cedd0baf182c14d6c16a247169a002417b5f4561`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 145.5 MB (145504813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c359f4e30f16df7457aa0997b77660d1ee0dc632e4796e674483db8fd258797`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f61beef8f5d224007037dbd7ca8aab66208a525e9a8f40f12bc5e8d4ce2c3b`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739f5e0a9cb12578c2568586af418870f949e842781897b46a6a99d329b50027`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 125.7 MB (125670053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:6cc65f0ace94beeb96c14a3f5921566b2709bf781c2234651ffe1130645bc5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86067969c5c8cf215bfe25d00607b3e242f2e0ee27282acd0c11394860a6b81b`

```dockerfile
```

-	Layers:
	-	`sha256:4c95ad4a9c692762169fabdb7e804ef305c05c82c6595124b49337f9eb20e6e4`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 2.9 MB (2940156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410257678d97922ca12533a81a7e653163352bb7bad268c74fbbd7640e763c0a`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 19.5 KB (19536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2aec184877b1df04f1a50ab6dd1015ba0c39867d8459cb568538e6fb4ea70998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298027554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c64298d88fb4822eeccef06c2760cb3f1d7287baef6dab40b254c7a70f8fb47`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a31d88a599c7581da325b7768830898dcc2c454af4a8ebb52d52b170a366ada3 NEO4J_TARBALL=neo4j-community-4.4.35-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127528c2a0803689f9e03ed144eb7051ec9b9953d24de2a7af6ce6248cafcdf`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 142.3 MB (142304056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c96cc03b5f5919fe4467177d168fd852c1b82da7ec70ab639a149b717b97d2`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2e5898f12c60503bf06d979edccadbe44b2e42a57c71fc47efe0ef67c7a17e`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cefe94d2cbc1c85f2fe1e11fbf9872c0e19db7a69db7a63686ba7fa3f4ab809`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 125.6 MB (125640460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:12a145ef60203d0e36c394778492d3bbc48508c821ef6f4d614d0015f16c37ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac74334ba12bc95262c523e40b796fe3e6c8b8c668e1e5511773efca455fb0c`

```dockerfile
```

-	Layers:
	-	`sha256:fd55ae996591627e85c914d35cb9c17faa505088172fa6bffa55bf4fdd3d6c1f`  
		Last Modified: Fri, 05 Jul 2024 01:55:39 GMT  
		Size: 2.9 MB (2940419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5b3dda8426e01553e693c09e081aec55fe38668327b8111049db0fc6f5c7640`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 20.1 KB (20089 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:53b370df2871ae5e3e37023cc036259c0ae167ab04368d8b7bcd2b0737e3b5d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5fd89c66a7d60cc171428bab349b7715e0885ac6ef2ffb8a365cc9ad90a40038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.5 MB (403476646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b11983d66b0725916c7fbe8072a640693c7c880b81dea70003f2629454caeb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b24c5cd6b1651b037d382e3d0d906410d63b857ed99dcb288a77f574f333fd52 NEO4J_TARBALL=neo4j-enterprise-4.4.35-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b017e1652706f82af0761c2d18f197ccd27c7836beebd4ac5c101f7f4a4b35b`  
		Last Modified: Fri, 05 Jul 2024 01:55:48 GMT  
		Size: 145.5 MB (145504812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c28e000d6d7dd42939442f8c226d1dcf740ad8d82c694967f0c76ce48379b99`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc42e13d58b8e48fe99c45e1e80e5c185e82e0611a7738a24cec7debfe91add`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7393aa3d303382d98da893e907d9b75a3ea71353ab1d78b7029cec00bbf32425`  
		Last Modified: Fri, 05 Jul 2024 01:55:49 GMT  
		Size: 226.5 MB (226536157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:35664bbe2fbe8b27d63ac0a59b4840d374d6bf31da220f355b0fe439306e16e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3080483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170f600a243535850acbcbe8bcb7c7b79dad949f7b5c64ec286c2a234715fdd4`

```dockerfile
```

-	Layers:
	-	`sha256:359248ad44e09bec3cf0eb890a4cef084611417da49e6f4dc17f9ec9aaf2dbe0`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 3.1 MB (3061516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4858106aaea807418876e3a0f4281af9c4cc3a2c661ee60936cf7ba71a924c3`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 19.0 KB (18967 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:af13fc94f509df052126ec13f21e31a506087389b511d2d9fcd9b261017e9c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.9 MB (398888058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe6bc7669f7093aa766ceb5e7890519b86207604abb28c60476c65b882db558`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b24c5cd6b1651b037d382e3d0d906410d63b857ed99dcb288a77f574f333fd52 NEO4J_TARBALL=neo4j-enterprise-4.4.35-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127528c2a0803689f9e03ed144eb7051ec9b9953d24de2a7af6ce6248cafcdf`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 142.3 MB (142304056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9c518c665bfb7ebad8361f04f5ae0db4f9b384565ec8075cdd893eacc942b4`  
		Last Modified: Fri, 05 Jul 2024 01:56:44 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7a1a317043650a984e1ffe19b213cdf74cb3705c2e92fa0d5f3bb79cdd47ce`  
		Last Modified: Fri, 05 Jul 2024 01:56:44 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701ff67564a6752d6c1a06d69da92fa5517424bfe1e6dae6938b0b244ce68c9f`  
		Last Modified: Fri, 05 Jul 2024 01:56:49 GMT  
		Size: 226.5 MB (226500966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c4307870c0c63ece1f9f2b60608f9d82b84a17aa6456d6558d327195d4e29923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3081251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f208c0fc2d7a6fd0c0e9b41394b14c9b45c97502e36b6d68e7b149f30fc21cb7`

```dockerfile
```

-	Layers:
	-	`sha256:34994f5eab05f619341264864e6f2cf986e028a860c5dbd7d48dcda2e7860c0d`  
		Last Modified: Fri, 05 Jul 2024 01:56:45 GMT  
		Size: 3.1 MB (3061755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e31aeb8b8b33ee2764dc242a2468143d9bbf48c77487ccf6bf3b24fe678fb065`  
		Last Modified: Fri, 05 Jul 2024 01:56:44 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.35`

```console
$ docker pull neo4j@sha256:548050168bc1c408bd6e5c6250ca2e1776db50555ab4a5f756ff0d94c98e1a8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.35` - linux; amd64

```console
$ docker pull neo4j@sha256:eb0b59d533f5c2c0faea4a98c74ddd6ee83f959f6fc8ab58023a2c883a657f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302610541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8d892cffe97d2c97903c6798120641c1bf166f101596f8c152d013dc4d9715`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a31d88a599c7581da325b7768830898dcc2c454af4a8ebb52d52b170a366ada3 NEO4J_TARBALL=neo4j-community-4.4.35-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b56c05cd79b071b1e40539cedd0baf182c14d6c16a247169a002417b5f4561`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 145.5 MB (145504813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c359f4e30f16df7457aa0997b77660d1ee0dc632e4796e674483db8fd258797`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f61beef8f5d224007037dbd7ca8aab66208a525e9a8f40f12bc5e8d4ce2c3b`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739f5e0a9cb12578c2568586af418870f949e842781897b46a6a99d329b50027`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 125.7 MB (125670053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.35` - unknown; unknown

```console
$ docker pull neo4j@sha256:6cc65f0ace94beeb96c14a3f5921566b2709bf781c2234651ffe1130645bc5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86067969c5c8cf215bfe25d00607b3e242f2e0ee27282acd0c11394860a6b81b`

```dockerfile
```

-	Layers:
	-	`sha256:4c95ad4a9c692762169fabdb7e804ef305c05c82c6595124b49337f9eb20e6e4`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 2.9 MB (2940156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410257678d97922ca12533a81a7e653163352bb7bad268c74fbbd7640e763c0a`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 19.5 KB (19536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.35` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2aec184877b1df04f1a50ab6dd1015ba0c39867d8459cb568538e6fb4ea70998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298027554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c64298d88fb4822eeccef06c2760cb3f1d7287baef6dab40b254c7a70f8fb47`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a31d88a599c7581da325b7768830898dcc2c454af4a8ebb52d52b170a366ada3 NEO4J_TARBALL=neo4j-community-4.4.35-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127528c2a0803689f9e03ed144eb7051ec9b9953d24de2a7af6ce6248cafcdf`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 142.3 MB (142304056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c96cc03b5f5919fe4467177d168fd852c1b82da7ec70ab639a149b717b97d2`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2e5898f12c60503bf06d979edccadbe44b2e42a57c71fc47efe0ef67c7a17e`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cefe94d2cbc1c85f2fe1e11fbf9872c0e19db7a69db7a63686ba7fa3f4ab809`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 125.6 MB (125640460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.35` - unknown; unknown

```console
$ docker pull neo4j@sha256:12a145ef60203d0e36c394778492d3bbc48508c821ef6f4d614d0015f16c37ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac74334ba12bc95262c523e40b796fe3e6c8b8c668e1e5511773efca455fb0c`

```dockerfile
```

-	Layers:
	-	`sha256:fd55ae996591627e85c914d35cb9c17faa505088172fa6bffa55bf4fdd3d6c1f`  
		Last Modified: Fri, 05 Jul 2024 01:55:39 GMT  
		Size: 2.9 MB (2940419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5b3dda8426e01553e693c09e081aec55fe38668327b8111049db0fc6f5c7640`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 20.1 KB (20089 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.35-community`

```console
$ docker pull neo4j@sha256:548050168bc1c408bd6e5c6250ca2e1776db50555ab4a5f756ff0d94c98e1a8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.35-community` - linux; amd64

```console
$ docker pull neo4j@sha256:eb0b59d533f5c2c0faea4a98c74ddd6ee83f959f6fc8ab58023a2c883a657f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302610541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8d892cffe97d2c97903c6798120641c1bf166f101596f8c152d013dc4d9715`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a31d88a599c7581da325b7768830898dcc2c454af4a8ebb52d52b170a366ada3 NEO4J_TARBALL=neo4j-community-4.4.35-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b56c05cd79b071b1e40539cedd0baf182c14d6c16a247169a002417b5f4561`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 145.5 MB (145504813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c359f4e30f16df7457aa0997b77660d1ee0dc632e4796e674483db8fd258797`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f61beef8f5d224007037dbd7ca8aab66208a525e9a8f40f12bc5e8d4ce2c3b`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739f5e0a9cb12578c2568586af418870f949e842781897b46a6a99d329b50027`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 125.7 MB (125670053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.35-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:6cc65f0ace94beeb96c14a3f5921566b2709bf781c2234651ffe1130645bc5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86067969c5c8cf215bfe25d00607b3e242f2e0ee27282acd0c11394860a6b81b`

```dockerfile
```

-	Layers:
	-	`sha256:4c95ad4a9c692762169fabdb7e804ef305c05c82c6595124b49337f9eb20e6e4`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 2.9 MB (2940156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410257678d97922ca12533a81a7e653163352bb7bad268c74fbbd7640e763c0a`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 19.5 KB (19536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.35-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2aec184877b1df04f1a50ab6dd1015ba0c39867d8459cb568538e6fb4ea70998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298027554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c64298d88fb4822eeccef06c2760cb3f1d7287baef6dab40b254c7a70f8fb47`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a31d88a599c7581da325b7768830898dcc2c454af4a8ebb52d52b170a366ada3 NEO4J_TARBALL=neo4j-community-4.4.35-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127528c2a0803689f9e03ed144eb7051ec9b9953d24de2a7af6ce6248cafcdf`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 142.3 MB (142304056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c96cc03b5f5919fe4467177d168fd852c1b82da7ec70ab639a149b717b97d2`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2e5898f12c60503bf06d979edccadbe44b2e42a57c71fc47efe0ef67c7a17e`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cefe94d2cbc1c85f2fe1e11fbf9872c0e19db7a69db7a63686ba7fa3f4ab809`  
		Last Modified: Fri, 05 Jul 2024 01:55:41 GMT  
		Size: 125.6 MB (125640460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.35-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:12a145ef60203d0e36c394778492d3bbc48508c821ef6f4d614d0015f16c37ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac74334ba12bc95262c523e40b796fe3e6c8b8c668e1e5511773efca455fb0c`

```dockerfile
```

-	Layers:
	-	`sha256:fd55ae996591627e85c914d35cb9c17faa505088172fa6bffa55bf4fdd3d6c1f`  
		Last Modified: Fri, 05 Jul 2024 01:55:39 GMT  
		Size: 2.9 MB (2940419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5b3dda8426e01553e693c09e081aec55fe38668327b8111049db0fc6f5c7640`  
		Last Modified: Fri, 05 Jul 2024 01:55:38 GMT  
		Size: 20.1 KB (20089 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.35-enterprise`

```console
$ docker pull neo4j@sha256:53b370df2871ae5e3e37023cc036259c0ae167ab04368d8b7bcd2b0737e3b5d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.35-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5fd89c66a7d60cc171428bab349b7715e0885ac6ef2ffb8a365cc9ad90a40038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.5 MB (403476646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b11983d66b0725916c7fbe8072a640693c7c880b81dea70003f2629454caeb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b24c5cd6b1651b037d382e3d0d906410d63b857ed99dcb288a77f574f333fd52 NEO4J_TARBALL=neo4j-enterprise-4.4.35-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b017e1652706f82af0761c2d18f197ccd27c7836beebd4ac5c101f7f4a4b35b`  
		Last Modified: Fri, 05 Jul 2024 01:55:48 GMT  
		Size: 145.5 MB (145504812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c28e000d6d7dd42939442f8c226d1dcf740ad8d82c694967f0c76ce48379b99`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc42e13d58b8e48fe99c45e1e80e5c185e82e0611a7738a24cec7debfe91add`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7393aa3d303382d98da893e907d9b75a3ea71353ab1d78b7029cec00bbf32425`  
		Last Modified: Fri, 05 Jul 2024 01:55:49 GMT  
		Size: 226.5 MB (226536157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.35-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:35664bbe2fbe8b27d63ac0a59b4840d374d6bf31da220f355b0fe439306e16e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3080483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170f600a243535850acbcbe8bcb7c7b79dad949f7b5c64ec286c2a234715fdd4`

```dockerfile
```

-	Layers:
	-	`sha256:359248ad44e09bec3cf0eb890a4cef084611417da49e6f4dc17f9ec9aaf2dbe0`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 3.1 MB (3061516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4858106aaea807418876e3a0f4281af9c4cc3a2c661ee60936cf7ba71a924c3`  
		Last Modified: Fri, 05 Jul 2024 01:55:45 GMT  
		Size: 19.0 KB (18967 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.35-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:af13fc94f509df052126ec13f21e31a506087389b511d2d9fcd9b261017e9c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.9 MB (398888058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe6bc7669f7093aa766ceb5e7890519b86207604abb28c60476c65b882db558`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 04 Jul 2024 09:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jul 2024 09:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=b24c5cd6b1651b037d382e3d0d906410d63b857ed99dcb288a77f574f333fd52 NEO4J_TARBALL=neo4j-enterprise-4.4.35-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.35-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 04 Jul 2024 09:48:10 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jul 2024 09:48:10 GMT
WORKDIR /var/lib/neo4j
# Thu, 04 Jul 2024 09:48:10 GMT
VOLUME [/data /logs]
# Thu, 04 Jul 2024 09:48:10 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 04 Jul 2024 09:48:10 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 04 Jul 2024 09:48:10 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127528c2a0803689f9e03ed144eb7051ec9b9953d24de2a7af6ce6248cafcdf`  
		Last Modified: Fri, 05 Jul 2024 01:55:42 GMT  
		Size: 142.3 MB (142304056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9c518c665bfb7ebad8361f04f5ae0db4f9b384565ec8075cdd893eacc942b4`  
		Last Modified: Fri, 05 Jul 2024 01:56:44 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7a1a317043650a984e1ffe19b213cdf74cb3705c2e92fa0d5f3bb79cdd47ce`  
		Last Modified: Fri, 05 Jul 2024 01:56:44 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701ff67564a6752d6c1a06d69da92fa5517424bfe1e6dae6938b0b244ce68c9f`  
		Last Modified: Fri, 05 Jul 2024 01:56:49 GMT  
		Size: 226.5 MB (226500966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.35-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c4307870c0c63ece1f9f2b60608f9d82b84a17aa6456d6558d327195d4e29923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3081251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f208c0fc2d7a6fd0c0e9b41394b14c9b45c97502e36b6d68e7b149f30fc21cb7`

```dockerfile
```

-	Layers:
	-	`sha256:34994f5eab05f619341264864e6f2cf986e028a860c5dbd7d48dcda2e7860c0d`  
		Last Modified: Fri, 05 Jul 2024 01:56:45 GMT  
		Size: 3.1 MB (3061755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e31aeb8b8b33ee2764dc242a2468143d9bbf48c77487ccf6bf3b24fe678fb065`  
		Last Modified: Fri, 05 Jul 2024 01:56:44 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:ffc7f16288174ad6674ff60309948dc2b84720e7d3f492577e681719227e3762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f03c47badc99528a7e122359f1d901cb298f962c94e56e6db0ecd31a815add8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290949534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea0753538e414dc073e3f5299b5336cb4dc62868ee152313e6153ee617ba608`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 27 Jun 2024 14:44:46 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef536f4dad38d4029007a3c0c874bd63a8447745dd74a2e803307b2a43e4bfaf`  
		Last Modified: Thu, 27 Jun 2024 18:55:42 GMT  
		Size: 125.1 MB (125114710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea596549228e026cd5a7153b75bfd794ba892d11e18e7909e8f5fc208279042`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a357a347f1c339e3aaab4b83c91c7f2b2f54d6b7051ba5fbb3e6ba2a033cccb`  
		Last Modified: Thu, 27 Jun 2024 18:55:41 GMT  
		Size: 127.0 MB (126972847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56c7125e7ffab755468030b8fe2e3a994eb4de4ca5690696e58c115e3b8b3cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba186b67cc9e1011cf084063f71011bd1c946af3c9c650f5a512384c34d8698`

```dockerfile
```

-	Layers:
	-	`sha256:59ffbc322f49d9fe5ff2fceae0e7688414767482d15dee65b205bce61e240668`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 5.1 MB (5052363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b9b9354ebc24b732ce2edbb905f417a701385261f868679792669d4504bb71`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 21.7 KB (21721 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45002a8c43bf87404457920a508b078b950fed93d33b94fe84aa9df4ca693325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289186819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818eb2f4a3569e0b9895f3e163290015df6b951a6f8fc8f7a077c74b1db4728`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bfc506818707cec2c06a141c43764cd1a6f2701bb174bfc5e02976f59c2f4`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 127.0 MB (126974246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e262333102f509b729b4b3d09000e0ba0b83a5f447ccf396ed378ad3d5e3f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f9e3f98ceb2f833aab1c40f12b68032a447c9b355c773a472598de9879b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:8495b0264746cf1d6194e85632587569f89030c84ab424d312fd2a8becc955c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 5.0 MB (5031650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019c04b56ea5810133a05a7b17486bfcdb0b2319007fe11f4524ed2ec9d2c758`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:4705e577aa259ba8ccc1fd8d656220c66534b82d4d23b0f25242ce04de339dce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d15801e2583c7ee6013df9ca4cb1a0ff7e4783fe7c407961546417c4ca39db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9870116d4be0a620eb915ac456729b0e7160370a45c7e650c8271aa1dcd5c055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe68269009ae76ebd480d4279f934c63bb9054c688088219585466bb5cc53ad`  
		Last Modified: Tue, 02 Jul 2024 07:08:53 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dbcd4df024a203f3550164811b35176f2f2f17c21d6e939760595472fdf8da`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3980dd600c2d502c04cc292cbd4ef59d30efe20b57537683a919163afd8554af`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d56046cf7f45c6eaca9e31c476e2db7365261c25a8081879631b2791a9c22ce`  
		Last Modified: Tue, 02 Jul 2024 07:08:58 GMT  
		Size: 412.8 MB (412831265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e01109e6ee3b753ca85c8c0ea230ae5808930a4b74374b127f163280352c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935c903006d0a86bcf5b9b3336e8e04c771294e64ad8893c1548cda53589dacf`

```dockerfile
```

-	Layers:
	-	`sha256:fb7c25e7c586b5a3a0787c7266877b3509a81fb467e8ee18da56c8ab617ce0c2`  
		Last Modified: Tue, 02 Jul 2024 07:08:49 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4872c58da475aeb616fa128243a6321c9c80428e0ab91eb33369b4d04aa49933`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c16f6edf08a2a6d9082a266659626a2c1a943e5ded2d202b76b00a974dc0a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586774715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43fb7aa8c8437f216e0f34b4c9c7afc9b49a883fb6e1515e5f2b432b5b88e6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e193394a16e7ce4f7319f265eb4490e90781352261c19ce610805e4db1d9e`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab12acc287d76f7ee208891bf35d50474ef788d26c99d013d705ab4e4b6e52b`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fc92950c63e0570a22a3c93548bbf86519afcb11354c0f86d73ad269d5a17`  
		Last Modified: Tue, 09 Jul 2024 19:39:38 GMT  
		Size: 412.8 MB (412798793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc6ef7512d3e9cbe1095837fd751001d3b5fe4e85e1b691a23371396cd66db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf741080bc44fe0b7220172f01f086c918fad2dc889918f935ac214a65bcd576`

```dockerfile
```

-	Layers:
	-	`sha256:40eac872f4ca581a51573364af436cbbbb85d33a3285d9eb9da982b08c61732c`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.2 MB (3188393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1734c8c05490e3e5f8cae58ce3093774c756ee923760bfe51998554ba3807`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 21.6 KB (21561 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4705e577aa259ba8ccc1fd8d656220c66534b82d4d23b0f25242ce04de339dce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d15801e2583c7ee6013df9ca4cb1a0ff7e4783fe7c407961546417c4ca39db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9870116d4be0a620eb915ac456729b0e7160370a45c7e650c8271aa1dcd5c055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe68269009ae76ebd480d4279f934c63bb9054c688088219585466bb5cc53ad`  
		Last Modified: Tue, 02 Jul 2024 07:08:53 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dbcd4df024a203f3550164811b35176f2f2f17c21d6e939760595472fdf8da`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3980dd600c2d502c04cc292cbd4ef59d30efe20b57537683a919163afd8554af`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d56046cf7f45c6eaca9e31c476e2db7365261c25a8081879631b2791a9c22ce`  
		Last Modified: Tue, 02 Jul 2024 07:08:58 GMT  
		Size: 412.8 MB (412831265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e01109e6ee3b753ca85c8c0ea230ae5808930a4b74374b127f163280352c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935c903006d0a86bcf5b9b3336e8e04c771294e64ad8893c1548cda53589dacf`

```dockerfile
```

-	Layers:
	-	`sha256:fb7c25e7c586b5a3a0787c7266877b3509a81fb467e8ee18da56c8ab617ce0c2`  
		Last Modified: Tue, 02 Jul 2024 07:08:49 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4872c58da475aeb616fa128243a6321c9c80428e0ab91eb33369b4d04aa49933`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c16f6edf08a2a6d9082a266659626a2c1a943e5ded2d202b76b00a974dc0a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586774715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43fb7aa8c8437f216e0f34b4c9c7afc9b49a883fb6e1515e5f2b432b5b88e6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e193394a16e7ce4f7319f265eb4490e90781352261c19ce610805e4db1d9e`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab12acc287d76f7ee208891bf35d50474ef788d26c99d013d705ab4e4b6e52b`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fc92950c63e0570a22a3c93548bbf86519afcb11354c0f86d73ad269d5a17`  
		Last Modified: Tue, 09 Jul 2024 19:39:38 GMT  
		Size: 412.8 MB (412798793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc6ef7512d3e9cbe1095837fd751001d3b5fe4e85e1b691a23371396cd66db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf741080bc44fe0b7220172f01f086c918fad2dc889918f935ac214a65bcd576`

```dockerfile
```

-	Layers:
	-	`sha256:40eac872f4ca581a51573364af436cbbbb85d33a3285d9eb9da982b08c61732c`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.2 MB (3188393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1734c8c05490e3e5f8cae58ce3093774c756ee923760bfe51998554ba3807`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 21.6 KB (21561 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:c3860a0f70cf2fb7da5cfe04549343d693c8cb5a4517674490b7f3b07dab1b3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:e1de83e5592894a18a1102d53886f4d8853c015393650121a76728cc5e0f82b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.9 MB (573877322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc8b629289eb167ebd9c65b003cba27b833d61721be60bcbbb63fd61a050fc4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 27 Jun 2024 14:44:46 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e432ee1bc5c723054c879803bdef8c899efb7530c4c6b5257173b55b1c5d2f52`  
		Last Modified: Thu, 27 Jun 2024 18:56:10 GMT  
		Size: 125.1 MB (125114900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2695dfb81f5e36e5e299dfbbfc3434045d1b56e0cd1e1fb567f3a007f1d97a84`  
		Last Modified: Thu, 27 Jun 2024 18:56:08 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9cec20293fe6265da7a5d56bb3c2fd25dfc7fec06432f9bbb946b17a95758d`  
		Last Modified: Thu, 27 Jun 2024 18:56:15 GMT  
		Size: 409.9 MB (409900440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d6092c087ee61b5b50a432326dbcc3db9719c92f6e4e7088cfa506a3e5045f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9370d495dcd1bf9dfa8ebd5738d14838e48a9e751fc30d85046cbde5e5e36ee5`

```dockerfile
```

-	Layers:
	-	`sha256:12efe3b36080a6686c7d1771eb30477cc5b74ce790dd84f9bb65efcf35889486`  
		Last Modified: Thu, 27 Jun 2024 18:56:09 GMT  
		Size: 5.3 MB (5273804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b603f7c60d5b1957323fcb76a3fe83861752210a01eb31283dbd2ef97eb7d53`  
		Last Modified: Thu, 27 Jun 2024 18:56:08 GMT  
		Size: 20.5 KB (20543 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55ca99e1e37a0ff24bfc225028e9341583bc2453b4563a4e72129ad55141f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572115757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfbed7bdb67fd2b50440fbcdf2cb597a3546a4f3436823ea6070a370bc29055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b3af58f0197b02815c5a3d75329582cc200673bf3f2b0ab99c35bdc87577f`  
		Last Modified: Tue, 09 Jul 2024 19:41:59 GMT  
		Size: 409.9 MB (409903184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4eaf4862d5950f34436895a3ff3b1b3393bc6a57285bdd8ab37eba918fef68c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e4c63f7fccc9ef9396728982c13b0096ceba5baf5c1b197142fc558943eb88`

```dockerfile
```

-	Layers:
	-	`sha256:2ce952bf9b1e5b78097973ea74a79e5acd85c939488585629d481428bbc9b593`  
		Last Modified: Tue, 09 Jul 2024 19:41:50 GMT  
		Size: 5.3 MB (5253043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721aafd21acb5cdb1fe8ecbad0b7869858ee2c8ffae07395ea556d57ecea6437`  
		Last Modified: Tue, 09 Jul 2024 19:41:50 GMT  
		Size: 20.9 KB (20851 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:ffc7f16288174ad6674ff60309948dc2b84720e7d3f492577e681719227e3762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f03c47badc99528a7e122359f1d901cb298f962c94e56e6db0ecd31a815add8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290949534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea0753538e414dc073e3f5299b5336cb4dc62868ee152313e6153ee617ba608`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 27 Jun 2024 14:44:46 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef536f4dad38d4029007a3c0c874bd63a8447745dd74a2e803307b2a43e4bfaf`  
		Last Modified: Thu, 27 Jun 2024 18:55:42 GMT  
		Size: 125.1 MB (125114710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea596549228e026cd5a7153b75bfd794ba892d11e18e7909e8f5fc208279042`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a357a347f1c339e3aaab4b83c91c7f2b2f54d6b7051ba5fbb3e6ba2a033cccb`  
		Last Modified: Thu, 27 Jun 2024 18:55:41 GMT  
		Size: 127.0 MB (126972847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56c7125e7ffab755468030b8fe2e3a994eb4de4ca5690696e58c115e3b8b3cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba186b67cc9e1011cf084063f71011bd1c946af3c9c650f5a512384c34d8698`

```dockerfile
```

-	Layers:
	-	`sha256:59ffbc322f49d9fe5ff2fceae0e7688414767482d15dee65b205bce61e240668`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 5.1 MB (5052363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b9b9354ebc24b732ce2edbb905f417a701385261f868679792669d4504bb71`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 21.7 KB (21721 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45002a8c43bf87404457920a508b078b950fed93d33b94fe84aa9df4ca693325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289186819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818eb2f4a3569e0b9895f3e163290015df6b951a6f8fc8f7a077c74b1db4728`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bfc506818707cec2c06a141c43764cd1a6f2701bb174bfc5e02976f59c2f4`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 127.0 MB (126974246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e262333102f509b729b4b3d09000e0ba0b83a5f447ccf396ed378ad3d5e3f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f9e3f98ceb2f833aab1c40f12b68032a447c9b355c773a472598de9879b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:8495b0264746cf1d6194e85632587569f89030c84ab424d312fd2a8becc955c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 5.0 MB (5031650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019c04b56ea5810133a05a7b17486bfcdb0b2319007fe11f4524ed2ec9d2c758`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-bullseye`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-community`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-community` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-community-bullseye`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-community-ubi9`

```console
$ docker pull neo4j@sha256:ffc7f16288174ad6674ff60309948dc2b84720e7d3f492577e681719227e3762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f03c47badc99528a7e122359f1d901cb298f962c94e56e6db0ecd31a815add8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290949534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea0753538e414dc073e3f5299b5336cb4dc62868ee152313e6153ee617ba608`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 27 Jun 2024 14:44:46 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef536f4dad38d4029007a3c0c874bd63a8447745dd74a2e803307b2a43e4bfaf`  
		Last Modified: Thu, 27 Jun 2024 18:55:42 GMT  
		Size: 125.1 MB (125114710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea596549228e026cd5a7153b75bfd794ba892d11e18e7909e8f5fc208279042`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a357a347f1c339e3aaab4b83c91c7f2b2f54d6b7051ba5fbb3e6ba2a033cccb`  
		Last Modified: Thu, 27 Jun 2024 18:55:41 GMT  
		Size: 127.0 MB (126972847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56c7125e7ffab755468030b8fe2e3a994eb4de4ca5690696e58c115e3b8b3cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba186b67cc9e1011cf084063f71011bd1c946af3c9c650f5a512384c34d8698`

```dockerfile
```

-	Layers:
	-	`sha256:59ffbc322f49d9fe5ff2fceae0e7688414767482d15dee65b205bce61e240668`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 5.1 MB (5052363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b9b9354ebc24b732ce2edbb905f417a701385261f868679792669d4504bb71`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 21.7 KB (21721 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45002a8c43bf87404457920a508b078b950fed93d33b94fe84aa9df4ca693325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289186819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818eb2f4a3569e0b9895f3e163290015df6b951a6f8fc8f7a077c74b1db4728`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bfc506818707cec2c06a141c43764cd1a6f2701bb174bfc5e02976f59c2f4`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 127.0 MB (126974246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e262333102f509b729b4b3d09000e0ba0b83a5f447ccf396ed378ad3d5e3f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f9e3f98ceb2f833aab1c40f12b68032a447c9b355c773a472598de9879b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:8495b0264746cf1d6194e85632587569f89030c84ab424d312fd2a8becc955c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 5.0 MB (5031650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019c04b56ea5810133a05a7b17486bfcdb0b2319007fe11f4524ed2ec9d2c758`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-enterprise`

```console
$ docker pull neo4j@sha256:4705e577aa259ba8ccc1fd8d656220c66534b82d4d23b0f25242ce04de339dce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d15801e2583c7ee6013df9ca4cb1a0ff7e4783fe7c407961546417c4ca39db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9870116d4be0a620eb915ac456729b0e7160370a45c7e650c8271aa1dcd5c055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe68269009ae76ebd480d4279f934c63bb9054c688088219585466bb5cc53ad`  
		Last Modified: Tue, 02 Jul 2024 07:08:53 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dbcd4df024a203f3550164811b35176f2f2f17c21d6e939760595472fdf8da`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3980dd600c2d502c04cc292cbd4ef59d30efe20b57537683a919163afd8554af`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d56046cf7f45c6eaca9e31c476e2db7365261c25a8081879631b2791a9c22ce`  
		Last Modified: Tue, 02 Jul 2024 07:08:58 GMT  
		Size: 412.8 MB (412831265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e01109e6ee3b753ca85c8c0ea230ae5808930a4b74374b127f163280352c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935c903006d0a86bcf5b9b3336e8e04c771294e64ad8893c1548cda53589dacf`

```dockerfile
```

-	Layers:
	-	`sha256:fb7c25e7c586b5a3a0787c7266877b3509a81fb467e8ee18da56c8ab617ce0c2`  
		Last Modified: Tue, 02 Jul 2024 07:08:49 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4872c58da475aeb616fa128243a6321c9c80428e0ab91eb33369b4d04aa49933`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c16f6edf08a2a6d9082a266659626a2c1a943e5ded2d202b76b00a974dc0a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586774715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43fb7aa8c8437f216e0f34b4c9c7afc9b49a883fb6e1515e5f2b432b5b88e6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e193394a16e7ce4f7319f265eb4490e90781352261c19ce610805e4db1d9e`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab12acc287d76f7ee208891bf35d50474ef788d26c99d013d705ab4e4b6e52b`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fc92950c63e0570a22a3c93548bbf86519afcb11354c0f86d73ad269d5a17`  
		Last Modified: Tue, 09 Jul 2024 19:39:38 GMT  
		Size: 412.8 MB (412798793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc6ef7512d3e9cbe1095837fd751001d3b5fe4e85e1b691a23371396cd66db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf741080bc44fe0b7220172f01f086c918fad2dc889918f935ac214a65bcd576`

```dockerfile
```

-	Layers:
	-	`sha256:40eac872f4ca581a51573364af436cbbbb85d33a3285d9eb9da982b08c61732c`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.2 MB (3188393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1734c8c05490e3e5f8cae58ce3093774c756ee923760bfe51998554ba3807`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 21.6 KB (21561 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4705e577aa259ba8ccc1fd8d656220c66534b82d4d23b0f25242ce04de339dce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d15801e2583c7ee6013df9ca4cb1a0ff7e4783fe7c407961546417c4ca39db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9870116d4be0a620eb915ac456729b0e7160370a45c7e650c8271aa1dcd5c055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe68269009ae76ebd480d4279f934c63bb9054c688088219585466bb5cc53ad`  
		Last Modified: Tue, 02 Jul 2024 07:08:53 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dbcd4df024a203f3550164811b35176f2f2f17c21d6e939760595472fdf8da`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3980dd600c2d502c04cc292cbd4ef59d30efe20b57537683a919163afd8554af`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d56046cf7f45c6eaca9e31c476e2db7365261c25a8081879631b2791a9c22ce`  
		Last Modified: Tue, 02 Jul 2024 07:08:58 GMT  
		Size: 412.8 MB (412831265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e01109e6ee3b753ca85c8c0ea230ae5808930a4b74374b127f163280352c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935c903006d0a86bcf5b9b3336e8e04c771294e64ad8893c1548cda53589dacf`

```dockerfile
```

-	Layers:
	-	`sha256:fb7c25e7c586b5a3a0787c7266877b3509a81fb467e8ee18da56c8ab617ce0c2`  
		Last Modified: Tue, 02 Jul 2024 07:08:49 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4872c58da475aeb616fa128243a6321c9c80428e0ab91eb33369b4d04aa49933`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c16f6edf08a2a6d9082a266659626a2c1a943e5ded2d202b76b00a974dc0a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586774715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43fb7aa8c8437f216e0f34b4c9c7afc9b49a883fb6e1515e5f2b432b5b88e6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e193394a16e7ce4f7319f265eb4490e90781352261c19ce610805e4db1d9e`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab12acc287d76f7ee208891bf35d50474ef788d26c99d013d705ab4e4b6e52b`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fc92950c63e0570a22a3c93548bbf86519afcb11354c0f86d73ad269d5a17`  
		Last Modified: Tue, 09 Jul 2024 19:39:38 GMT  
		Size: 412.8 MB (412798793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc6ef7512d3e9cbe1095837fd751001d3b5fe4e85e1b691a23371396cd66db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf741080bc44fe0b7220172f01f086c918fad2dc889918f935ac214a65bcd576`

```dockerfile
```

-	Layers:
	-	`sha256:40eac872f4ca581a51573364af436cbbbb85d33a3285d9eb9da982b08c61732c`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.2 MB (3188393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1734c8c05490e3e5f8cae58ce3093774c756ee923760bfe51998554ba3807`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 21.6 KB (21561 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:c3860a0f70cf2fb7da5cfe04549343d693c8cb5a4517674490b7f3b07dab1b3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:e1de83e5592894a18a1102d53886f4d8853c015393650121a76728cc5e0f82b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.9 MB (573877322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc8b629289eb167ebd9c65b003cba27b833d61721be60bcbbb63fd61a050fc4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 27 Jun 2024 14:44:46 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e432ee1bc5c723054c879803bdef8c899efb7530c4c6b5257173b55b1c5d2f52`  
		Last Modified: Thu, 27 Jun 2024 18:56:10 GMT  
		Size: 125.1 MB (125114900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2695dfb81f5e36e5e299dfbbfc3434045d1b56e0cd1e1fb567f3a007f1d97a84`  
		Last Modified: Thu, 27 Jun 2024 18:56:08 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9cec20293fe6265da7a5d56bb3c2fd25dfc7fec06432f9bbb946b17a95758d`  
		Last Modified: Thu, 27 Jun 2024 18:56:15 GMT  
		Size: 409.9 MB (409900440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d6092c087ee61b5b50a432326dbcc3db9719c92f6e4e7088cfa506a3e5045f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9370d495dcd1bf9dfa8ebd5738d14838e48a9e751fc30d85046cbde5e5e36ee5`

```dockerfile
```

-	Layers:
	-	`sha256:12efe3b36080a6686c7d1771eb30477cc5b74ce790dd84f9bb65efcf35889486`  
		Last Modified: Thu, 27 Jun 2024 18:56:09 GMT  
		Size: 5.3 MB (5273804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b603f7c60d5b1957323fcb76a3fe83861752210a01eb31283dbd2ef97eb7d53`  
		Last Modified: Thu, 27 Jun 2024 18:56:08 GMT  
		Size: 20.5 KB (20543 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55ca99e1e37a0ff24bfc225028e9341583bc2453b4563a4e72129ad55141f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572115757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfbed7bdb67fd2b50440fbcdf2cb597a3546a4f3436823ea6070a370bc29055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b3af58f0197b02815c5a3d75329582cc200673bf3f2b0ab99c35bdc87577f`  
		Last Modified: Tue, 09 Jul 2024 19:41:59 GMT  
		Size: 409.9 MB (409903184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4eaf4862d5950f34436895a3ff3b1b3393bc6a57285bdd8ab37eba918fef68c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e4c63f7fccc9ef9396728982c13b0096ceba5baf5c1b197142fc558943eb88`

```dockerfile
```

-	Layers:
	-	`sha256:2ce952bf9b1e5b78097973ea74a79e5acd85c939488585629d481428bbc9b593`  
		Last Modified: Tue, 09 Jul 2024 19:41:50 GMT  
		Size: 5.3 MB (5253043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721aafd21acb5cdb1fe8ecbad0b7869858ee2c8ffae07395ea556d57ecea6437`  
		Last Modified: Tue, 09 Jul 2024 19:41:50 GMT  
		Size: 20.9 KB (20851 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-ubi9`

```console
$ docker pull neo4j@sha256:ffc7f16288174ad6674ff60309948dc2b84720e7d3f492577e681719227e3762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f03c47badc99528a7e122359f1d901cb298f962c94e56e6db0ecd31a815add8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290949534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea0753538e414dc073e3f5299b5336cb4dc62868ee152313e6153ee617ba608`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 27 Jun 2024 14:44:46 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef536f4dad38d4029007a3c0c874bd63a8447745dd74a2e803307b2a43e4bfaf`  
		Last Modified: Thu, 27 Jun 2024 18:55:42 GMT  
		Size: 125.1 MB (125114710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea596549228e026cd5a7153b75bfd794ba892d11e18e7909e8f5fc208279042`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a357a347f1c339e3aaab4b83c91c7f2b2f54d6b7051ba5fbb3e6ba2a033cccb`  
		Last Modified: Thu, 27 Jun 2024 18:55:41 GMT  
		Size: 127.0 MB (126972847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56c7125e7ffab755468030b8fe2e3a994eb4de4ca5690696e58c115e3b8b3cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba186b67cc9e1011cf084063f71011bd1c946af3c9c650f5a512384c34d8698`

```dockerfile
```

-	Layers:
	-	`sha256:59ffbc322f49d9fe5ff2fceae0e7688414767482d15dee65b205bce61e240668`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 5.1 MB (5052363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b9b9354ebc24b732ce2edbb905f417a701385261f868679792669d4504bb71`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 21.7 KB (21721 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45002a8c43bf87404457920a508b078b950fed93d33b94fe84aa9df4ca693325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289186819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818eb2f4a3569e0b9895f3e163290015df6b951a6f8fc8f7a077c74b1db4728`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bfc506818707cec2c06a141c43764cd1a6f2701bb174bfc5e02976f59c2f4`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 127.0 MB (126974246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e262333102f509b729b4b3d09000e0ba0b83a5f447ccf396ed378ad3d5e3f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f9e3f98ceb2f833aab1c40f12b68032a447c9b355c773a472598de9879b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:8495b0264746cf1d6194e85632587569f89030c84ab424d312fd2a8becc955c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 5.0 MB (5031650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019c04b56ea5810133a05a7b17486bfcdb0b2319007fe11f4524ed2ec9d2c758`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.2`

```console
$ docker pull neo4j@sha256:a58e7fd330b60fcd32e2de9fa7cd37f00e7256a0155937d2bc17eb0a9e8b191b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.2` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.2` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.2-bullseye`

```console
$ docker pull neo4j@sha256:a58e7fd330b60fcd32e2de9fa7cd37f00e7256a0155937d2bc17eb0a9e8b191b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.2-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.2-community`

```console
$ docker pull neo4j@sha256:a58e7fd330b60fcd32e2de9fa7cd37f00e7256a0155937d2bc17eb0a9e8b191b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.2-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.2-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.2-community-bullseye`

```console
$ docker pull neo4j@sha256:a58e7fd330b60fcd32e2de9fa7cd37f00e7256a0155937d2bc17eb0a9e8b191b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.2-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.2-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.2-community-ubi9`

```console
$ docker pull neo4j@sha256:f34e4ada6d642b80603c3c4fd153b9b8d24c22e15d4127d212f7412f5abae0fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.2-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45002a8c43bf87404457920a508b078b950fed93d33b94fe84aa9df4ca693325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289186819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818eb2f4a3569e0b9895f3e163290015df6b951a6f8fc8f7a077c74b1db4728`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bfc506818707cec2c06a141c43764cd1a6f2701bb174bfc5e02976f59c2f4`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 127.0 MB (126974246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.2-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e262333102f509b729b4b3d09000e0ba0b83a5f447ccf396ed378ad3d5e3f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f9e3f98ceb2f833aab1c40f12b68032a447c9b355c773a472598de9879b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:8495b0264746cf1d6194e85632587569f89030c84ab424d312fd2a8becc955c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 5.0 MB (5031650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019c04b56ea5810133a05a7b17486bfcdb0b2319007fe11f4524ed2ec9d2c758`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.2-enterprise`

```console
$ docker pull neo4j@sha256:44ef4758294d50064385279653631895b8be6badf9b3f421ef0f63eb16983747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.2-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c16f6edf08a2a6d9082a266659626a2c1a943e5ded2d202b76b00a974dc0a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586774715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43fb7aa8c8437f216e0f34b4c9c7afc9b49a883fb6e1515e5f2b432b5b88e6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e193394a16e7ce4f7319f265eb4490e90781352261c19ce610805e4db1d9e`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab12acc287d76f7ee208891bf35d50474ef788d26c99d013d705ab4e4b6e52b`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fc92950c63e0570a22a3c93548bbf86519afcb11354c0f86d73ad269d5a17`  
		Last Modified: Tue, 09 Jul 2024 19:39:38 GMT  
		Size: 412.8 MB (412798793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.2-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc6ef7512d3e9cbe1095837fd751001d3b5fe4e85e1b691a23371396cd66db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf741080bc44fe0b7220172f01f086c918fad2dc889918f935ac214a65bcd576`

```dockerfile
```

-	Layers:
	-	`sha256:40eac872f4ca581a51573364af436cbbbb85d33a3285d9eb9da982b08c61732c`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.2 MB (3188393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1734c8c05490e3e5f8cae58ce3093774c756ee923760bfe51998554ba3807`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 21.6 KB (21561 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.2-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:44ef4758294d50064385279653631895b8be6badf9b3f421ef0f63eb16983747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.2-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c16f6edf08a2a6d9082a266659626a2c1a943e5ded2d202b76b00a974dc0a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586774715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43fb7aa8c8437f216e0f34b4c9c7afc9b49a883fb6e1515e5f2b432b5b88e6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e193394a16e7ce4f7319f265eb4490e90781352261c19ce610805e4db1d9e`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab12acc287d76f7ee208891bf35d50474ef788d26c99d013d705ab4e4b6e52b`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fc92950c63e0570a22a3c93548bbf86519afcb11354c0f86d73ad269d5a17`  
		Last Modified: Tue, 09 Jul 2024 19:39:38 GMT  
		Size: 412.8 MB (412798793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.2-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc6ef7512d3e9cbe1095837fd751001d3b5fe4e85e1b691a23371396cd66db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf741080bc44fe0b7220172f01f086c918fad2dc889918f935ac214a65bcd576`

```dockerfile
```

-	Layers:
	-	`sha256:40eac872f4ca581a51573364af436cbbbb85d33a3285d9eb9da982b08c61732c`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.2 MB (3188393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1734c8c05490e3e5f8cae58ce3093774c756ee923760bfe51998554ba3807`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 21.6 KB (21561 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.2-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:adbc5819d34f6c559eb16bda546d3874b98373c5ddd7c64e15e3649842c8e215
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.2-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55ca99e1e37a0ff24bfc225028e9341583bc2453b4563a4e72129ad55141f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572115757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfbed7bdb67fd2b50440fbcdf2cb597a3546a4f3436823ea6070a370bc29055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b3af58f0197b02815c5a3d75329582cc200673bf3f2b0ab99c35bdc87577f`  
		Last Modified: Tue, 09 Jul 2024 19:41:59 GMT  
		Size: 409.9 MB (409903184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.2-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4eaf4862d5950f34436895a3ff3b1b3393bc6a57285bdd8ab37eba918fef68c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e4c63f7fccc9ef9396728982c13b0096ceba5baf5c1b197142fc558943eb88`

```dockerfile
```

-	Layers:
	-	`sha256:2ce952bf9b1e5b78097973ea74a79e5acd85c939488585629d481428bbc9b593`  
		Last Modified: Tue, 09 Jul 2024 19:41:50 GMT  
		Size: 5.3 MB (5253043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721aafd21acb5cdb1fe8ecbad0b7869858ee2c8ffae07395ea556d57ecea6437`  
		Last Modified: Tue, 09 Jul 2024 19:41:50 GMT  
		Size: 20.9 KB (20851 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.2-ubi9`

```console
$ docker pull neo4j@sha256:f34e4ada6d642b80603c3c4fd153b9b8d24c22e15d4127d212f7412f5abae0fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.2-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45002a8c43bf87404457920a508b078b950fed93d33b94fe84aa9df4ca693325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289186819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818eb2f4a3569e0b9895f3e163290015df6b951a6f8fc8f7a077c74b1db4728`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bfc506818707cec2c06a141c43764cd1a6f2701bb174bfc5e02976f59c2f4`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 127.0 MB (126974246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.2-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e262333102f509b729b4b3d09000e0ba0b83a5f447ccf396ed378ad3d5e3f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f9e3f98ceb2f833aab1c40f12b68032a447c9b355c773a472598de9879b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:8495b0264746cf1d6194e85632587569f89030c84ab424d312fd2a8becc955c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 5.0 MB (5031650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019c04b56ea5810133a05a7b17486bfcdb0b2319007fe11f4524ed2ec9d2c758`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:ffc7f16288174ad6674ff60309948dc2b84720e7d3f492577e681719227e3762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f03c47badc99528a7e122359f1d901cb298f962c94e56e6db0ecd31a815add8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290949534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea0753538e414dc073e3f5299b5336cb4dc62868ee152313e6153ee617ba608`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 27 Jun 2024 14:44:46 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef536f4dad38d4029007a3c0c874bd63a8447745dd74a2e803307b2a43e4bfaf`  
		Last Modified: Thu, 27 Jun 2024 18:55:42 GMT  
		Size: 125.1 MB (125114710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea596549228e026cd5a7153b75bfd794ba892d11e18e7909e8f5fc208279042`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a357a347f1c339e3aaab4b83c91c7f2b2f54d6b7051ba5fbb3e6ba2a033cccb`  
		Last Modified: Thu, 27 Jun 2024 18:55:41 GMT  
		Size: 127.0 MB (126972847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56c7125e7ffab755468030b8fe2e3a994eb4de4ca5690696e58c115e3b8b3cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba186b67cc9e1011cf084063f71011bd1c946af3c9c650f5a512384c34d8698`

```dockerfile
```

-	Layers:
	-	`sha256:59ffbc322f49d9fe5ff2fceae0e7688414767482d15dee65b205bce61e240668`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 5.1 MB (5052363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b9b9354ebc24b732ce2edbb905f417a701385261f868679792669d4504bb71`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 21.7 KB (21721 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45002a8c43bf87404457920a508b078b950fed93d33b94fe84aa9df4ca693325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289186819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818eb2f4a3569e0b9895f3e163290015df6b951a6f8fc8f7a077c74b1db4728`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bfc506818707cec2c06a141c43764cd1a6f2701bb174bfc5e02976f59c2f4`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 127.0 MB (126974246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e262333102f509b729b4b3d09000e0ba0b83a5f447ccf396ed378ad3d5e3f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f9e3f98ceb2f833aab1c40f12b68032a447c9b355c773a472598de9879b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:8495b0264746cf1d6194e85632587569f89030c84ab424d312fd2a8becc955c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 5.0 MB (5031650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019c04b56ea5810133a05a7b17486bfcdb0b2319007fe11f4524ed2ec9d2c758`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:4705e577aa259ba8ccc1fd8d656220c66534b82d4d23b0f25242ce04de339dce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d15801e2583c7ee6013df9ca4cb1a0ff7e4783fe7c407961546417c4ca39db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9870116d4be0a620eb915ac456729b0e7160370a45c7e650c8271aa1dcd5c055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe68269009ae76ebd480d4279f934c63bb9054c688088219585466bb5cc53ad`  
		Last Modified: Tue, 02 Jul 2024 07:08:53 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dbcd4df024a203f3550164811b35176f2f2f17c21d6e939760595472fdf8da`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3980dd600c2d502c04cc292cbd4ef59d30efe20b57537683a919163afd8554af`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d56046cf7f45c6eaca9e31c476e2db7365261c25a8081879631b2791a9c22ce`  
		Last Modified: Tue, 02 Jul 2024 07:08:58 GMT  
		Size: 412.8 MB (412831265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e01109e6ee3b753ca85c8c0ea230ae5808930a4b74374b127f163280352c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935c903006d0a86bcf5b9b3336e8e04c771294e64ad8893c1548cda53589dacf`

```dockerfile
```

-	Layers:
	-	`sha256:fb7c25e7c586b5a3a0787c7266877b3509a81fb467e8ee18da56c8ab617ce0c2`  
		Last Modified: Tue, 02 Jul 2024 07:08:49 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4872c58da475aeb616fa128243a6321c9c80428e0ab91eb33369b4d04aa49933`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c16f6edf08a2a6d9082a266659626a2c1a943e5ded2d202b76b00a974dc0a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586774715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43fb7aa8c8437f216e0f34b4c9c7afc9b49a883fb6e1515e5f2b432b5b88e6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e193394a16e7ce4f7319f265eb4490e90781352261c19ce610805e4db1d9e`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab12acc287d76f7ee208891bf35d50474ef788d26c99d013d705ab4e4b6e52b`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fc92950c63e0570a22a3c93548bbf86519afcb11354c0f86d73ad269d5a17`  
		Last Modified: Tue, 09 Jul 2024 19:39:38 GMT  
		Size: 412.8 MB (412798793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc6ef7512d3e9cbe1095837fd751001d3b5fe4e85e1b691a23371396cd66db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf741080bc44fe0b7220172f01f086c918fad2dc889918f935ac214a65bcd576`

```dockerfile
```

-	Layers:
	-	`sha256:40eac872f4ca581a51573364af436cbbbb85d33a3285d9eb9da982b08c61732c`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.2 MB (3188393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1734c8c05490e3e5f8cae58ce3093774c756ee923760bfe51998554ba3807`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 21.6 KB (21561 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4705e577aa259ba8ccc1fd8d656220c66534b82d4d23b0f25242ce04de339dce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:d15801e2583c7ee6013df9ca4cb1a0ff7e4783fe7c407961546417c4ca39db2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9870116d4be0a620eb915ac456729b0e7160370a45c7e650c8271aa1dcd5c055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe68269009ae76ebd480d4279f934c63bb9054c688088219585466bb5cc53ad`  
		Last Modified: Tue, 02 Jul 2024 07:08:53 GMT  
		Size: 145.1 MB (145095124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dbcd4df024a203f3550164811b35176f2f2f17c21d6e939760595472fdf8da`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3980dd600c2d502c04cc292cbd4ef59d30efe20b57537683a919163afd8554af`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d56046cf7f45c6eaca9e31c476e2db7365261c25a8081879631b2791a9c22ce`  
		Last Modified: Tue, 02 Jul 2024 07:08:58 GMT  
		Size: 412.8 MB (412831265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e01109e6ee3b753ca85c8c0ea230ae5808930a4b74374b127f163280352c08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935c903006d0a86bcf5b9b3336e8e04c771294e64ad8893c1548cda53589dacf`

```dockerfile
```

-	Layers:
	-	`sha256:fb7c25e7c586b5a3a0787c7266877b3509a81fb467e8ee18da56c8ab617ce0c2`  
		Last Modified: Tue, 02 Jul 2024 07:08:49 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4872c58da475aeb616fa128243a6321c9c80428e0ab91eb33369b4d04aa49933`  
		Last Modified: Tue, 02 Jul 2024 07:08:48 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c16f6edf08a2a6d9082a266659626a2c1a943e5ded2d202b76b00a974dc0a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586774715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43fb7aa8c8437f216e0f34b4c9c7afc9b49a883fb6e1515e5f2b432b5b88e6f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597e193394a16e7ce4f7319f265eb4490e90781352261c19ce610805e4db1d9e`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab12acc287d76f7ee208891bf35d50474ef788d26c99d013d705ab4e4b6e52b`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fc92950c63e0570a22a3c93548bbf86519afcb11354c0f86d73ad269d5a17`  
		Last Modified: Tue, 09 Jul 2024 19:39:38 GMT  
		Size: 412.8 MB (412798793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc6ef7512d3e9cbe1095837fd751001d3b5fe4e85e1b691a23371396cd66db44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf741080bc44fe0b7220172f01f086c918fad2dc889918f935ac214a65bcd576`

```dockerfile
```

-	Layers:
	-	`sha256:40eac872f4ca581a51573364af436cbbbb85d33a3285d9eb9da982b08c61732c`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 3.2 MB (3188393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44b1734c8c05490e3e5f8cae58ce3093774c756ee923760bfe51998554ba3807`  
		Last Modified: Tue, 09 Jul 2024 19:39:29 GMT  
		Size: 21.6 KB (21561 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:c3860a0f70cf2fb7da5cfe04549343d693c8cb5a4517674490b7f3b07dab1b3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:e1de83e5592894a18a1102d53886f4d8853c015393650121a76728cc5e0f82b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.9 MB (573877322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc8b629289eb167ebd9c65b003cba27b833d61721be60bcbbb63fd61a050fc4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 27 Jun 2024 14:44:46 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV NEO4J_SHA256=d1761704ed2e7f01756219ea6f04fce729230ac12d8e30946b7692f49ddcdba8 NEO4J_TARBALL=neo4j-enterprise-5.21.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e432ee1bc5c723054c879803bdef8c899efb7530c4c6b5257173b55b1c5d2f52`  
		Last Modified: Thu, 27 Jun 2024 18:56:10 GMT  
		Size: 125.1 MB (125114900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2695dfb81f5e36e5e299dfbbfc3434045d1b56e0cd1e1fb567f3a007f1d97a84`  
		Last Modified: Thu, 27 Jun 2024 18:56:08 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9cec20293fe6265da7a5d56bb3c2fd25dfc7fec06432f9bbb946b17a95758d`  
		Last Modified: Thu, 27 Jun 2024 18:56:15 GMT  
		Size: 409.9 MB (409900440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d6092c087ee61b5b50a432326dbcc3db9719c92f6e4e7088cfa506a3e5045f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9370d495dcd1bf9dfa8ebd5738d14838e48a9e751fc30d85046cbde5e5e36ee5`

```dockerfile
```

-	Layers:
	-	`sha256:12efe3b36080a6686c7d1771eb30477cc5b74ce790dd84f9bb65efcf35889486`  
		Last Modified: Thu, 27 Jun 2024 18:56:09 GMT  
		Size: 5.3 MB (5273804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b603f7c60d5b1957323fcb76a3fe83861752210a01eb31283dbd2ef97eb7d53`  
		Last Modified: Thu, 27 Jun 2024 18:56:08 GMT  
		Size: 20.5 KB (20543 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d55ca99e1e37a0ff24bfc225028e9341583bc2453b4563a4e72129ad55141f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572115757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfbed7bdb67fd2b50440fbcdf2cb597a3546a4f3436823ea6070a370bc29055`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=9850004735377a931bafa0889f753ec5cf73cd6760b43971ab774024584241f1 NEO4J_TARBALL=neo4j-enterprise-5.21.2-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b3af58f0197b02815c5a3d75329582cc200673bf3f2b0ab99c35bdc87577f`  
		Last Modified: Tue, 09 Jul 2024 19:41:59 GMT  
		Size: 409.9 MB (409903184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4eaf4862d5950f34436895a3ff3b1b3393bc6a57285bdd8ab37eba918fef68c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e4c63f7fccc9ef9396728982c13b0096ceba5baf5c1b197142fc558943eb88`

```dockerfile
```

-	Layers:
	-	`sha256:2ce952bf9b1e5b78097973ea74a79e5acd85c939488585629d481428bbc9b593`  
		Last Modified: Tue, 09 Jul 2024 19:41:50 GMT  
		Size: 5.3 MB (5253043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721aafd21acb5cdb1fe8ecbad0b7869858ee2c8ffae07395ea556d57ecea6437`  
		Last Modified: Tue, 09 Jul 2024 19:41:50 GMT  
		Size: 20.9 KB (20851 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:43f28a7a146bd850f567c4bc5cdd395e64b26c4011b34ed1f845be4cbffe0b7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:27b1349d7650437a585c8ffc9f70891655073426b554724fd0a99f9edd70c59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d598bca478ec08f5a0ca884f9b2bc88c3420928408727c40d3ebdaa3404b96ac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 27 Jun 2024 14:44:46 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["bash"]
# Thu, 27 Jun 2024 14:44:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 14:44:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37a4a9d79c28e50fdb96bcfd24a0efd54ccdb7d3407215dc9e643662fa13b4`  
		Last Modified: Tue, 02 Jul 2024 07:08:08 GMT  
		Size: 145.1 MB (145095154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9676345400a6d2460e019ed1cf296fdd6ecfd93453ed1d237ac07f45f0c395c`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336408820c6bd67bf9bd791327ba53ddc86edff27996856703149346fd63f07b`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb20757b743215887c2cb575df5fed2708c0a27e39dfb70362d20ab3cb0d22`  
		Last Modified: Tue, 02 Jul 2024 07:08:09 GMT  
		Size: 129.9 MB (129899522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:e4e6ac6106918b0c2fbbbb1b4c2b0a71b653a1983486fb0bb576b2a54da80fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda2f246be6a096b88b0d508e66a88ecc5ec54924afda58c7ef7e5c570a0251`

```dockerfile
```

-	Layers:
	-	`sha256:957852aa41d4c102e7f13e168346c5d41db68f2d6b10f5481bac89ca4dfa486e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cea62f1f16cad55f4e2e431359689d756280322d2ada27bc51d3882b50c9d5e`  
		Last Modified: Tue, 02 Jul 2024 07:08:06 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:139b1200d8d5282202226910cc0ce095235a68b080c3b5b5c398af44335b2a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303845031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf82c9b9443760c50a1f69c0ea083a164ee86c63634ca171b7c7fe568eb6b716`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 09:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Jul 2024 09:34:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2078032af0a14be1eb7920a266d17321b8004bb9b70c6531591de46d84527a26`  
		Last Modified: Tue, 09 Jul 2024 19:38:15 GMT  
		Size: 143.9 MB (143892788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57507f101533bf3106c90f2a22feaaaf3af3d1ac1c5fbcf395b3b0e4c7ed6b41`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a5aa9c590ffdefd8b8071b1409d47f47e82524587d0dcfd8864cfcb8f9cdd`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ae27da2132b83317331cc6adf0605207315d69b29dc7b92ca7e9927852e27`  
		Last Modified: Tue, 09 Jul 2024 19:38:14 GMT  
		Size: 129.9 MB (129869107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:19aba376fa441c5c65a4980bc460f769f2f301f443ba5c839ac385608e7a7985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f961ca0ae6bf64171a5e1ea21cd0b2a10ace7ce14c0a8ec8cc68600730c7a18`

```dockerfile
```

-	Layers:
	-	`sha256:2e66d0f3d38569d06273ecaa5286a5d4fb1274f3954dbf0aed84c52ab68e4869`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 3.0 MB (2968242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2141c870b2f4b318dde26398aae76e98ea8c73761d7ddb98314a2482fa33747a`  
		Last Modified: Tue, 09 Jul 2024 19:38:10 GMT  
		Size: 24.0 KB (24025 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:ffc7f16288174ad6674ff60309948dc2b84720e7d3f492577e681719227e3762
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f03c47badc99528a7e122359f1d901cb298f962c94e56e6db0ecd31a815add8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290949534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea0753538e414dc073e3f5299b5336cb4dc62868ee152313e6153ee617ba608`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 06 Jun 2024 01:00:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:46 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:47 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:47 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:47 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:47 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:47 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:48 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:48 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:49 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:50 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:51 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 27 Jun 2024 14:44:46 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV NEO4J_SHA256=3451a852a986f1502b42ac74a7ca83520bdbb519d86e4d4c60f490e425057b18 NEO4J_TARBALL=neo4j-community-5.21.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
# Thu, 27 Jun 2024 14:44:46 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 27 Jun 2024 14:44:46 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 14:44:46 GMT
WORKDIR /var/lib/neo4j
# Thu, 27 Jun 2024 14:44:46 GMT
VOLUME [/data /logs]
# Thu, 27 Jun 2024 14:44:46 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 27 Jun 2024 14:44:46 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 27 Jun 2024 14:44:46 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef536f4dad38d4029007a3c0c874bd63a8447745dd74a2e803307b2a43e4bfaf`  
		Last Modified: Thu, 27 Jun 2024 18:55:42 GMT  
		Size: 125.1 MB (125114710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea596549228e026cd5a7153b75bfd794ba892d11e18e7909e8f5fc208279042`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a357a347f1c339e3aaab4b83c91c7f2b2f54d6b7051ba5fbb3e6ba2a033cccb`  
		Last Modified: Thu, 27 Jun 2024 18:55:41 GMT  
		Size: 127.0 MB (126972847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:56c7125e7ffab755468030b8fe2e3a994eb4de4ca5690696e58c115e3b8b3cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba186b67cc9e1011cf084063f71011bd1c946af3c9c650f5a512384c34d8698`

```dockerfile
```

-	Layers:
	-	`sha256:59ffbc322f49d9fe5ff2fceae0e7688414767482d15dee65b205bce61e240668`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 5.1 MB (5052363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b9b9354ebc24b732ce2edbb905f417a701385261f868679792669d4504bb71`  
		Last Modified: Thu, 27 Jun 2024 18:55:40 GMT  
		Size: 21.7 KB (21721 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45002a8c43bf87404457920a508b078b950fed93d33b94fe84aa9df4ca693325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289186819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1818eb2f4a3569e0b9895f3e163290015df6b951a6f8fc8f7a077c74b1db4728`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 06 Jun 2024 01:00:43 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 06 Jun 2024 01:00:44 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 06 Jun 2024 01:00:44 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 06 Jun 2024 01:00:44 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.expose-services=""
# Thu, 06 Jun 2024 01:00:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 06 Jun 2024 01:00:44 GMT
ENV container oci
# Thu, 06 Jun 2024 01:00:44 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Jun 2024 01:00:44 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 01:00:45 GMT
RUN rm -rf /var/log/*
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL release=1134
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 06 Jun 2024 01:00:45 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 06 Jun 2024 01:00:45 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 06 Jun 2024 01:00:47 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 06 Jun 2024 01:00:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 06 Jun 2024 01:00:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Tue, 09 Jul 2024 09:34:40 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV NEO4J_SHA256=19fd2ddbedf9fab526cdec55d1d5cbc9ebda282984f8af9fb7216d9dbc7d0af6 NEO4J_TARBALL=neo4j-community-5.21.2-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
# Tue, 09 Jul 2024 09:34:40 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.21.2-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Tue, 09 Jul 2024 09:34:40 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 09:34:40 GMT
WORKDIR /var/lib/neo4j
# Tue, 09 Jul 2024 09:34:40 GMT
VOLUME [/data /logs]
# Tue, 09 Jul 2024 09:34:40 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 09 Jul 2024 09:34:40 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 09 Jul 2024 09:34:40 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bcaf6052d94a76bac5567669157a2c0b4c1c2217304fecbcb3f3ded4e65faf`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 125.1 MB (125084528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc304a1fefb7d09d2c03c3feda525673444a04900f62b547931b332c73de48c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bfc506818707cec2c06a141c43764cd1a6f2701bb174bfc5e02976f59c2f4`  
		Last Modified: Tue, 09 Jul 2024 19:40:49 GMT  
		Size: 127.0 MB (126974246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e262333102f509b729b4b3d09000e0ba0b83a5f447ccf396ed378ad3d5e3f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f9e3f98ceb2f833aab1c40f12b68032a447c9b355c773a472598de9879b1b6`

```dockerfile
```

-	Layers:
	-	`sha256:8495b0264746cf1d6194e85632587569f89030c84ab424d312fd2a8becc955c3`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 5.0 MB (5031650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019c04b56ea5810133a05a7b17486bfcdb0b2319007fe11f4524ed2ec9d2c758`  
		Last Modified: Tue, 09 Jul 2024 19:40:46 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json
