<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.32`](#neo4j4432)
-	[`neo4j:4.4.32-community`](#neo4j4432-community)
-	[`neo4j:4.4.32-enterprise`](#neo4j4432-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi8`](#neo4j5-community-ubi8)
-	[`neo4j:5-community-ubi9`](#neo4j5-community-ubi9)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi8`](#neo4j5-enterprise-ubi8)
-	[`neo4j:5-enterprise-ubi9`](#neo4j5-enterprise-ubi9)
-	[`neo4j:5-ubi8`](#neo4j5-ubi8)
-	[`neo4j:5-ubi9`](#neo4j5-ubi9)
-	[`neo4j:5.19`](#neo4j519)
-	[`neo4j:5.19-bullseye`](#neo4j519-bullseye)
-	[`neo4j:5.19-community`](#neo4j519-community)
-	[`neo4j:5.19-community-bullseye`](#neo4j519-community-bullseye)
-	[`neo4j:5.19-community-ubi8`](#neo4j519-community-ubi8)
-	[`neo4j:5.19-community-ubi9`](#neo4j519-community-ubi9)
-	[`neo4j:5.19-enterprise`](#neo4j519-enterprise)
-	[`neo4j:5.19-enterprise-bullseye`](#neo4j519-enterprise-bullseye)
-	[`neo4j:5.19-enterprise-ubi8`](#neo4j519-enterprise-ubi8)
-	[`neo4j:5.19-enterprise-ubi9`](#neo4j519-enterprise-ubi9)
-	[`neo4j:5.19-ubi8`](#neo4j519-ubi8)
-	[`neo4j:5.19-ubi9`](#neo4j519-ubi9)
-	[`neo4j:5.19.0`](#neo4j5190)
-	[`neo4j:5.19.0-bullseye`](#neo4j5190-bullseye)
-	[`neo4j:5.19.0-community`](#neo4j5190-community)
-	[`neo4j:5.19.0-community-bullseye`](#neo4j5190-community-bullseye)
-	[`neo4j:5.19.0-community-ubi8`](#neo4j5190-community-ubi8)
-	[`neo4j:5.19.0-community-ubi9`](#neo4j5190-community-ubi9)
-	[`neo4j:5.19.0-enterprise`](#neo4j5190-enterprise)
-	[`neo4j:5.19.0-enterprise-bullseye`](#neo4j5190-enterprise-bullseye)
-	[`neo4j:5.19.0-enterprise-ubi8`](#neo4j5190-enterprise-ubi8)
-	[`neo4j:5.19.0-enterprise-ubi9`](#neo4j5190-enterprise-ubi9)
-	[`neo4j:5.19.0-ubi8`](#neo4j5190-ubi8)
-	[`neo4j:5.19.0-ubi9`](#neo4j5190-ubi9)
-	[`neo4j:bullseye`](#neo4jbullseye)
-	[`neo4j:community`](#neo4jcommunity)
-	[`neo4j:community-bullseye`](#neo4jcommunity-bullseye)
-	[`neo4j:community-ubi8`](#neo4jcommunity-ubi8)
-	[`neo4j:community-ubi9`](#neo4jcommunity-ubi9)
-	[`neo4j:enterprise`](#neo4jenterprise)
-	[`neo4j:enterprise-bullseye`](#neo4jenterprise-bullseye)
-	[`neo4j:enterprise-ubi8`](#neo4jenterprise-ubi8)
-	[`neo4j:enterprise-ubi9`](#neo4jenterprise-ubi9)
-	[`neo4j:latest`](#neo4jlatest)
-	[`neo4j:ubi8`](#neo4jubi8)
-	[`neo4j:ubi9`](#neo4jubi9)

## `neo4j:4.4`

```console
$ docker pull neo4j@sha256:e3a7a84262c89252f428f81ff9055be8cb6e130f2e4de9d922a2d53b5bb65cf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:9b28695232a5b2265bfe37a6897a614191135183a3ffc480e872aa0234c47603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297731577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43626be910bc56fcb1a6571ba2775ca1d323370aed7abd3ee995dc69dbc6dd38`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d49ff16676a07837de9ea5b826358a8ccf480984c602c58cb3bf24ed84f6abe8 NEO4J_TARBALL=neo4j-community-4.4.32-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463d49b0d89577f424a5c25eb1d028714690f2ff2de3023d3e7cd938751c2e4a`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 145.3 MB (145271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08eca3f5f19cc7b2f1945293fab3dbaaa62791e962445935c553de249b77324`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 3.9 KB (3850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5eff8a4f3966034fe3c95db61db90d89fe217b66ecc52471eee2fa6fe199ed`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e52ee18b37db30c56f653dda2d9f0d2f6e0b9f105b053d4a6b9095c180f03b`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 121.0 MB (121018888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:cd5cb4ca6e0f19b00c9a03419fa388c8117563bb362330051d63948d990eb06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fd29ec1cb21aa1ca14b2c2f7990efdd53e8090bb1ff4ba941dcb607f184487`

```dockerfile
```

-	Layers:
	-	`sha256:8c39e80b6a3e9490bf52408d4c52a78fcb20e795275c165816d6b636da1b9f8b`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 2.9 MB (2938593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0b87cdb39185aa6a3f61d69d52960a50b15e510c09a72b9599a273681aee`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ae4ba84ef2b262916a7a34ff9512057dcf430f0c941c479626d578aa48a87dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293077121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952df0f2f1baccf80fad81ee290526e137da179255ede4cffd3ca50fd9641b10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d49ff16676a07837de9ea5b826358a8ccf480984c602c58cb3bf24ed84f6abe8 NEO4J_TARBALL=neo4j-community-4.4.32-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f4a11fd2bb8956f88f33b9a3cdd0a29b6f9b2b8342e01877eda20d7a0105b9`  
		Last Modified: Wed, 10 Apr 2024 16:55:12 GMT  
		Size: 142.0 MB (142006496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2590b6d0ecef65b0efdcc5b3a7d536912bf9469973f692c45c95d6c0bd79c1c`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ca9dd7f0386f6f4f01812f89e6d80bef02419ba53ea7e9e640a4532d4c5ca9`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583d999daf8047def4c9a5a8473ffb382e14fdcb15bb012cafd8729f8b0f02e6`  
		Last Modified: Wed, 10 Apr 2024 16:55:11 GMT  
		Size: 121.0 MB (120980973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:073b5cd408d1910e9587f047cf947affccaffe2658ed603fd85fecbf3e1bbec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d20500721528c2ae95ef452281f95ed263564765b5247a8658737d3bf6656a5`

```dockerfile
```

-	Layers:
	-	`sha256:2f4092df8280e1e0f940664afe65bc07ba0854048c8a0d4a1bd428997995cd29`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 2.9 MB (2938813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f46c531361d47cbd78cec3690be547e19ae53f3fc226a8b0506f7a88ad1929e5`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:e3a7a84262c89252f428f81ff9055be8cb6e130f2e4de9d922a2d53b5bb65cf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9b28695232a5b2265bfe37a6897a614191135183a3ffc480e872aa0234c47603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297731577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43626be910bc56fcb1a6571ba2775ca1d323370aed7abd3ee995dc69dbc6dd38`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d49ff16676a07837de9ea5b826358a8ccf480984c602c58cb3bf24ed84f6abe8 NEO4J_TARBALL=neo4j-community-4.4.32-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463d49b0d89577f424a5c25eb1d028714690f2ff2de3023d3e7cd938751c2e4a`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 145.3 MB (145271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08eca3f5f19cc7b2f1945293fab3dbaaa62791e962445935c553de249b77324`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 3.9 KB (3850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5eff8a4f3966034fe3c95db61db90d89fe217b66ecc52471eee2fa6fe199ed`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e52ee18b37db30c56f653dda2d9f0d2f6e0b9f105b053d4a6b9095c180f03b`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 121.0 MB (121018888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:cd5cb4ca6e0f19b00c9a03419fa388c8117563bb362330051d63948d990eb06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fd29ec1cb21aa1ca14b2c2f7990efdd53e8090bb1ff4ba941dcb607f184487`

```dockerfile
```

-	Layers:
	-	`sha256:8c39e80b6a3e9490bf52408d4c52a78fcb20e795275c165816d6b636da1b9f8b`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 2.9 MB (2938593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0b87cdb39185aa6a3f61d69d52960a50b15e510c09a72b9599a273681aee`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ae4ba84ef2b262916a7a34ff9512057dcf430f0c941c479626d578aa48a87dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293077121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952df0f2f1baccf80fad81ee290526e137da179255ede4cffd3ca50fd9641b10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d49ff16676a07837de9ea5b826358a8ccf480984c602c58cb3bf24ed84f6abe8 NEO4J_TARBALL=neo4j-community-4.4.32-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f4a11fd2bb8956f88f33b9a3cdd0a29b6f9b2b8342e01877eda20d7a0105b9`  
		Last Modified: Wed, 10 Apr 2024 16:55:12 GMT  
		Size: 142.0 MB (142006496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2590b6d0ecef65b0efdcc5b3a7d536912bf9469973f692c45c95d6c0bd79c1c`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ca9dd7f0386f6f4f01812f89e6d80bef02419ba53ea7e9e640a4532d4c5ca9`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583d999daf8047def4c9a5a8473ffb382e14fdcb15bb012cafd8729f8b0f02e6`  
		Last Modified: Wed, 10 Apr 2024 16:55:11 GMT  
		Size: 121.0 MB (120980973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:073b5cd408d1910e9587f047cf947affccaffe2658ed603fd85fecbf3e1bbec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d20500721528c2ae95ef452281f95ed263564765b5247a8658737d3bf6656a5`

```dockerfile
```

-	Layers:
	-	`sha256:2f4092df8280e1e0f940664afe65bc07ba0854048c8a0d4a1bd428997995cd29`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 2.9 MB (2938813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f46c531361d47cbd78cec3690be547e19ae53f3fc226a8b0506f7a88ad1929e5`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:bc8d8952cb524eb1a08068582db740d49dac5797886917c511208f6bafe3c0a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c70ebb4a107c5ca17f3d76c8d9bdc899f6b852be022ae9324e7c15cadded7204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 MB (401643695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e140a4f0156525d28f4320cab4bb32ad59df84b1dd88e87b4c2534ff99fcf4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79c5dda47716101192540da2159d278ba1ed25fbc032bd68a486bc990176c9f8 NEO4J_TARBALL=neo4j-enterprise-4.4.32-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463d49b0d89577f424a5c25eb1d028714690f2ff2de3023d3e7cd938751c2e4a`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 145.3 MB (145271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c12b4dd2d2f55b614db1594c8195550ca3cff6c877003c52113bc9c07eb4768`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f9fbf53dae1eda8678fd433ce7f2da3de562e40a105c83eb0a9ae6fb3dd1b6`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47eaf67a386de8a3d84b7d0f28e615d79d9442b8a87dbae7010735725443826`  
		Last Modified: Wed, 10 Apr 2024 02:54:48 GMT  
		Size: 224.9 MB (224931017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:236d5a899d46b24c1ab6ac9db3dd1afcd85f8db6fe56ee3cdcb4140bd777ed0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39c7aaa5afacf8f64c8bfa1bb01adebeb4befa9a3b0ec0f5360817a55c89646`

```dockerfile
```

-	Layers:
	-	`sha256:6d46b51de6afac6b37b696c611a61e724352cec954f49d971dbaacf4b1de3a3b`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 3.1 MB (3067486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195d9298a623bf9c53887b41571725095be9fbc0f1f4a2afa094a0bba4d5bd38`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15223bba4ef07f603363a81cf6758342ae1e653570b20fb181f00de695bd5641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.0 MB (396992849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf2bc0b62e8aac6ba3903fef09292151b005b62d410d423c48edbbd80028eeb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79c5dda47716101192540da2159d278ba1ed25fbc032bd68a486bc990176c9f8 NEO4J_TARBALL=neo4j-enterprise-4.4.32-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f4a11fd2bb8956f88f33b9a3cdd0a29b6f9b2b8342e01877eda20d7a0105b9`  
		Last Modified: Wed, 10 Apr 2024 16:55:12 GMT  
		Size: 142.0 MB (142006496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c379421957c128b2d21c847ce5232cbff8142772ab6c21d65124f42f8f0f9c7f`  
		Last Modified: Wed, 10 Apr 2024 16:56:23 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c6dceace1ac3ec1a58e9e9fa3950b0416944604605a02714e5fe0ae17ba127`  
		Last Modified: Wed, 10 Apr 2024 16:56:23 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c18038edd4c2a06429f53ad345e9b4c96575e8d3ae607a6c2001857ec7541d`  
		Last Modified: Wed, 10 Apr 2024 16:56:28 GMT  
		Size: 224.9 MB (224896710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e9f24f641ac742c0cbd7bd3e4be0d488b7c9b6cfc5d28cc53b1449ce2f529722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3086474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f327809d2e4abd62f79514d64e719401993fbde017253186abf4a97dac36650`

```dockerfile
```

-	Layers:
	-	`sha256:d343b34a9fed55183f89bba450504d05195d81fb7775dd6a1892f300c3cd9876`  
		Last Modified: Wed, 10 Apr 2024 16:56:24 GMT  
		Size: 3.1 MB (3067702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91025ab619ae61289b1fc190354582cd042405e7fee318ba284380bd13ac9932`  
		Last Modified: Wed, 10 Apr 2024 16:56:23 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.32`

```console
$ docker pull neo4j@sha256:e3a7a84262c89252f428f81ff9055be8cb6e130f2e4de9d922a2d53b5bb65cf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.32` - linux; amd64

```console
$ docker pull neo4j@sha256:9b28695232a5b2265bfe37a6897a614191135183a3ffc480e872aa0234c47603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297731577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43626be910bc56fcb1a6571ba2775ca1d323370aed7abd3ee995dc69dbc6dd38`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d49ff16676a07837de9ea5b826358a8ccf480984c602c58cb3bf24ed84f6abe8 NEO4J_TARBALL=neo4j-community-4.4.32-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463d49b0d89577f424a5c25eb1d028714690f2ff2de3023d3e7cd938751c2e4a`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 145.3 MB (145271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08eca3f5f19cc7b2f1945293fab3dbaaa62791e962445935c553de249b77324`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 3.9 KB (3850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5eff8a4f3966034fe3c95db61db90d89fe217b66ecc52471eee2fa6fe199ed`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e52ee18b37db30c56f653dda2d9f0d2f6e0b9f105b053d4a6b9095c180f03b`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 121.0 MB (121018888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32` - unknown; unknown

```console
$ docker pull neo4j@sha256:cd5cb4ca6e0f19b00c9a03419fa388c8117563bb362330051d63948d990eb06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fd29ec1cb21aa1ca14b2c2f7990efdd53e8090bb1ff4ba941dcb607f184487`

```dockerfile
```

-	Layers:
	-	`sha256:8c39e80b6a3e9490bf52408d4c52a78fcb20e795275c165816d6b636da1b9f8b`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 2.9 MB (2938593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0b87cdb39185aa6a3f61d69d52960a50b15e510c09a72b9599a273681aee`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.32` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ae4ba84ef2b262916a7a34ff9512057dcf430f0c941c479626d578aa48a87dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293077121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952df0f2f1baccf80fad81ee290526e137da179255ede4cffd3ca50fd9641b10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d49ff16676a07837de9ea5b826358a8ccf480984c602c58cb3bf24ed84f6abe8 NEO4J_TARBALL=neo4j-community-4.4.32-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f4a11fd2bb8956f88f33b9a3cdd0a29b6f9b2b8342e01877eda20d7a0105b9`  
		Last Modified: Wed, 10 Apr 2024 16:55:12 GMT  
		Size: 142.0 MB (142006496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2590b6d0ecef65b0efdcc5b3a7d536912bf9469973f692c45c95d6c0bd79c1c`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ca9dd7f0386f6f4f01812f89e6d80bef02419ba53ea7e9e640a4532d4c5ca9`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583d999daf8047def4c9a5a8473ffb382e14fdcb15bb012cafd8729f8b0f02e6`  
		Last Modified: Wed, 10 Apr 2024 16:55:11 GMT  
		Size: 121.0 MB (120980973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32` - unknown; unknown

```console
$ docker pull neo4j@sha256:073b5cd408d1910e9587f047cf947affccaffe2658ed603fd85fecbf3e1bbec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d20500721528c2ae95ef452281f95ed263564765b5247a8658737d3bf6656a5`

```dockerfile
```

-	Layers:
	-	`sha256:2f4092df8280e1e0f940664afe65bc07ba0854048c8a0d4a1bd428997995cd29`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 2.9 MB (2938813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f46c531361d47cbd78cec3690be547e19ae53f3fc226a8b0506f7a88ad1929e5`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.32-community`

```console
$ docker pull neo4j@sha256:e3a7a84262c89252f428f81ff9055be8cb6e130f2e4de9d922a2d53b5bb65cf7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.32-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9b28695232a5b2265bfe37a6897a614191135183a3ffc480e872aa0234c47603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297731577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43626be910bc56fcb1a6571ba2775ca1d323370aed7abd3ee995dc69dbc6dd38`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d49ff16676a07837de9ea5b826358a8ccf480984c602c58cb3bf24ed84f6abe8 NEO4J_TARBALL=neo4j-community-4.4.32-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463d49b0d89577f424a5c25eb1d028714690f2ff2de3023d3e7cd938751c2e4a`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 145.3 MB (145271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08eca3f5f19cc7b2f1945293fab3dbaaa62791e962445935c553de249b77324`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 3.9 KB (3850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5eff8a4f3966034fe3c95db61db90d89fe217b66ecc52471eee2fa6fe199ed`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e52ee18b37db30c56f653dda2d9f0d2f6e0b9f105b053d4a6b9095c180f03b`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 121.0 MB (121018888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:cd5cb4ca6e0f19b00c9a03419fa388c8117563bb362330051d63948d990eb06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fd29ec1cb21aa1ca14b2c2f7990efdd53e8090bb1ff4ba941dcb607f184487`

```dockerfile
```

-	Layers:
	-	`sha256:8c39e80b6a3e9490bf52408d4c52a78fcb20e795275c165816d6b636da1b9f8b`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 2.9 MB (2938593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3b0b87cdb39185aa6a3f61d69d52960a50b15e510c09a72b9599a273681aee`  
		Last Modified: Wed, 10 Apr 2024 02:54:41 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.32-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ae4ba84ef2b262916a7a34ff9512057dcf430f0c941c479626d578aa48a87dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293077121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952df0f2f1baccf80fad81ee290526e137da179255ede4cffd3ca50fd9641b10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=d49ff16676a07837de9ea5b826358a8ccf480984c602c58cb3bf24ed84f6abe8 NEO4J_TARBALL=neo4j-community-4.4.32-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f4a11fd2bb8956f88f33b9a3cdd0a29b6f9b2b8342e01877eda20d7a0105b9`  
		Last Modified: Wed, 10 Apr 2024 16:55:12 GMT  
		Size: 142.0 MB (142006496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2590b6d0ecef65b0efdcc5b3a7d536912bf9469973f692c45c95d6c0bd79c1c`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ca9dd7f0386f6f4f01812f89e6d80bef02419ba53ea7e9e640a4532d4c5ca9`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583d999daf8047def4c9a5a8473ffb382e14fdcb15bb012cafd8729f8b0f02e6`  
		Last Modified: Wed, 10 Apr 2024 16:55:11 GMT  
		Size: 121.0 MB (120980973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:073b5cd408d1910e9587f047cf947affccaffe2658ed603fd85fecbf3e1bbec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d20500721528c2ae95ef452281f95ed263564765b5247a8658737d3bf6656a5`

```dockerfile
```

-	Layers:
	-	`sha256:2f4092df8280e1e0f940664afe65bc07ba0854048c8a0d4a1bd428997995cd29`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 2.9 MB (2938813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f46c531361d47cbd78cec3690be547e19ae53f3fc226a8b0506f7a88ad1929e5`  
		Last Modified: Wed, 10 Apr 2024 16:55:08 GMT  
		Size: 19.3 KB (19344 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.32-enterprise`

```console
$ docker pull neo4j@sha256:bc8d8952cb524eb1a08068582db740d49dac5797886917c511208f6bafe3c0a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.32-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c70ebb4a107c5ca17f3d76c8d9bdc899f6b852be022ae9324e7c15cadded7204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 MB (401643695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e140a4f0156525d28f4320cab4bb32ad59df84b1dd88e87b4c2534ff99fcf4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79c5dda47716101192540da2159d278ba1ed25fbc032bd68a486bc990176c9f8 NEO4J_TARBALL=neo4j-enterprise-4.4.32-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463d49b0d89577f424a5c25eb1d028714690f2ff2de3023d3e7cd938751c2e4a`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 145.3 MB (145271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c12b4dd2d2f55b614db1594c8195550ca3cff6c877003c52113bc9c07eb4768`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f9fbf53dae1eda8678fd433ce7f2da3de562e40a105c83eb0a9ae6fb3dd1b6`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47eaf67a386de8a3d84b7d0f28e615d79d9442b8a87dbae7010735725443826`  
		Last Modified: Wed, 10 Apr 2024 02:54:48 GMT  
		Size: 224.9 MB (224931017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:236d5a899d46b24c1ab6ac9db3dd1afcd85f8db6fe56ee3cdcb4140bd777ed0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39c7aaa5afacf8f64c8bfa1bb01adebeb4befa9a3b0ec0f5360817a55c89646`

```dockerfile
```

-	Layers:
	-	`sha256:6d46b51de6afac6b37b696c611a61e724352cec954f49d971dbaacf4b1de3a3b`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 3.1 MB (3067486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195d9298a623bf9c53887b41571725095be9fbc0f1f4a2afa094a0bba4d5bd38`  
		Last Modified: Wed, 10 Apr 2024 02:54:44 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.32-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:15223bba4ef07f603363a81cf6758342ae1e653570b20fb181f00de695bd5641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.0 MB (396992849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf2bc0b62e8aac6ba3903fef09292151b005b62d410d423c48edbbd80028eeb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 26 Mar 2024 09:59:35 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["bash"]
# Tue, 26 Mar 2024 09:59:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Mar 2024 09:59:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=79c5dda47716101192540da2159d278ba1ed25fbc032bd68a486bc990176c9f8 NEO4J_TARBALL=neo4j-enterprise-4.4.32-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.32-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 26 Mar 2024 09:59:35 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Mar 2024 09:59:35 GMT
WORKDIR /var/lib/neo4j
# Tue, 26 Mar 2024 09:59:35 GMT
VOLUME [/data /logs]
# Tue, 26 Mar 2024 09:59:35 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 26 Mar 2024 09:59:35 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 26 Mar 2024 09:59:35 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f4a11fd2bb8956f88f33b9a3cdd0a29b6f9b2b8342e01877eda20d7a0105b9`  
		Last Modified: Wed, 10 Apr 2024 16:55:12 GMT  
		Size: 142.0 MB (142006496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c379421957c128b2d21c847ce5232cbff8142772ab6c21d65124f42f8f0f9c7f`  
		Last Modified: Wed, 10 Apr 2024 16:56:23 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c6dceace1ac3ec1a58e9e9fa3950b0416944604605a02714e5fe0ae17ba127`  
		Last Modified: Wed, 10 Apr 2024 16:56:23 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c18038edd4c2a06429f53ad345e9b4c96575e8d3ae607a6c2001857ec7541d`  
		Last Modified: Wed, 10 Apr 2024 16:56:28 GMT  
		Size: 224.9 MB (224896710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e9f24f641ac742c0cbd7bd3e4be0d488b7c9b6cfc5d28cc53b1449ce2f529722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3086474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f327809d2e4abd62f79514d64e719401993fbde017253186abf4a97dac36650`

```dockerfile
```

-	Layers:
	-	`sha256:d343b34a9fed55183f89bba450504d05195d81fb7775dd6a1892f300c3cd9876`  
		Last Modified: Wed, 10 Apr 2024 16:56:24 GMT  
		Size: 3.1 MB (3067702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91025ab619ae61289b1fc190354582cd042405e7fee318ba284380bd13ac9932`  
		Last Modified: Wed, 10 Apr 2024 16:56:23 GMT  
		Size: 18.8 KB (18772 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:8f01f7bb053e5564eb84a3f1824e4ca2202d29dd415d196cf8e27c8f7e6b611e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:0cd023a61a7db68382fa6f1487a2dc1fc3affc104f14065668377a85d3ba4065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300375577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c23c35dfe5d5ec73cb5f1c972000bbea3c24b39e742d5114d38c6d7e63c60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e33d951618549541cc068ed17683ff2a3f0b7cbefea016f222096d9cb22b0`  
		Last Modified: Wed, 10 Apr 2024 02:54:58 GMT  
		Size: 144.9 MB (144893016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1c3182522949778e5775b24fd74db5bc3c6cd2438e249f07221a9bdbb32c5`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631513be69398c8e1a0bdcbf7f8f4825d8d6ad957edb79a26a17affdc4be8489`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d27ab0005a260d857e1c197b6aa1fd50c2747093dd83f48cb4ecd8b7b5080`  
		Last Modified: Wed, 10 Apr 2024 02:54:57 GMT  
		Size: 124.0 MB (124041409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:6eda6f886e066d809f6d2867b361c4549af878d178cbab1b51b1ac7a6f21242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad817d89123afe185e097c6bcbfbe211166906f5537259911e35a2736ccdc9e2`

```dockerfile
```

-	Layers:
	-	`sha256:2366739bae468fca36e28b7f4fa1f1776b74b169cdbd2cb2780e614f8dacabea`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd516509b7fd549ae344d8509ec9caae568039fc8cc706fc685c6445d7328ecc`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ec690a8774668fb32f2625f94bd4b4f08503e8a5d8a8bd9cb6d4be8a837648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297817119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ec57403fc86eb4c39f8e291f1e186f4a67941b1fac02bea42bad3ca9debdfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b5186423c9272e3df067a07d722326f5e0024bd939d2174a951618e2198d34`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a87ea67ac4b21223193e74488d97a23f3a2c6927edcc799fce5bd2b2e39c441`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33436c4395f3381e3f6dcbcf996536c598c86eaa06b9fbcddf55593178a2dea6`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 124.0 MB (124006958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:5db59e0022877bdb072a79ab24a4d449fd847bdce6cbb5c029644d19ca12219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c23cac791cbbd3f4051ceb70b23fade9cf32f0c6f57fccae572356ec94b63f`

```dockerfile
```

-	Layers:
	-	`sha256:b6a30ffaf392f55ce48e1dd5d51f254e70efaea64ff92c8f0fb5ebd5b53b9414`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f77a18924df862c1ee6ae480e3b26f59104cba1346694c374c8d7efd284391a`  
		Last Modified: Wed, 10 Apr 2024 16:52:44 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:8f01f7bb053e5564eb84a3f1824e4ca2202d29dd415d196cf8e27c8f7e6b611e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0cd023a61a7db68382fa6f1487a2dc1fc3affc104f14065668377a85d3ba4065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300375577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c23c35dfe5d5ec73cb5f1c972000bbea3c24b39e742d5114d38c6d7e63c60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e33d951618549541cc068ed17683ff2a3f0b7cbefea016f222096d9cb22b0`  
		Last Modified: Wed, 10 Apr 2024 02:54:58 GMT  
		Size: 144.9 MB (144893016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1c3182522949778e5775b24fd74db5bc3c6cd2438e249f07221a9bdbb32c5`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631513be69398c8e1a0bdcbf7f8f4825d8d6ad957edb79a26a17affdc4be8489`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d27ab0005a260d857e1c197b6aa1fd50c2747093dd83f48cb4ecd8b7b5080`  
		Last Modified: Wed, 10 Apr 2024 02:54:57 GMT  
		Size: 124.0 MB (124041409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:6eda6f886e066d809f6d2867b361c4549af878d178cbab1b51b1ac7a6f21242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad817d89123afe185e097c6bcbfbe211166906f5537259911e35a2736ccdc9e2`

```dockerfile
```

-	Layers:
	-	`sha256:2366739bae468fca36e28b7f4fa1f1776b74b169cdbd2cb2780e614f8dacabea`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd516509b7fd549ae344d8509ec9caae568039fc8cc706fc685c6445d7328ecc`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ec690a8774668fb32f2625f94bd4b4f08503e8a5d8a8bd9cb6d4be8a837648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297817119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ec57403fc86eb4c39f8e291f1e186f4a67941b1fac02bea42bad3ca9debdfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b5186423c9272e3df067a07d722326f5e0024bd939d2174a951618e2198d34`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a87ea67ac4b21223193e74488d97a23f3a2c6927edcc799fce5bd2b2e39c441`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33436c4395f3381e3f6dcbcf996536c598c86eaa06b9fbcddf55593178a2dea6`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 124.0 MB (124006958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5db59e0022877bdb072a79ab24a4d449fd847bdce6cbb5c029644d19ca12219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c23cac791cbbd3f4051ceb70b23fade9cf32f0c6f57fccae572356ec94b63f`

```dockerfile
```

-	Layers:
	-	`sha256:b6a30ffaf392f55ce48e1dd5d51f254e70efaea64ff92c8f0fb5ebd5b53b9414`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f77a18924df862c1ee6ae480e3b26f59104cba1346694c374c8d7efd284391a`  
		Last Modified: Wed, 10 Apr 2024 16:52:44 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:8f01f7bb053e5564eb84a3f1824e4ca2202d29dd415d196cf8e27c8f7e6b611e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:0cd023a61a7db68382fa6f1487a2dc1fc3affc104f14065668377a85d3ba4065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300375577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c23c35dfe5d5ec73cb5f1c972000bbea3c24b39e742d5114d38c6d7e63c60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e33d951618549541cc068ed17683ff2a3f0b7cbefea016f222096d9cb22b0`  
		Last Modified: Wed, 10 Apr 2024 02:54:58 GMT  
		Size: 144.9 MB (144893016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1c3182522949778e5775b24fd74db5bc3c6cd2438e249f07221a9bdbb32c5`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631513be69398c8e1a0bdcbf7f8f4825d8d6ad957edb79a26a17affdc4be8489`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d27ab0005a260d857e1c197b6aa1fd50c2747093dd83f48cb4ecd8b7b5080`  
		Last Modified: Wed, 10 Apr 2024 02:54:57 GMT  
		Size: 124.0 MB (124041409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:6eda6f886e066d809f6d2867b361c4549af878d178cbab1b51b1ac7a6f21242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad817d89123afe185e097c6bcbfbe211166906f5537259911e35a2736ccdc9e2`

```dockerfile
```

-	Layers:
	-	`sha256:2366739bae468fca36e28b7f4fa1f1776b74b169cdbd2cb2780e614f8dacabea`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd516509b7fd549ae344d8509ec9caae568039fc8cc706fc685c6445d7328ecc`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ec690a8774668fb32f2625f94bd4b4f08503e8a5d8a8bd9cb6d4be8a837648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297817119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ec57403fc86eb4c39f8e291f1e186f4a67941b1fac02bea42bad3ca9debdfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b5186423c9272e3df067a07d722326f5e0024bd939d2174a951618e2198d34`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a87ea67ac4b21223193e74488d97a23f3a2c6927edcc799fce5bd2b2e39c441`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33436c4395f3381e3f6dcbcf996536c598c86eaa06b9fbcddf55593178a2dea6`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 124.0 MB (124006958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5db59e0022877bdb072a79ab24a4d449fd847bdce6cbb5c029644d19ca12219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c23cac791cbbd3f4051ceb70b23fade9cf32f0c6f57fccae572356ec94b63f`

```dockerfile
```

-	Layers:
	-	`sha256:b6a30ffaf392f55ce48e1dd5d51f254e70efaea64ff92c8f0fb5ebd5b53b9414`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f77a18924df862c1ee6ae480e3b26f59104cba1346694c374c8d7efd284391a`  
		Last Modified: Wed, 10 Apr 2024 16:52:44 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:8f01f7bb053e5564eb84a3f1824e4ca2202d29dd415d196cf8e27c8f7e6b611e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0cd023a61a7db68382fa6f1487a2dc1fc3affc104f14065668377a85d3ba4065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300375577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c23c35dfe5d5ec73cb5f1c972000bbea3c24b39e742d5114d38c6d7e63c60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e33d951618549541cc068ed17683ff2a3f0b7cbefea016f222096d9cb22b0`  
		Last Modified: Wed, 10 Apr 2024 02:54:58 GMT  
		Size: 144.9 MB (144893016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1c3182522949778e5775b24fd74db5bc3c6cd2438e249f07221a9bdbb32c5`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631513be69398c8e1a0bdcbf7f8f4825d8d6ad957edb79a26a17affdc4be8489`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d27ab0005a260d857e1c197b6aa1fd50c2747093dd83f48cb4ecd8b7b5080`  
		Last Modified: Wed, 10 Apr 2024 02:54:57 GMT  
		Size: 124.0 MB (124041409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:6eda6f886e066d809f6d2867b361c4549af878d178cbab1b51b1ac7a6f21242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad817d89123afe185e097c6bcbfbe211166906f5537259911e35a2736ccdc9e2`

```dockerfile
```

-	Layers:
	-	`sha256:2366739bae468fca36e28b7f4fa1f1776b74b169cdbd2cb2780e614f8dacabea`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd516509b7fd549ae344d8509ec9caae568039fc8cc706fc685c6445d7328ecc`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ec690a8774668fb32f2625f94bd4b4f08503e8a5d8a8bd9cb6d4be8a837648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297817119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ec57403fc86eb4c39f8e291f1e186f4a67941b1fac02bea42bad3ca9debdfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b5186423c9272e3df067a07d722326f5e0024bd939d2174a951618e2198d34`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a87ea67ac4b21223193e74488d97a23f3a2c6927edcc799fce5bd2b2e39c441`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33436c4395f3381e3f6dcbcf996536c598c86eaa06b9fbcddf55593178a2dea6`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 124.0 MB (124006958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5db59e0022877bdb072a79ab24a4d449fd847bdce6cbb5c029644d19ca12219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c23cac791cbbd3f4051ceb70b23fade9cf32f0c6f57fccae572356ec94b63f`

```dockerfile
```

-	Layers:
	-	`sha256:b6a30ffaf392f55ce48e1dd5d51f254e70efaea64ff92c8f0fb5ebd5b53b9414`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f77a18924df862c1ee6ae480e3b26f59104cba1346694c374c8d7efd284391a`  
		Last Modified: Wed, 10 Apr 2024 16:52:44 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:745cfda6713a7fa14f763d0730f464fd5b16afaccf5328ff9b4c5785c87b5f37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7892fadf588136b4995e2dadb3258bb4036bcbcd6379137f921e88932f349f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557177856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46da598369fb6e4773cdfb331b7bf71c2c92e4201c7e4716e38ee1194db98ada`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a00cc2b21f5ecd3de405268bf01e364c9695aed0737469fdec7d8598e24369`  
		Last Modified: Wed, 10 Apr 2024 02:54:48 GMT  
		Size: 144.9 MB (144893017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662af1be01460b8b6a12b6d6dd173ee13703a93763e37d44e8468ff5afbb72b6`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3ce273d4caa4113bffd2595fffe729336220ef0d49c290805cf33947af05e3`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838446ef71babdb652a97f2127783fa27993fbd3be0fa25e0ce234bcad36c8e`  
		Last Modified: Wed, 10 Apr 2024 02:54:52 GMT  
		Size: 380.8 MB (380843689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ea539a331c4295ad1c1934aa89a9a9ab422805da05507c569729929af559beed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e4b72d6ca7896894cf2915e3d9dbb1650fe03e201f5422649a504d25e8276f`

```dockerfile
```

-	Layers:
	-	`sha256:8153b48968317229e8e8cfa6cc1a8a005958c7730cbbcd2557d20dfba4854104`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7277080f0f69b3888a88bf5408b7ff210339d4af40033b70d9ffb81f44eecd71`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b1f253281cf41373367f814b7c8f9a68b87e35b973fb679d40dc53adefea8b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554618001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adb26df3f32ff6f1c870da02c7e6548b897694cfa6c7fe0af186b278cf303e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee51cb7d7a462689dab9be72845d2a86126e29d8b25e913ad83b8b38534e6a9`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc455094a2a3133f7906a1fa449efeb8c0f342563708fd0b43aa816251a4892d`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ef254a7b2994d44045b0a7479d1361f9f6c33c0d89374bed4b3edc60e6ecd4`  
		Last Modified: Wed, 10 Apr 2024 16:54:09 GMT  
		Size: 380.8 MB (380807841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:055a1e3c950bd52adccc2b6164b8f2967a59f8454e559163b82f6e72568d45a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc983ae56550c8ecd29e41b8d439890a43a58ed0d53d93270aa28e3b849dae48`

```dockerfile
```

-	Layers:
	-	`sha256:5d53089e355997c348cab74154b9cdda684635735dd9d556e55b64b729d085ca`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35309ba1616779ead45454e1a104337f7dac847ea46b0f7c23f42899d972095d`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:745cfda6713a7fa14f763d0730f464fd5b16afaccf5328ff9b4c5785c87b5f37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:7892fadf588136b4995e2dadb3258bb4036bcbcd6379137f921e88932f349f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557177856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46da598369fb6e4773cdfb331b7bf71c2c92e4201c7e4716e38ee1194db98ada`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a00cc2b21f5ecd3de405268bf01e364c9695aed0737469fdec7d8598e24369`  
		Last Modified: Wed, 10 Apr 2024 02:54:48 GMT  
		Size: 144.9 MB (144893017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662af1be01460b8b6a12b6d6dd173ee13703a93763e37d44e8468ff5afbb72b6`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3ce273d4caa4113bffd2595fffe729336220ef0d49c290805cf33947af05e3`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838446ef71babdb652a97f2127783fa27993fbd3be0fa25e0ce234bcad36c8e`  
		Last Modified: Wed, 10 Apr 2024 02:54:52 GMT  
		Size: 380.8 MB (380843689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ea539a331c4295ad1c1934aa89a9a9ab422805da05507c569729929af559beed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e4b72d6ca7896894cf2915e3d9dbb1650fe03e201f5422649a504d25e8276f`

```dockerfile
```

-	Layers:
	-	`sha256:8153b48968317229e8e8cfa6cc1a8a005958c7730cbbcd2557d20dfba4854104`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7277080f0f69b3888a88bf5408b7ff210339d4af40033b70d9ffb81f44eecd71`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b1f253281cf41373367f814b7c8f9a68b87e35b973fb679d40dc53adefea8b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554618001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adb26df3f32ff6f1c870da02c7e6548b897694cfa6c7fe0af186b278cf303e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee51cb7d7a462689dab9be72845d2a86126e29d8b25e913ad83b8b38534e6a9`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc455094a2a3133f7906a1fa449efeb8c0f342563708fd0b43aa816251a4892d`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ef254a7b2994d44045b0a7479d1361f9f6c33c0d89374bed4b3edc60e6ecd4`  
		Last Modified: Wed, 10 Apr 2024 16:54:09 GMT  
		Size: 380.8 MB (380807841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:055a1e3c950bd52adccc2b6164b8f2967a59f8454e559163b82f6e72568d45a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc983ae56550c8ecd29e41b8d439890a43a58ed0d53d93270aa28e3b849dae48`

```dockerfile
```

-	Layers:
	-	`sha256:5d53089e355997c348cab74154b9cdda684635735dd9d556e55b64b729d085ca`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35309ba1616779ead45454e1a104337f7dac847ea46b0f7c23f42899d972095d`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:028d39afde25cffc412bd4d2215250643b8f78994d999d8ca44b2b6bca1e0116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:bdc85e7d4dda1d59301314fb7411398a4d8d9c76c09bfc2f31790024f20d1b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20263cfa9aaae7114b8a5e314d98325104d8c1b9f969dfcb22ec79b6fac1fde4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeaf0187031d5e65bed357c6a79752d9e5def9ee9c53c3be6c6c3a042bc5db`  
		Last Modified: Mon, 18 Mar 2024 18:37:37 GMT  
		Size: 163.6 MB (163561416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b5d48fa2aecee03dafb6be8f4133326c101ef017d6b353f7c61000ffd00fcf`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426c1d7f95efe077824e87e2534eae9acaf2a719a279c696e8feccf83a1a3fac`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 377.9 MB (377910398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:704bd376a838562ab1f9ed5ec7288f06e2bab7f4425d34e2508f0e2d5cb31487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be44e245386a0a32d7fa3e3a5026e0b3a94e589aa051c76dd77ed75c9f9390d`

```dockerfile
```

-	Layers:
	-	`sha256:aad12e01053fbf9b990734de91969d5905dd48ea47c992855ad91b536d266eeb`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e6f109446db0aba96c1b07f80229504fce79d3e7fb0c35bd61fc27424f6d4a`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:328f1909789e22d0fed607229291370642425be5d1e83b8911a10b5d8adfc6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7dce4ba3e76d332624612779eed331747d02149a43e087c72f82aca41dd3bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9296980305731d7ce62d092c2576cd341a35385e56a58fd11d67b12b96b3caa`  
		Last Modified: Mon, 18 Mar 2024 20:13:13 GMT  
		Size: 377.9 MB (377910224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:77985fbc6e6f95bdc5a6dab6a9125d77e138ba17262492f854ae69d6824dbe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97767c981b1268424128c71497280ecb5108d633eb059da5206e4d9471ff6a2`

```dockerfile
```

-	Layers:
	-	`sha256:bd439036cf03f79f376ff66cccc71f5ab7ac8038ddf54945fba09eb2e8e4979f`  
		Last Modified: Mon, 18 Mar 2024 20:12:55 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec919468a70abc4da3f758702c2efad7ebdacb31bc73b1e41407dd93b86bf9c`  
		Last Modified: Mon, 18 Mar 2024 20:12:54 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:84c02c864777ed97a8431e3b9b4406a7f49966ccd8fc86fd6db76115c01e05b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:dc763c74655873adb0691329c58edfc7552a02bbff786b085ce9d5d66e9918b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27239bba9891c68d24b03b42cd9d2b85801384d7a2dc293543227fa7de783be`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a24476c4520b1e9c9c66d29c1916e9e62c5a75316e29ce3fc9fff11b59a152`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 257.0 MB (257005824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba5a03dc0af0cc8ce429c45c6639db251f0567674616f890010b13763bc4ed6`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267d38eaffbe637912c68444a66b1b720b609ff2c3877135c3db5abd3d0797d`  
		Last Modified: Mon, 18 Mar 2024 18:37:48 GMT  
		Size: 377.9 MB (377910325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:36c457c46727f8ebd718971ffcb9de0304cb9a2e9cf0b51ef835dab7d6ab5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca751d616a406313aad5d5bd4fe7b36bdea60a843af03a2ff29f8e8758f369`

```dockerfile
```

-	Layers:
	-	`sha256:b51c8a0bdf7d22f2b4d2de07406b6a825c1e5a91801de492f35ef31d6a49c0e0`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb72743887e25635a510673c39ec83b5ae9120532fbdaa247017ce2d4e86544c`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:486cdbb0fd895d792b1567b6f2a7d8d2f0df705a0d5c42e523c4b7454fa144ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663463358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71973171c1f949830ac2f9e3c0c32edb51256f100017d5cabb477aff0877c081`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c609b766a135e00a9ded0424884aa346927f42d3db21d2f80d5dda20599bca5`  
		Last Modified: Mon, 18 Mar 2024 19:58:41 GMT  
		Size: 377.9 MB (377910423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e531c0248bccb0822ada97cfd969348dee3a50f9e4b74ec0733fca4e95642009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ab395c80e808d14fb3aae0e1d2a6183466a98b44958df3061f13375cfbba85`

```dockerfile
```

-	Layers:
	-	`sha256:7954b29e2052c6a0e0dfc227614f61aa18e39ca8069ba1657527e4a934de63cc`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d49e13727dc2f6e004439b75b5a58c304c8e36de7be9a0d3e47d6e7729dff82`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 19.8 KB (19785 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19`

**does not exist** (yet?)

## `neo4j:5.19-bullseye`

**does not exist** (yet?)

## `neo4j:5.19-community`

**does not exist** (yet?)

## `neo4j:5.19-community-bullseye`

**does not exist** (yet?)

## `neo4j:5.19-community-ubi8`

**does not exist** (yet?)

## `neo4j:5.19-community-ubi9`

**does not exist** (yet?)

## `neo4j:5.19-enterprise`

**does not exist** (yet?)

## `neo4j:5.19-enterprise-bullseye`

**does not exist** (yet?)

## `neo4j:5.19-enterprise-ubi8`

**does not exist** (yet?)

## `neo4j:5.19-enterprise-ubi9`

**does not exist** (yet?)

## `neo4j:5.19-ubi8`

**does not exist** (yet?)

## `neo4j:5.19-ubi9`

**does not exist** (yet?)

## `neo4j:5.19.0`

**does not exist** (yet?)

## `neo4j:5.19.0-bullseye`

**does not exist** (yet?)

## `neo4j:5.19.0-community`

**does not exist** (yet?)

## `neo4j:5.19.0-community-bullseye`

**does not exist** (yet?)

## `neo4j:5.19.0-community-ubi8`

**does not exist** (yet?)

## `neo4j:5.19.0-community-ubi9`

**does not exist** (yet?)

## `neo4j:5.19.0-enterprise`

**does not exist** (yet?)

## `neo4j:5.19.0-enterprise-bullseye`

**does not exist** (yet?)

## `neo4j:5.19.0-enterprise-ubi8`

**does not exist** (yet?)

## `neo4j:5.19.0-enterprise-ubi9`

**does not exist** (yet?)

## `neo4j:5.19.0-ubi8`

**does not exist** (yet?)

## `neo4j:5.19.0-ubi9`

**does not exist** (yet?)

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:8f01f7bb053e5564eb84a3f1824e4ca2202d29dd415d196cf8e27c8f7e6b611e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0cd023a61a7db68382fa6f1487a2dc1fc3affc104f14065668377a85d3ba4065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300375577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c23c35dfe5d5ec73cb5f1c972000bbea3c24b39e742d5114d38c6d7e63c60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e33d951618549541cc068ed17683ff2a3f0b7cbefea016f222096d9cb22b0`  
		Last Modified: Wed, 10 Apr 2024 02:54:58 GMT  
		Size: 144.9 MB (144893016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1c3182522949778e5775b24fd74db5bc3c6cd2438e249f07221a9bdbb32c5`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631513be69398c8e1a0bdcbf7f8f4825d8d6ad957edb79a26a17affdc4be8489`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d27ab0005a260d857e1c197b6aa1fd50c2747093dd83f48cb4ecd8b7b5080`  
		Last Modified: Wed, 10 Apr 2024 02:54:57 GMT  
		Size: 124.0 MB (124041409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:6eda6f886e066d809f6d2867b361c4549af878d178cbab1b51b1ac7a6f21242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad817d89123afe185e097c6bcbfbe211166906f5537259911e35a2736ccdc9e2`

```dockerfile
```

-	Layers:
	-	`sha256:2366739bae468fca36e28b7f4fa1f1776b74b169cdbd2cb2780e614f8dacabea`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd516509b7fd549ae344d8509ec9caae568039fc8cc706fc685c6445d7328ecc`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ec690a8774668fb32f2625f94bd4b4f08503e8a5d8a8bd9cb6d4be8a837648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297817119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ec57403fc86eb4c39f8e291f1e186f4a67941b1fac02bea42bad3ca9debdfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b5186423c9272e3df067a07d722326f5e0024bd939d2174a951618e2198d34`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a87ea67ac4b21223193e74488d97a23f3a2c6927edcc799fce5bd2b2e39c441`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33436c4395f3381e3f6dcbcf996536c598c86eaa06b9fbcddf55593178a2dea6`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 124.0 MB (124006958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5db59e0022877bdb072a79ab24a4d449fd847bdce6cbb5c029644d19ca12219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c23cac791cbbd3f4051ceb70b23fade9cf32f0c6f57fccae572356ec94b63f`

```dockerfile
```

-	Layers:
	-	`sha256:b6a30ffaf392f55ce48e1dd5d51f254e70efaea64ff92c8f0fb5ebd5b53b9414`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f77a18924df862c1ee6ae480e3b26f59104cba1346694c374c8d7efd284391a`  
		Last Modified: Wed, 10 Apr 2024 16:52:44 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:8f01f7bb053e5564eb84a3f1824e4ca2202d29dd415d196cf8e27c8f7e6b611e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:0cd023a61a7db68382fa6f1487a2dc1fc3affc104f14065668377a85d3ba4065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300375577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c23c35dfe5d5ec73cb5f1c972000bbea3c24b39e742d5114d38c6d7e63c60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e33d951618549541cc068ed17683ff2a3f0b7cbefea016f222096d9cb22b0`  
		Last Modified: Wed, 10 Apr 2024 02:54:58 GMT  
		Size: 144.9 MB (144893016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1c3182522949778e5775b24fd74db5bc3c6cd2438e249f07221a9bdbb32c5`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631513be69398c8e1a0bdcbf7f8f4825d8d6ad957edb79a26a17affdc4be8489`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d27ab0005a260d857e1c197b6aa1fd50c2747093dd83f48cb4ecd8b7b5080`  
		Last Modified: Wed, 10 Apr 2024 02:54:57 GMT  
		Size: 124.0 MB (124041409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:6eda6f886e066d809f6d2867b361c4549af878d178cbab1b51b1ac7a6f21242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad817d89123afe185e097c6bcbfbe211166906f5537259911e35a2736ccdc9e2`

```dockerfile
```

-	Layers:
	-	`sha256:2366739bae468fca36e28b7f4fa1f1776b74b169cdbd2cb2780e614f8dacabea`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd516509b7fd549ae344d8509ec9caae568039fc8cc706fc685c6445d7328ecc`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ec690a8774668fb32f2625f94bd4b4f08503e8a5d8a8bd9cb6d4be8a837648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297817119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ec57403fc86eb4c39f8e291f1e186f4a67941b1fac02bea42bad3ca9debdfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b5186423c9272e3df067a07d722326f5e0024bd939d2174a951618e2198d34`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a87ea67ac4b21223193e74488d97a23f3a2c6927edcc799fce5bd2b2e39c441`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33436c4395f3381e3f6dcbcf996536c598c86eaa06b9fbcddf55593178a2dea6`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 124.0 MB (124006958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:5db59e0022877bdb072a79ab24a4d449fd847bdce6cbb5c029644d19ca12219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c23cac791cbbd3f4051ceb70b23fade9cf32f0c6f57fccae572356ec94b63f`

```dockerfile
```

-	Layers:
	-	`sha256:b6a30ffaf392f55ce48e1dd5d51f254e70efaea64ff92c8f0fb5ebd5b53b9414`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f77a18924df862c1ee6ae480e3b26f59104cba1346694c374c8d7efd284391a`  
		Last Modified: Wed, 10 Apr 2024 16:52:44 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:8f01f7bb053e5564eb84a3f1824e4ca2202d29dd415d196cf8e27c8f7e6b611e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:0cd023a61a7db68382fa6f1487a2dc1fc3affc104f14065668377a85d3ba4065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300375577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c23c35dfe5d5ec73cb5f1c972000bbea3c24b39e742d5114d38c6d7e63c60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e33d951618549541cc068ed17683ff2a3f0b7cbefea016f222096d9cb22b0`  
		Last Modified: Wed, 10 Apr 2024 02:54:58 GMT  
		Size: 144.9 MB (144893016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1c3182522949778e5775b24fd74db5bc3c6cd2438e249f07221a9bdbb32c5`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631513be69398c8e1a0bdcbf7f8f4825d8d6ad957edb79a26a17affdc4be8489`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d27ab0005a260d857e1c197b6aa1fd50c2747093dd83f48cb4ecd8b7b5080`  
		Last Modified: Wed, 10 Apr 2024 02:54:57 GMT  
		Size: 124.0 MB (124041409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:6eda6f886e066d809f6d2867b361c4549af878d178cbab1b51b1ac7a6f21242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad817d89123afe185e097c6bcbfbe211166906f5537259911e35a2736ccdc9e2`

```dockerfile
```

-	Layers:
	-	`sha256:2366739bae468fca36e28b7f4fa1f1776b74b169cdbd2cb2780e614f8dacabea`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd516509b7fd549ae344d8509ec9caae568039fc8cc706fc685c6445d7328ecc`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ec690a8774668fb32f2625f94bd4b4f08503e8a5d8a8bd9cb6d4be8a837648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297817119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ec57403fc86eb4c39f8e291f1e186f4a67941b1fac02bea42bad3ca9debdfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b5186423c9272e3df067a07d722326f5e0024bd939d2174a951618e2198d34`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a87ea67ac4b21223193e74488d97a23f3a2c6927edcc799fce5bd2b2e39c441`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33436c4395f3381e3f6dcbcf996536c598c86eaa06b9fbcddf55593178a2dea6`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 124.0 MB (124006958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:5db59e0022877bdb072a79ab24a4d449fd847bdce6cbb5c029644d19ca12219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c23cac791cbbd3f4051ceb70b23fade9cf32f0c6f57fccae572356ec94b63f`

```dockerfile
```

-	Layers:
	-	`sha256:b6a30ffaf392f55ce48e1dd5d51f254e70efaea64ff92c8f0fb5ebd5b53b9414`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f77a18924df862c1ee6ae480e3b26f59104cba1346694c374c8d7efd284391a`  
		Last Modified: Wed, 10 Apr 2024 16:52:44 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:745cfda6713a7fa14f763d0730f464fd5b16afaccf5328ff9b4c5785c87b5f37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:7892fadf588136b4995e2dadb3258bb4036bcbcd6379137f921e88932f349f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557177856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46da598369fb6e4773cdfb331b7bf71c2c92e4201c7e4716e38ee1194db98ada`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a00cc2b21f5ecd3de405268bf01e364c9695aed0737469fdec7d8598e24369`  
		Last Modified: Wed, 10 Apr 2024 02:54:48 GMT  
		Size: 144.9 MB (144893017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662af1be01460b8b6a12b6d6dd173ee13703a93763e37d44e8468ff5afbb72b6`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3ce273d4caa4113bffd2595fffe729336220ef0d49c290805cf33947af05e3`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838446ef71babdb652a97f2127783fa27993fbd3be0fa25e0ce234bcad36c8e`  
		Last Modified: Wed, 10 Apr 2024 02:54:52 GMT  
		Size: 380.8 MB (380843689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ea539a331c4295ad1c1934aa89a9a9ab422805da05507c569729929af559beed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e4b72d6ca7896894cf2915e3d9dbb1650fe03e201f5422649a504d25e8276f`

```dockerfile
```

-	Layers:
	-	`sha256:8153b48968317229e8e8cfa6cc1a8a005958c7730cbbcd2557d20dfba4854104`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7277080f0f69b3888a88bf5408b7ff210339d4af40033b70d9ffb81f44eecd71`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b1f253281cf41373367f814b7c8f9a68b87e35b973fb679d40dc53adefea8b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554618001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adb26df3f32ff6f1c870da02c7e6548b897694cfa6c7fe0af186b278cf303e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee51cb7d7a462689dab9be72845d2a86126e29d8b25e913ad83b8b38534e6a9`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc455094a2a3133f7906a1fa449efeb8c0f342563708fd0b43aa816251a4892d`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ef254a7b2994d44045b0a7479d1361f9f6c33c0d89374bed4b3edc60e6ecd4`  
		Last Modified: Wed, 10 Apr 2024 16:54:09 GMT  
		Size: 380.8 MB (380807841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:055a1e3c950bd52adccc2b6164b8f2967a59f8454e559163b82f6e72568d45a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc983ae56550c8ecd29e41b8d439890a43a58ed0d53d93270aa28e3b849dae48`

```dockerfile
```

-	Layers:
	-	`sha256:5d53089e355997c348cab74154b9cdda684635735dd9d556e55b64b729d085ca`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35309ba1616779ead45454e1a104337f7dac847ea46b0f7c23f42899d972095d`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:745cfda6713a7fa14f763d0730f464fd5b16afaccf5328ff9b4c5785c87b5f37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:7892fadf588136b4995e2dadb3258bb4036bcbcd6379137f921e88932f349f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557177856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46da598369fb6e4773cdfb331b7bf71c2c92e4201c7e4716e38ee1194db98ada`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a00cc2b21f5ecd3de405268bf01e364c9695aed0737469fdec7d8598e24369`  
		Last Modified: Wed, 10 Apr 2024 02:54:48 GMT  
		Size: 144.9 MB (144893017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662af1be01460b8b6a12b6d6dd173ee13703a93763e37d44e8468ff5afbb72b6`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3ce273d4caa4113bffd2595fffe729336220ef0d49c290805cf33947af05e3`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838446ef71babdb652a97f2127783fa27993fbd3be0fa25e0ce234bcad36c8e`  
		Last Modified: Wed, 10 Apr 2024 02:54:52 GMT  
		Size: 380.8 MB (380843689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ea539a331c4295ad1c1934aa89a9a9ab422805da05507c569729929af559beed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e4b72d6ca7896894cf2915e3d9dbb1650fe03e201f5422649a504d25e8276f`

```dockerfile
```

-	Layers:
	-	`sha256:8153b48968317229e8e8cfa6cc1a8a005958c7730cbbcd2557d20dfba4854104`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7277080f0f69b3888a88bf5408b7ff210339d4af40033b70d9ffb81f44eecd71`  
		Last Modified: Wed, 10 Apr 2024 02:54:45 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b1f253281cf41373367f814b7c8f9a68b87e35b973fb679d40dc53adefea8b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554618001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28adb26df3f32ff6f1c870da02c7e6548b897694cfa6c7fe0af186b278cf303e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee51cb7d7a462689dab9be72845d2a86126e29d8b25e913ad83b8b38534e6a9`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc455094a2a3133f7906a1fa449efeb8c0f342563708fd0b43aa816251a4892d`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ef254a7b2994d44045b0a7479d1361f9f6c33c0d89374bed4b3edc60e6ecd4`  
		Last Modified: Wed, 10 Apr 2024 16:54:09 GMT  
		Size: 380.8 MB (380807841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:055a1e3c950bd52adccc2b6164b8f2967a59f8454e559163b82f6e72568d45a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc983ae56550c8ecd29e41b8d439890a43a58ed0d53d93270aa28e3b849dae48`

```dockerfile
```

-	Layers:
	-	`sha256:5d53089e355997c348cab74154b9cdda684635735dd9d556e55b64b729d085ca`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35309ba1616779ead45454e1a104337f7dac847ea46b0f7c23f42899d972095d`  
		Last Modified: Wed, 10 Apr 2024 16:53:59 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:028d39afde25cffc412bd4d2215250643b8f78994d999d8ca44b2b6bca1e0116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:bdc85e7d4dda1d59301314fb7411398a4d8d9c76c09bfc2f31790024f20d1b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20263cfa9aaae7114b8a5e314d98325104d8c1b9f969dfcb22ec79b6fac1fde4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeaf0187031d5e65bed357c6a79752d9e5def9ee9c53c3be6c6c3a042bc5db`  
		Last Modified: Mon, 18 Mar 2024 18:37:37 GMT  
		Size: 163.6 MB (163561416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b5d48fa2aecee03dafb6be8f4133326c101ef017d6b353f7c61000ffd00fcf`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426c1d7f95efe077824e87e2534eae9acaf2a719a279c696e8feccf83a1a3fac`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 377.9 MB (377910398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:704bd376a838562ab1f9ed5ec7288f06e2bab7f4425d34e2508f0e2d5cb31487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be44e245386a0a32d7fa3e3a5026e0b3a94e589aa051c76dd77ed75c9f9390d`

```dockerfile
```

-	Layers:
	-	`sha256:aad12e01053fbf9b990734de91969d5905dd48ea47c992855ad91b536d266eeb`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e6f109446db0aba96c1b07f80229504fce79d3e7fb0c35bd61fc27424f6d4a`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:328f1909789e22d0fed607229291370642425be5d1e83b8911a10b5d8adfc6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7dce4ba3e76d332624612779eed331747d02149a43e087c72f82aca41dd3bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9296980305731d7ce62d092c2576cd341a35385e56a58fd11d67b12b96b3caa`  
		Last Modified: Mon, 18 Mar 2024 20:13:13 GMT  
		Size: 377.9 MB (377910224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:77985fbc6e6f95bdc5a6dab6a9125d77e138ba17262492f854ae69d6824dbe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97767c981b1268424128c71497280ecb5108d633eb059da5206e4d9471ff6a2`

```dockerfile
```

-	Layers:
	-	`sha256:bd439036cf03f79f376ff66cccc71f5ab7ac8038ddf54945fba09eb2e8e4979f`  
		Last Modified: Mon, 18 Mar 2024 20:12:55 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec919468a70abc4da3f758702c2efad7ebdacb31bc73b1e41407dd93b86bf9c`  
		Last Modified: Mon, 18 Mar 2024 20:12:54 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:84c02c864777ed97a8431e3b9b4406a7f49966ccd8fc86fd6db76115c01e05b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:dc763c74655873adb0691329c58edfc7552a02bbff786b085ce9d5d66e9918b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27239bba9891c68d24b03b42cd9d2b85801384d7a2dc293543227fa7de783be`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a24476c4520b1e9c9c66d29c1916e9e62c5a75316e29ce3fc9fff11b59a152`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 257.0 MB (257005824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba5a03dc0af0cc8ce429c45c6639db251f0567674616f890010b13763bc4ed6`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267d38eaffbe637912c68444a66b1b720b609ff2c3877135c3db5abd3d0797d`  
		Last Modified: Mon, 18 Mar 2024 18:37:48 GMT  
		Size: 377.9 MB (377910325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:36c457c46727f8ebd718971ffcb9de0304cb9a2e9cf0b51ef835dab7d6ab5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca751d616a406313aad5d5bd4fe7b36bdea60a843af03a2ff29f8e8758f369`

```dockerfile
```

-	Layers:
	-	`sha256:b51c8a0bdf7d22f2b4d2de07406b6a825c1e5a91801de492f35ef31d6a49c0e0`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb72743887e25635a510673c39ec83b5ae9120532fbdaa247017ce2d4e86544c`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:486cdbb0fd895d792b1567b6f2a7d8d2f0df705a0d5c42e523c4b7454fa144ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663463358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71973171c1f949830ac2f9e3c0c32edb51256f100017d5cabb477aff0877c081`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c609b766a135e00a9ded0424884aa346927f42d3db21d2f80d5dda20599bca5`  
		Last Modified: Mon, 18 Mar 2024 19:58:41 GMT  
		Size: 377.9 MB (377910423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e531c0248bccb0822ada97cfd969348dee3a50f9e4b74ec0733fca4e95642009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ab395c80e808d14fb3aae0e1d2a6183466a98b44958df3061f13375cfbba85`

```dockerfile
```

-	Layers:
	-	`sha256:7954b29e2052c6a0e0dfc227614f61aa18e39ca8069ba1657527e4a934de63cc`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d49e13727dc2f6e004439b75b5a58c304c8e36de7be9a0d3e47d6e7729dff82`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 19.8 KB (19785 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:8f01f7bb053e5564eb84a3f1824e4ca2202d29dd415d196cf8e27c8f7e6b611e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:0cd023a61a7db68382fa6f1487a2dc1fc3affc104f14065668377a85d3ba4065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300375577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec9c23c35dfe5d5ec73cb5f1c972000bbea3c24b39e742d5114d38c6d7e63c60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e33d951618549541cc068ed17683ff2a3f0b7cbefea016f222096d9cb22b0`  
		Last Modified: Wed, 10 Apr 2024 02:54:58 GMT  
		Size: 144.9 MB (144893016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1c3182522949778e5775b24fd74db5bc3c6cd2438e249f07221a9bdbb32c5`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631513be69398c8e1a0bdcbf7f8f4825d8d6ad957edb79a26a17affdc4be8489`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580d27ab0005a260d857e1c197b6aa1fd50c2747093dd83f48cb4ecd8b7b5080`  
		Last Modified: Wed, 10 Apr 2024 02:54:57 GMT  
		Size: 124.0 MB (124041409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:6eda6f886e066d809f6d2867b361c4549af878d178cbab1b51b1ac7a6f21242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad817d89123afe185e097c6bcbfbe211166906f5537259911e35a2736ccdc9e2`

```dockerfile
```

-	Layers:
	-	`sha256:2366739bae468fca36e28b7f4fa1f1776b74b169cdbd2cb2780e614f8dacabea`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd516509b7fd549ae344d8509ec9caae568039fc8cc706fc685c6445d7328ecc`  
		Last Modified: Wed, 10 Apr 2024 02:54:55 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ec690a8774668fb32f2625f94bd4b4f08503e8a5d8a8bd9cb6d4be8a837648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297817119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ec57403fc86eb4c39f8e291f1e186f4a67941b1fac02bea42bad3ca9debdfa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 18 Mar 2024 11:02:14 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37eef3a9dbe3fa76c06bfc7157f87cec3852800f95a9628866ef1a0ea069142`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 143.7 MB (143720418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b5186423c9272e3df067a07d722326f5e0024bd939d2174a951618e2198d34`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a87ea67ac4b21223193e74488d97a23f3a2c6927edcc799fce5bd2b2e39c441`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33436c4395f3381e3f6dcbcf996536c598c86eaa06b9fbcddf55593178a2dea6`  
		Last Modified: Wed, 10 Apr 2024 16:52:47 GMT  
		Size: 124.0 MB (124006958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:5db59e0022877bdb072a79ab24a4d449fd847bdce6cbb5c029644d19ca12219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c23cac791cbbd3f4051ceb70b23fade9cf32f0c6f57fccae572356ec94b63f`

```dockerfile
```

-	Layers:
	-	`sha256:b6a30ffaf392f55ce48e1dd5d51f254e70efaea64ff92c8f0fb5ebd5b53b9414`  
		Last Modified: Wed, 10 Apr 2024 16:52:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f77a18924df862c1ee6ae480e3b26f59104cba1346694c374c8d7efd284391a`  
		Last Modified: Wed, 10 Apr 2024 16:52:44 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json
