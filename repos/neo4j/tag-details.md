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
$ docker pull neo4j@sha256:907b2d8ad6c584185898d23102f0fe14c41d1b54d7349e4916cfc5be6ba1820c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:d47293f94734215cac31e96d513ad671c7d6481613b68d8e80ab3493f1640243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297731194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaa37cbb545db1f98cb63da1ceb71108c844103249a9a8024c16c866f52fc9d`
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
	-	`sha256:54f3125b7a9f2b84043a3502d512c11472aa46b0526748c0a48c093622ecfcf3`  
		Last Modified: Tue, 16 Apr 2024 05:57:19 GMT  
		Size: 145.3 MB (145271258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bb4bfdf7b715a259bf9d6ef4d7bce65c8f57f08120ededc7cb2bf326425530`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df7ad2400c2d5e597cb269bed5a46df2f697df5c97fd2e1676f5d8618789351`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f26c914173a237646b9eee1661285182601cfadef93968b4771ba76cb27c6f8`  
		Last Modified: Tue, 16 Apr 2024 05:57:20 GMT  
		Size: 121.0 MB (121018884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:548628e552118c0cf2095c73375c7934db73399d5f0a71921215910201d55b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d14559d299223f271ef337134e88538494f388b9663f3ec29d525b67d01ffb`

```dockerfile
```

-	Layers:
	-	`sha256:790dee98e6c883ae306f037669bd86f3674da9e04dd9d7227ad1655fa88db32a`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 2.9 MB (2938593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0948dc47dcca5b6aba30f07fc9ade49dbb9d806bb5da612b0807b8904e72231`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e13294642c64bba9c6c799a6bc58e7195fc3630e6658d06fb27835dd7c9b4703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293077250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77272f7ef131c92cb6eeec2f69e32ea0dbcbacc44a94d4a7ce8cd61e905dc4f`
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
	-	`sha256:3f5130f5c3de89aa1e8b27370a52cbaa751894ec6de409a56da6663655ad3e75`  
		Last Modified: Tue, 16 Apr 2024 15:56:19 GMT  
		Size: 142.0 MB (142006521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4103af4fe48e2cab1f479da3239b1c35f81eb90c6943347bd125bee5b307a4`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7047cc1d7d34b6730792b9d48f4965967a96d746cc0a43be4a872743ab64b17d`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3672c02f48a46f2aa08dc303c34fd40372e28a92e40dd2251c52724334f8d`  
		Last Modified: Tue, 16 Apr 2024 15:56:18 GMT  
		Size: 121.0 MB (120981079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:f45d370282b8043461abdbd804f702f9623357c0071ab57eb7e6e0de6cb17702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6768a93134027154a448570366ab0a6cc30dd08d14a730f111522f82939dacba`

```dockerfile
```

-	Layers:
	-	`sha256:a6b2dc2922381576bb663a5fdca371d6e43d16a213451aa9a2f6d852e855a883`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 2.9 MB (2938813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4e41aa455ee0b0673ae01d406b17a47107ec12eb0ce3276dacade18d6be4a3`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 18.5 KB (18514 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:907b2d8ad6c584185898d23102f0fe14c41d1b54d7349e4916cfc5be6ba1820c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d47293f94734215cac31e96d513ad671c7d6481613b68d8e80ab3493f1640243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297731194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaa37cbb545db1f98cb63da1ceb71108c844103249a9a8024c16c866f52fc9d`
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
	-	`sha256:54f3125b7a9f2b84043a3502d512c11472aa46b0526748c0a48c093622ecfcf3`  
		Last Modified: Tue, 16 Apr 2024 05:57:19 GMT  
		Size: 145.3 MB (145271258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bb4bfdf7b715a259bf9d6ef4d7bce65c8f57f08120ededc7cb2bf326425530`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df7ad2400c2d5e597cb269bed5a46df2f697df5c97fd2e1676f5d8618789351`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f26c914173a237646b9eee1661285182601cfadef93968b4771ba76cb27c6f8`  
		Last Modified: Tue, 16 Apr 2024 05:57:20 GMT  
		Size: 121.0 MB (121018884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:548628e552118c0cf2095c73375c7934db73399d5f0a71921215910201d55b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d14559d299223f271ef337134e88538494f388b9663f3ec29d525b67d01ffb`

```dockerfile
```

-	Layers:
	-	`sha256:790dee98e6c883ae306f037669bd86f3674da9e04dd9d7227ad1655fa88db32a`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 2.9 MB (2938593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0948dc47dcca5b6aba30f07fc9ade49dbb9d806bb5da612b0807b8904e72231`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e13294642c64bba9c6c799a6bc58e7195fc3630e6658d06fb27835dd7c9b4703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293077250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77272f7ef131c92cb6eeec2f69e32ea0dbcbacc44a94d4a7ce8cd61e905dc4f`
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
	-	`sha256:3f5130f5c3de89aa1e8b27370a52cbaa751894ec6de409a56da6663655ad3e75`  
		Last Modified: Tue, 16 Apr 2024 15:56:19 GMT  
		Size: 142.0 MB (142006521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4103af4fe48e2cab1f479da3239b1c35f81eb90c6943347bd125bee5b307a4`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7047cc1d7d34b6730792b9d48f4965967a96d746cc0a43be4a872743ab64b17d`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3672c02f48a46f2aa08dc303c34fd40372e28a92e40dd2251c52724334f8d`  
		Last Modified: Tue, 16 Apr 2024 15:56:18 GMT  
		Size: 121.0 MB (120981079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:f45d370282b8043461abdbd804f702f9623357c0071ab57eb7e6e0de6cb17702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6768a93134027154a448570366ab0a6cc30dd08d14a730f111522f82939dacba`

```dockerfile
```

-	Layers:
	-	`sha256:a6b2dc2922381576bb663a5fdca371d6e43d16a213451aa9a2f6d852e855a883`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 2.9 MB (2938813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4e41aa455ee0b0673ae01d406b17a47107ec12eb0ce3276dacade18d6be4a3`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 18.5 KB (18514 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:4b510c681eaef8b38fa3446006139d6f1b389460b5fd13b5dcab07fe6fdac172
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d04d9bddee801312e01cb0660f0251f41444fbfedf7143ec85758083a029c1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 MB (401643347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8dbfb952d8820d6d08a921884fb1c64684a413919ef38fb56ece24cf463c5e8`
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
	-	`sha256:38ac339d81e7edcc93f21b112e12e7bcb22b776d9c9a92eacb3ee586d643295e`  
		Last Modified: Tue, 16 Apr 2024 05:57:37 GMT  
		Size: 145.3 MB (145271258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa06f6d67dbc76d1716fcb93044f0063c3e3d94a9744735e267f8fe62e9e326f`  
		Last Modified: Tue, 16 Apr 2024 05:57:34 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4d498b66d4bb1bb976cb5c44f3f052805adc13bfc15f3f5eba16a7d4c8347`  
		Last Modified: Tue, 16 Apr 2024 05:57:35 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb823d0d88809eac442e69d05b5ecac3721e764bf009671a9789d30863b6dbd3`  
		Last Modified: Tue, 16 Apr 2024 05:57:39 GMT  
		Size: 224.9 MB (224931037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3acebbea9c65f71122cffc81341764e24d3de083278860b5bcc414de29dc0b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f1ddfa5e90765afc63c313d3dd198d8a5d3f5eaea751b9dab46122984e69f2`

```dockerfile
```

-	Layers:
	-	`sha256:89741c0b5e571b4c02d78f85d82ebc7698d5fecefc328ee6660927681b10cb6a`  
		Last Modified: Tue, 16 Apr 2024 05:57:35 GMT  
		Size: 3.1 MB (3067486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c14d93c65a12fbfdd86380b1087759d1fb8bb53e56226e72f2677e9152384c4`  
		Last Modified: Tue, 16 Apr 2024 05:57:35 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cc5cb8b894e7b1c2b960aed85735479c8d466d893e057ca61e7548e92c07a87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.0 MB (396992611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bbfbce4677e33a5a1041d0318760074f02ae5304d0b803aea607108e53bb7f`
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
	-	`sha256:3f5130f5c3de89aa1e8b27370a52cbaa751894ec6de409a56da6663655ad3e75`  
		Last Modified: Tue, 16 Apr 2024 15:56:19 GMT  
		Size: 142.0 MB (142006521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492e2b43c1d5cd326b1c2dfa5ac3ec2f87d6e9c6373cd212cb3aac652ce5517`  
		Last Modified: Tue, 16 Apr 2024 15:57:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ea2d40a4c3be0842fa032cf4cb965528b147ffcc3ac6e0018cc6c5dc030a7c`  
		Last Modified: Tue, 16 Apr 2024 15:57:28 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a9a33b574ba44e087dedf0f99c5203ac1f87f2e456d8ff45d299eb56695195`  
		Last Modified: Tue, 16 Apr 2024 15:57:34 GMT  
		Size: 224.9 MB (224896444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e169cc52027fe55c6afbcfe9ce5e35ff3c0ad3ab0c4b629f3e4ecd44cd9fbc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e58598021e7c925e4e912bc693c4d3f023d948cf9be9dab61c0d0828922e45`

```dockerfile
```

-	Layers:
	-	`sha256:3eef62d908e96302281b7b92207ed9a5e53fd1f9187c19e08300476f889f94ef`  
		Last Modified: Tue, 16 Apr 2024 15:57:28 GMT  
		Size: 3.1 MB (3067702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36240b38dc2a1b46b5f1aa89d573d18307554133b056b6ec700cae1845d1713a`  
		Last Modified: Tue, 16 Apr 2024 15:57:28 GMT  
		Size: 17.9 KB (17942 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.32`

```console
$ docker pull neo4j@sha256:907b2d8ad6c584185898d23102f0fe14c41d1b54d7349e4916cfc5be6ba1820c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.32` - linux; amd64

```console
$ docker pull neo4j@sha256:d47293f94734215cac31e96d513ad671c7d6481613b68d8e80ab3493f1640243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297731194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaa37cbb545db1f98cb63da1ceb71108c844103249a9a8024c16c866f52fc9d`
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
	-	`sha256:54f3125b7a9f2b84043a3502d512c11472aa46b0526748c0a48c093622ecfcf3`  
		Last Modified: Tue, 16 Apr 2024 05:57:19 GMT  
		Size: 145.3 MB (145271258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bb4bfdf7b715a259bf9d6ef4d7bce65c8f57f08120ededc7cb2bf326425530`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df7ad2400c2d5e597cb269bed5a46df2f697df5c97fd2e1676f5d8618789351`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f26c914173a237646b9eee1661285182601cfadef93968b4771ba76cb27c6f8`  
		Last Modified: Tue, 16 Apr 2024 05:57:20 GMT  
		Size: 121.0 MB (121018884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32` - unknown; unknown

```console
$ docker pull neo4j@sha256:548628e552118c0cf2095c73375c7934db73399d5f0a71921215910201d55b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d14559d299223f271ef337134e88538494f388b9663f3ec29d525b67d01ffb`

```dockerfile
```

-	Layers:
	-	`sha256:790dee98e6c883ae306f037669bd86f3674da9e04dd9d7227ad1655fa88db32a`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 2.9 MB (2938593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0948dc47dcca5b6aba30f07fc9ade49dbb9d806bb5da612b0807b8904e72231`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.32` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e13294642c64bba9c6c799a6bc58e7195fc3630e6658d06fb27835dd7c9b4703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293077250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77272f7ef131c92cb6eeec2f69e32ea0dbcbacc44a94d4a7ce8cd61e905dc4f`
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
	-	`sha256:3f5130f5c3de89aa1e8b27370a52cbaa751894ec6de409a56da6663655ad3e75`  
		Last Modified: Tue, 16 Apr 2024 15:56:19 GMT  
		Size: 142.0 MB (142006521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4103af4fe48e2cab1f479da3239b1c35f81eb90c6943347bd125bee5b307a4`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7047cc1d7d34b6730792b9d48f4965967a96d746cc0a43be4a872743ab64b17d`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3672c02f48a46f2aa08dc303c34fd40372e28a92e40dd2251c52724334f8d`  
		Last Modified: Tue, 16 Apr 2024 15:56:18 GMT  
		Size: 121.0 MB (120981079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32` - unknown; unknown

```console
$ docker pull neo4j@sha256:f45d370282b8043461abdbd804f702f9623357c0071ab57eb7e6e0de6cb17702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6768a93134027154a448570366ab0a6cc30dd08d14a730f111522f82939dacba`

```dockerfile
```

-	Layers:
	-	`sha256:a6b2dc2922381576bb663a5fdca371d6e43d16a213451aa9a2f6d852e855a883`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 2.9 MB (2938813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4e41aa455ee0b0673ae01d406b17a47107ec12eb0ce3276dacade18d6be4a3`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 18.5 KB (18514 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.32-community`

```console
$ docker pull neo4j@sha256:907b2d8ad6c584185898d23102f0fe14c41d1b54d7349e4916cfc5be6ba1820c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.32-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d47293f94734215cac31e96d513ad671c7d6481613b68d8e80ab3493f1640243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297731194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaa37cbb545db1f98cb63da1ceb71108c844103249a9a8024c16c866f52fc9d`
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
	-	`sha256:54f3125b7a9f2b84043a3502d512c11472aa46b0526748c0a48c093622ecfcf3`  
		Last Modified: Tue, 16 Apr 2024 05:57:19 GMT  
		Size: 145.3 MB (145271258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40bb4bfdf7b715a259bf9d6ef4d7bce65c8f57f08120ededc7cb2bf326425530`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df7ad2400c2d5e597cb269bed5a46df2f697df5c97fd2e1676f5d8618789351`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f26c914173a237646b9eee1661285182601cfadef93968b4771ba76cb27c6f8`  
		Last Modified: Tue, 16 Apr 2024 05:57:20 GMT  
		Size: 121.0 MB (121018884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:548628e552118c0cf2095c73375c7934db73399d5f0a71921215910201d55b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d14559d299223f271ef337134e88538494f388b9663f3ec29d525b67d01ffb`

```dockerfile
```

-	Layers:
	-	`sha256:790dee98e6c883ae306f037669bd86f3674da9e04dd9d7227ad1655fa88db32a`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 2.9 MB (2938593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0948dc47dcca5b6aba30f07fc9ade49dbb9d806bb5da612b0807b8904e72231`  
		Last Modified: Tue, 16 Apr 2024 05:57:18 GMT  
		Size: 20.3 KB (20320 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.32-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e13294642c64bba9c6c799a6bc58e7195fc3630e6658d06fb27835dd7c9b4703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293077250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77272f7ef131c92cb6eeec2f69e32ea0dbcbacc44a94d4a7ce8cd61e905dc4f`
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
	-	`sha256:3f5130f5c3de89aa1e8b27370a52cbaa751894ec6de409a56da6663655ad3e75`  
		Last Modified: Tue, 16 Apr 2024 15:56:19 GMT  
		Size: 142.0 MB (142006521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4103af4fe48e2cab1f479da3239b1c35f81eb90c6943347bd125bee5b307a4`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7047cc1d7d34b6730792b9d48f4965967a96d746cc0a43be4a872743ab64b17d`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3672c02f48a46f2aa08dc303c34fd40372e28a92e40dd2251c52724334f8d`  
		Last Modified: Tue, 16 Apr 2024 15:56:18 GMT  
		Size: 121.0 MB (120981079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:f45d370282b8043461abdbd804f702f9623357c0071ab57eb7e6e0de6cb17702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6768a93134027154a448570366ab0a6cc30dd08d14a730f111522f82939dacba`

```dockerfile
```

-	Layers:
	-	`sha256:a6b2dc2922381576bb663a5fdca371d6e43d16a213451aa9a2f6d852e855a883`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 2.9 MB (2938813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4e41aa455ee0b0673ae01d406b17a47107ec12eb0ce3276dacade18d6be4a3`  
		Last Modified: Tue, 16 Apr 2024 15:56:15 GMT  
		Size: 18.5 KB (18514 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.32-enterprise`

```console
$ docker pull neo4j@sha256:4b510c681eaef8b38fa3446006139d6f1b389460b5fd13b5dcab07fe6fdac172
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.32-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:d04d9bddee801312e01cb0660f0251f41444fbfedf7143ec85758083a029c1f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 MB (401643347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8dbfb952d8820d6d08a921884fb1c64684a413919ef38fb56ece24cf463c5e8`
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
	-	`sha256:38ac339d81e7edcc93f21b112e12e7bcb22b776d9c9a92eacb3ee586d643295e`  
		Last Modified: Tue, 16 Apr 2024 05:57:37 GMT  
		Size: 145.3 MB (145271258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa06f6d67dbc76d1716fcb93044f0063c3e3d94a9744735e267f8fe62e9e326f`  
		Last Modified: Tue, 16 Apr 2024 05:57:34 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4d498b66d4bb1bb976cb5c44f3f052805adc13bfc15f3f5eba16a7d4c8347`  
		Last Modified: Tue, 16 Apr 2024 05:57:35 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb823d0d88809eac442e69d05b5ecac3721e764bf009671a9789d30863b6dbd3`  
		Last Modified: Tue, 16 Apr 2024 05:57:39 GMT  
		Size: 224.9 MB (224931037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3acebbea9c65f71122cffc81341764e24d3de083278860b5bcc414de29dc0b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f1ddfa5e90765afc63c313d3dd198d8a5d3f5eaea751b9dab46122984e69f2`

```dockerfile
```

-	Layers:
	-	`sha256:89741c0b5e571b4c02d78f85d82ebc7698d5fecefc328ee6660927681b10cb6a`  
		Last Modified: Tue, 16 Apr 2024 05:57:35 GMT  
		Size: 3.1 MB (3067486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c14d93c65a12fbfdd86380b1087759d1fb8bb53e56226e72f2677e9152384c4`  
		Last Modified: Tue, 16 Apr 2024 05:57:35 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.32-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cc5cb8b894e7b1c2b960aed85735479c8d466d893e057ca61e7548e92c07a87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.0 MB (396992611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bbfbce4677e33a5a1041d0318760074f02ae5304d0b803aea607108e53bb7f`
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
	-	`sha256:3f5130f5c3de89aa1e8b27370a52cbaa751894ec6de409a56da6663655ad3e75`  
		Last Modified: Tue, 16 Apr 2024 15:56:19 GMT  
		Size: 142.0 MB (142006521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492e2b43c1d5cd326b1c2dfa5ac3ec2f87d6e9c6373cd212cb3aac652ce5517`  
		Last Modified: Tue, 16 Apr 2024 15:57:28 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ea2d40a4c3be0842fa032cf4cb965528b147ffcc3ac6e0018cc6c5dc030a7c`  
		Last Modified: Tue, 16 Apr 2024 15:57:28 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a9a33b574ba44e087dedf0f99c5203ac1f87f2e456d8ff45d299eb56695195`  
		Last Modified: Tue, 16 Apr 2024 15:57:34 GMT  
		Size: 224.9 MB (224896444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.32-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e169cc52027fe55c6afbcfe9ce5e35ff3c0ad3ab0c4b629f3e4ecd44cd9fbc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e58598021e7c925e4e912bc693c4d3f023d948cf9be9dab61c0d0828922e45`

```dockerfile
```

-	Layers:
	-	`sha256:3eef62d908e96302281b7b92207ed9a5e53fd1f9187c19e08300476f889f94ef`  
		Last Modified: Tue, 16 Apr 2024 15:57:28 GMT  
		Size: 3.1 MB (3067702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36240b38dc2a1b46b5f1aa89d573d18307554133b056b6ec700cae1845d1713a`  
		Last Modified: Tue, 16 Apr 2024 15:57:28 GMT  
		Size: 17.9 KB (17942 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:6ff60303020e2096e531b9f51b3dd4214048f1a5ddb18567a432b4b915a699b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f149a16096b268dba8e37ed6e5d24fe7ac5c6983968fc0125c3fbb359618a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286420831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc3b6882253ce210505f75e486545939729b369eb5643d02191d30f97629eaf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4d548f72423b629fc299dd261f4722d402412e8b4fe61875ab8d63480ce46`  
		Last Modified: Mon, 15 Apr 2024 17:51:01 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1723d6bcbed903f837fd473590884bc58b375b65328ab1359931d92c64b182`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aff705976fd86083b61ee67758825c9bef2e45d006bab49f519579437fa65d`  
		Last Modified: Mon, 15 Apr 2024 17:50:58 GMT  
		Size: 122.8 MB (122826975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:65d53bd3ea916b64914691c4aeb5591f528c7aee6e809227a6e953db61d70c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27723c9613aea064ae328dee8559c26636b684c83b537ec17070f0bd044be331`

```dockerfile
```

-	Layers:
	-	`sha256:823b61534db2c0ed114afeb0c6c28f81e7f81514c9556fb6def3631e5ae348b5`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 5.4 MB (5417885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdb4df3706050afec01c3e6274d4cdb10abfd677e5ea961643ae9afefc41e09`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6368437fd3773a1050545de70c20bca7b013814bf8e36f7d55467c122a836840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284611216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702e579745fc2a928a87cd021296f4cdf936dfcf1129836e1e07a677b9df0c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6187c7fd1c1e727d5c371663cfb33e4c89e37e22e341428081690910bba081b`  
		Last Modified: Mon, 15 Apr 2024 19:09:15 GMT  
		Size: 122.8 MB (122827018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:6b3f019f726265bd69cc5651c1345829ad30a9766b73c6803bef06b30b2b63ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6d1d3b0b9316c7ee553eb668c978392e59125770c1b5438c65a0bdf0abaed1`

```dockerfile
```

-	Layers:
	-	`sha256:88cb64c2418306d7250b6cc02741291917bfd7f472fc80e1da16d0206268378a`  
		Last Modified: Mon, 15 Apr 2024 19:09:12 GMT  
		Size: 5.4 MB (5390869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448970127a68a3cc956ee123dba4233fad905999643583fa9b89e2418bd1c1df`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 21.7 KB (21680 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:4f291adffe0ec129df6caf0cc9be605c57c05085893a8b4589ff93ceaaa120d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8c1e19ad0b1e883111bb89141d19fecfc6e281bca8973c46251e430cab68840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560550562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ad53fda496550bb00b4817ba143f311ad16b871f7c01298a6b9ead22daf4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d045914fdd85147feef4c27332ccedc71c3625d48be84d4e1448030e7db861f`  
		Last Modified: Tue, 16 Apr 2024 05:57:33 GMT  
		Size: 144.9 MB (144893027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b34be4f734d57d2efbc55dc282f3c78576fce72c513b1b412af0216b522020`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193e685bc96219f8a854cc2a5d86e6e02b2333a740f268994faacd43a83331f`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe524bfd946cd8309231f1f5198be4d67ca9a0bea79dca975b8b63cef0e64355`  
		Last Modified: Tue, 16 Apr 2024 05:57:38 GMT  
		Size: 384.2 MB (384216386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:047686ec5f426106154399ec07a654b829585a378764fd93d365657bc691b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64159ef276bf73183baefc169377c967eab58197d2a43a6d26d4dd996cc2ddfd`

```dockerfile
```

-	Layers:
	-	`sha256:35b27975db30bd3b2a0355408fd1898403025317dbb84e598a0457a5616f6b84`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.1 MB (3126524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3dcd552532dcb80666569c6e18bd89683ee201efbbf3e706877ffd9703910`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8799880179071a8027ab15ad95033a286b30879174c455c292f8bf0973a31d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557992776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d011ea593ca5bde711d08805b50b2117adc3a3868cbc00d62fe875d33ff531e1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b683ac2451b67f0da52a6304839840ee13e6f54e9b1a63fd4853e2e17e9b86`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8144829e7b285c8018aa0453e0ccec7d5703a294919e1e8c3974941be1c8beb1`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70d1603b7a10dd3241687a08a21b9411285fcf2e42d313fe3814a96f41b50f8`  
		Last Modified: Tue, 16 Apr 2024 15:55:11 GMT  
		Size: 384.2 MB (384182650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:baf973a97e5a7ede6ed6ce9106629967231220f6adc03e918600da42134f1e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ce9b907cd05a6a237e87e598a73d903da33bda427927090dc654fadc8d4530`

```dockerfile
```

-	Layers:
	-	`sha256:b29993de27c66d7391d637f9d01da43c110d1fe91e54ebee49418c8eea56a536`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.1 MB (3126752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb18ec9846983c4e38dc062d0a6041cac3158c768c8167591bffb3b23a69cab`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4f291adffe0ec129df6caf0cc9be605c57c05085893a8b4589ff93ceaaa120d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8c1e19ad0b1e883111bb89141d19fecfc6e281bca8973c46251e430cab68840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560550562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ad53fda496550bb00b4817ba143f311ad16b871f7c01298a6b9ead22daf4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d045914fdd85147feef4c27332ccedc71c3625d48be84d4e1448030e7db861f`  
		Last Modified: Tue, 16 Apr 2024 05:57:33 GMT  
		Size: 144.9 MB (144893027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b34be4f734d57d2efbc55dc282f3c78576fce72c513b1b412af0216b522020`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193e685bc96219f8a854cc2a5d86e6e02b2333a740f268994faacd43a83331f`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe524bfd946cd8309231f1f5198be4d67ca9a0bea79dca975b8b63cef0e64355`  
		Last Modified: Tue, 16 Apr 2024 05:57:38 GMT  
		Size: 384.2 MB (384216386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:047686ec5f426106154399ec07a654b829585a378764fd93d365657bc691b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64159ef276bf73183baefc169377c967eab58197d2a43a6d26d4dd996cc2ddfd`

```dockerfile
```

-	Layers:
	-	`sha256:35b27975db30bd3b2a0355408fd1898403025317dbb84e598a0457a5616f6b84`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.1 MB (3126524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3dcd552532dcb80666569c6e18bd89683ee201efbbf3e706877ffd9703910`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8799880179071a8027ab15ad95033a286b30879174c455c292f8bf0973a31d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557992776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d011ea593ca5bde711d08805b50b2117adc3a3868cbc00d62fe875d33ff531e1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b683ac2451b67f0da52a6304839840ee13e6f54e9b1a63fd4853e2e17e9b86`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8144829e7b285c8018aa0453e0ccec7d5703a294919e1e8c3974941be1c8beb1`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70d1603b7a10dd3241687a08a21b9411285fcf2e42d313fe3814a96f41b50f8`  
		Last Modified: Tue, 16 Apr 2024 15:55:11 GMT  
		Size: 384.2 MB (384182650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:baf973a97e5a7ede6ed6ce9106629967231220f6adc03e918600da42134f1e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ce9b907cd05a6a237e87e598a73d903da33bda427927090dc654fadc8d4530`

```dockerfile
```

-	Layers:
	-	`sha256:b29993de27c66d7391d637f9d01da43c110d1fe91e54ebee49418c8eea56a536`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.1 MB (3126752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb18ec9846983c4e38dc062d0a6041cac3158c768c8167591bffb3b23a69cab`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4b46fa568dd07658aa91edb82a39cd6ab1da29594e85f0e64a7b6b34852cdb71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:89e66e370b953867865ec42529f549e6592bd6218dde1eb6b2d4b9e3a8fa8e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572789982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8741b07b1bd0088bf10a2a4d0b0dfd7b475bf61efd57b0426f836afda8c7dd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761328989f6454fc52ab4a6325c234c252505728a21baaf4fa876ccdf1a6286`  
		Last Modified: Mon, 15 Apr 2024 17:51:29 GMT  
		Size: 152.2 MB (152193909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca229d35f3a54ebb7e89ddc8aabb118af7271a43866409a70c90c848d2de7d4`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c6f275388aedb4cac2a7c6bac0015549e72a024a89d9b84a60dcd176905ef0`  
		Last Modified: Mon, 15 Apr 2024 17:51:34 GMT  
		Size: 381.3 MB (381283989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:49193bd409ec39194cdd4cb019da5aa44e6e4760e9a98253687ffaeeefc28245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fac76f47059c8b9555a247ddc0bc909f2d230031ef54c4d3897a458cfbb6b`

```dockerfile
```

-	Layers:
	-	`sha256:6f52a794f1410c61aad221842f37232750fce9db4900157073061108086a959d`  
		Last Modified: Mon, 15 Apr 2024 17:51:28 GMT  
		Size: 10.5 MB (10476665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6754a719bbbc73035667d9f73ef8a9854e85f89807d09e098d8779a08919b23`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb19dc31dcc014978d6df364433a477ff72aa14005a732d684a5435a02975369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569756380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c286a5b4dc9711136965c77cf1e54bd96b7726da0fcf41bfca3d7fd3466be21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cdc4ba88fa17faa117469b03cc7a82a8d4f6066b952764949edb2dfd272266`  
		Last Modified: Mon, 15 Apr 2024 20:18:30 GMT  
		Size: 381.3 MB (381284101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:f6d89a6dc4cb0617fc906b8507a2821d6bc944256f3ee4b12d3ccf96343acb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b2347fb030d4e4077a59bd469395607e522560486095e9cf9bcfdffe7fc0e5`

```dockerfile
```

-	Layers:
	-	`sha256:b557b2be4aa277741aecb0989e315a06fc1aa63e569a423b23513ef0e92ff682`  
		Last Modified: Mon, 15 Apr 2024 20:18:24 GMT  
		Size: 10.5 MB (10474203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95428b7beb425e0a9adc2f040a930e9ad237ab51eacceedf6454e3700c54ff49`  
		Last Modified: Mon, 15 Apr 2024 20:18:22 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9af1902ed24cc018c4e56563ef0e8920db365d30feaaf5fd00973a63fac77c44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fc6f5a67872c09b3e55b9a1f2b86b07318cc823a4169c55730b7f37366028d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.9 MB (544877316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db590246bc60971db355a306d691f31f6f791668f115cd64f5f930cb676296b7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfaeed02d926d856000abe4d8db10c1eb84530e4cf95177d739fca840844123`  
		Last Modified: Mon, 15 Apr 2024 17:51:14 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1c916a88f38f8fdfae4addc23aa1b1788a9d0499fb5ac36cbc24a87546527c`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ce8d0c209068dd3485e886fa5f7346cdaf0e320b6019a4dc79b8425ec575b5`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 381.3 MB (381283460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8ac0de2f84a62d87a8a1381efd3e060fcb6cc68dd436958ad1228b00bbf0e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c371570f6e09477f6baaf17e4df2d5ce796e3bbe59a6dcf3968bdbe365331f3`

```dockerfile
```

-	Layers:
	-	`sha256:cb65ba41f986cad2e3e579670622dcfe895b5b7ddba8190b219b2f6f75a9f0b5`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 5.6 MB (5587018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ff2ff8f9ac2445155647932d693945e0ef8266a01990ba8cd74f9c6d044557`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 20.5 KB (20484 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:637a8197ff99fa0f906f6c26256e9eb4c8de6ba5ccca019e539281754afc238f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.1 MB (543067694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02901e3022acd57191950a629b2ca5f90c3c66e497feca9dac1f7ec1bd256447`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae80cbe3ca198d4d11e7962fae14ee788722cb5a8ca5f903c72f87193ef956bc`  
		Last Modified: Mon, 15 Apr 2024 19:10:21 GMT  
		Size: 381.3 MB (381283496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e26dfdcee33177fcf234925e568baa937631fb46005a572606b34800e84042a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5580321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1506341da924059aeac7173abdf1023cf5629b771b6df5200571d1f1cbbde4d4`

```dockerfile
```

-	Layers:
	-	`sha256:8926afc3c6e0024c1a13aaf4563d391042c634e16f7b3d96d9fafb3af7eacb6c`  
		Last Modified: Mon, 15 Apr 2024 19:10:08 GMT  
		Size: 5.6 MB (5559994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48cd796aff86e8bbc276190abe5bb73daeddc61e99c43911d07fce103c94248`  
		Last Modified: Mon, 15 Apr 2024 19:10:08 GMT  
		Size: 20.3 KB (20327 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:6ff60303020e2096e531b9f51b3dd4214048f1a5ddb18567a432b4b915a699b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f149a16096b268dba8e37ed6e5d24fe7ac5c6983968fc0125c3fbb359618a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286420831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc3b6882253ce210505f75e486545939729b369eb5643d02191d30f97629eaf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4d548f72423b629fc299dd261f4722d402412e8b4fe61875ab8d63480ce46`  
		Last Modified: Mon, 15 Apr 2024 17:51:01 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1723d6bcbed903f837fd473590884bc58b375b65328ab1359931d92c64b182`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aff705976fd86083b61ee67758825c9bef2e45d006bab49f519579437fa65d`  
		Last Modified: Mon, 15 Apr 2024 17:50:58 GMT  
		Size: 122.8 MB (122826975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:65d53bd3ea916b64914691c4aeb5591f528c7aee6e809227a6e953db61d70c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27723c9613aea064ae328dee8559c26636b684c83b537ec17070f0bd044be331`

```dockerfile
```

-	Layers:
	-	`sha256:823b61534db2c0ed114afeb0c6c28f81e7f81514c9556fb6def3631e5ae348b5`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 5.4 MB (5417885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdb4df3706050afec01c3e6274d4cdb10abfd677e5ea961643ae9afefc41e09`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6368437fd3773a1050545de70c20bca7b013814bf8e36f7d55467c122a836840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284611216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702e579745fc2a928a87cd021296f4cdf936dfcf1129836e1e07a677b9df0c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6187c7fd1c1e727d5c371663cfb33e4c89e37e22e341428081690910bba081b`  
		Last Modified: Mon, 15 Apr 2024 19:09:15 GMT  
		Size: 122.8 MB (122827018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:6b3f019f726265bd69cc5651c1345829ad30a9766b73c6803bef06b30b2b63ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6d1d3b0b9316c7ee553eb668c978392e59125770c1b5438c65a0bdf0abaed1`

```dockerfile
```

-	Layers:
	-	`sha256:88cb64c2418306d7250b6cc02741291917bfd7f472fc80e1da16d0206268378a`  
		Last Modified: Mon, 15 Apr 2024 19:09:12 GMT  
		Size: 5.4 MB (5390869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448970127a68a3cc956ee123dba4233fad905999643583fa9b89e2418bd1c1df`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 21.7 KB (21680 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-bullseye`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-community`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-community-bullseye`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-community-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-community-ubi9`

```console
$ docker pull neo4j@sha256:6ff60303020e2096e531b9f51b3dd4214048f1a5ddb18567a432b4b915a699b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f149a16096b268dba8e37ed6e5d24fe7ac5c6983968fc0125c3fbb359618a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286420831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc3b6882253ce210505f75e486545939729b369eb5643d02191d30f97629eaf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4d548f72423b629fc299dd261f4722d402412e8b4fe61875ab8d63480ce46`  
		Last Modified: Mon, 15 Apr 2024 17:51:01 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1723d6bcbed903f837fd473590884bc58b375b65328ab1359931d92c64b182`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aff705976fd86083b61ee67758825c9bef2e45d006bab49f519579437fa65d`  
		Last Modified: Mon, 15 Apr 2024 17:50:58 GMT  
		Size: 122.8 MB (122826975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:65d53bd3ea916b64914691c4aeb5591f528c7aee6e809227a6e953db61d70c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27723c9613aea064ae328dee8559c26636b684c83b537ec17070f0bd044be331`

```dockerfile
```

-	Layers:
	-	`sha256:823b61534db2c0ed114afeb0c6c28f81e7f81514c9556fb6def3631e5ae348b5`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 5.4 MB (5417885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdb4df3706050afec01c3e6274d4cdb10abfd677e5ea961643ae9afefc41e09`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6368437fd3773a1050545de70c20bca7b013814bf8e36f7d55467c122a836840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284611216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702e579745fc2a928a87cd021296f4cdf936dfcf1129836e1e07a677b9df0c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6187c7fd1c1e727d5c371663cfb33e4c89e37e22e341428081690910bba081b`  
		Last Modified: Mon, 15 Apr 2024 19:09:15 GMT  
		Size: 122.8 MB (122827018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:6b3f019f726265bd69cc5651c1345829ad30a9766b73c6803bef06b30b2b63ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6d1d3b0b9316c7ee553eb668c978392e59125770c1b5438c65a0bdf0abaed1`

```dockerfile
```

-	Layers:
	-	`sha256:88cb64c2418306d7250b6cc02741291917bfd7f472fc80e1da16d0206268378a`  
		Last Modified: Mon, 15 Apr 2024 19:09:12 GMT  
		Size: 5.4 MB (5390869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448970127a68a3cc956ee123dba4233fad905999643583fa9b89e2418bd1c1df`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 21.7 KB (21680 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-enterprise`

```console
$ docker pull neo4j@sha256:4f291adffe0ec129df6caf0cc9be605c57c05085893a8b4589ff93ceaaa120d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8c1e19ad0b1e883111bb89141d19fecfc6e281bca8973c46251e430cab68840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560550562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ad53fda496550bb00b4817ba143f311ad16b871f7c01298a6b9ead22daf4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d045914fdd85147feef4c27332ccedc71c3625d48be84d4e1448030e7db861f`  
		Last Modified: Tue, 16 Apr 2024 05:57:33 GMT  
		Size: 144.9 MB (144893027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b34be4f734d57d2efbc55dc282f3c78576fce72c513b1b412af0216b522020`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193e685bc96219f8a854cc2a5d86e6e02b2333a740f268994faacd43a83331f`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe524bfd946cd8309231f1f5198be4d67ca9a0bea79dca975b8b63cef0e64355`  
		Last Modified: Tue, 16 Apr 2024 05:57:38 GMT  
		Size: 384.2 MB (384216386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:047686ec5f426106154399ec07a654b829585a378764fd93d365657bc691b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64159ef276bf73183baefc169377c967eab58197d2a43a6d26d4dd996cc2ddfd`

```dockerfile
```

-	Layers:
	-	`sha256:35b27975db30bd3b2a0355408fd1898403025317dbb84e598a0457a5616f6b84`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.1 MB (3126524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3dcd552532dcb80666569c6e18bd89683ee201efbbf3e706877ffd9703910`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8799880179071a8027ab15ad95033a286b30879174c455c292f8bf0973a31d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557992776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d011ea593ca5bde711d08805b50b2117adc3a3868cbc00d62fe875d33ff531e1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b683ac2451b67f0da52a6304839840ee13e6f54e9b1a63fd4853e2e17e9b86`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8144829e7b285c8018aa0453e0ccec7d5703a294919e1e8c3974941be1c8beb1`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70d1603b7a10dd3241687a08a21b9411285fcf2e42d313fe3814a96f41b50f8`  
		Last Modified: Tue, 16 Apr 2024 15:55:11 GMT  
		Size: 384.2 MB (384182650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:baf973a97e5a7ede6ed6ce9106629967231220f6adc03e918600da42134f1e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ce9b907cd05a6a237e87e598a73d903da33bda427927090dc654fadc8d4530`

```dockerfile
```

-	Layers:
	-	`sha256:b29993de27c66d7391d637f9d01da43c110d1fe91e54ebee49418c8eea56a536`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.1 MB (3126752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb18ec9846983c4e38dc062d0a6041cac3158c768c8167591bffb3b23a69cab`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4f291adffe0ec129df6caf0cc9be605c57c05085893a8b4589ff93ceaaa120d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8c1e19ad0b1e883111bb89141d19fecfc6e281bca8973c46251e430cab68840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560550562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ad53fda496550bb00b4817ba143f311ad16b871f7c01298a6b9ead22daf4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d045914fdd85147feef4c27332ccedc71c3625d48be84d4e1448030e7db861f`  
		Last Modified: Tue, 16 Apr 2024 05:57:33 GMT  
		Size: 144.9 MB (144893027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b34be4f734d57d2efbc55dc282f3c78576fce72c513b1b412af0216b522020`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193e685bc96219f8a854cc2a5d86e6e02b2333a740f268994faacd43a83331f`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe524bfd946cd8309231f1f5198be4d67ca9a0bea79dca975b8b63cef0e64355`  
		Last Modified: Tue, 16 Apr 2024 05:57:38 GMT  
		Size: 384.2 MB (384216386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:047686ec5f426106154399ec07a654b829585a378764fd93d365657bc691b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64159ef276bf73183baefc169377c967eab58197d2a43a6d26d4dd996cc2ddfd`

```dockerfile
```

-	Layers:
	-	`sha256:35b27975db30bd3b2a0355408fd1898403025317dbb84e598a0457a5616f6b84`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.1 MB (3126524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3dcd552532dcb80666569c6e18bd89683ee201efbbf3e706877ffd9703910`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8799880179071a8027ab15ad95033a286b30879174c455c292f8bf0973a31d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557992776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d011ea593ca5bde711d08805b50b2117adc3a3868cbc00d62fe875d33ff531e1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b683ac2451b67f0da52a6304839840ee13e6f54e9b1a63fd4853e2e17e9b86`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8144829e7b285c8018aa0453e0ccec7d5703a294919e1e8c3974941be1c8beb1`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70d1603b7a10dd3241687a08a21b9411285fcf2e42d313fe3814a96f41b50f8`  
		Last Modified: Tue, 16 Apr 2024 15:55:11 GMT  
		Size: 384.2 MB (384182650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:baf973a97e5a7ede6ed6ce9106629967231220f6adc03e918600da42134f1e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ce9b907cd05a6a237e87e598a73d903da33bda427927090dc654fadc8d4530`

```dockerfile
```

-	Layers:
	-	`sha256:b29993de27c66d7391d637f9d01da43c110d1fe91e54ebee49418c8eea56a536`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.1 MB (3126752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb18ec9846983c4e38dc062d0a6041cac3158c768c8167591bffb3b23a69cab`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4b46fa568dd07658aa91edb82a39cd6ab1da29594e85f0e64a7b6b34852cdb71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:89e66e370b953867865ec42529f549e6592bd6218dde1eb6b2d4b9e3a8fa8e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572789982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8741b07b1bd0088bf10a2a4d0b0dfd7b475bf61efd57b0426f836afda8c7dd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761328989f6454fc52ab4a6325c234c252505728a21baaf4fa876ccdf1a6286`  
		Last Modified: Mon, 15 Apr 2024 17:51:29 GMT  
		Size: 152.2 MB (152193909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca229d35f3a54ebb7e89ddc8aabb118af7271a43866409a70c90c848d2de7d4`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c6f275388aedb4cac2a7c6bac0015549e72a024a89d9b84a60dcd176905ef0`  
		Last Modified: Mon, 15 Apr 2024 17:51:34 GMT  
		Size: 381.3 MB (381283989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:49193bd409ec39194cdd4cb019da5aa44e6e4760e9a98253687ffaeeefc28245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fac76f47059c8b9555a247ddc0bc909f2d230031ef54c4d3897a458cfbb6b`

```dockerfile
```

-	Layers:
	-	`sha256:6f52a794f1410c61aad221842f37232750fce9db4900157073061108086a959d`  
		Last Modified: Mon, 15 Apr 2024 17:51:28 GMT  
		Size: 10.5 MB (10476665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6754a719bbbc73035667d9f73ef8a9854e85f89807d09e098d8779a08919b23`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb19dc31dcc014978d6df364433a477ff72aa14005a732d684a5435a02975369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569756380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c286a5b4dc9711136965c77cf1e54bd96b7726da0fcf41bfca3d7fd3466be21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cdc4ba88fa17faa117469b03cc7a82a8d4f6066b952764949edb2dfd272266`  
		Last Modified: Mon, 15 Apr 2024 20:18:30 GMT  
		Size: 381.3 MB (381284101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:f6d89a6dc4cb0617fc906b8507a2821d6bc944256f3ee4b12d3ccf96343acb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b2347fb030d4e4077a59bd469395607e522560486095e9cf9bcfdffe7fc0e5`

```dockerfile
```

-	Layers:
	-	`sha256:b557b2be4aa277741aecb0989e315a06fc1aa63e569a423b23513ef0e92ff682`  
		Last Modified: Mon, 15 Apr 2024 20:18:24 GMT  
		Size: 10.5 MB (10474203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95428b7beb425e0a9adc2f040a930e9ad237ab51eacceedf6454e3700c54ff49`  
		Last Modified: Mon, 15 Apr 2024 20:18:22 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9af1902ed24cc018c4e56563ef0e8920db365d30feaaf5fd00973a63fac77c44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fc6f5a67872c09b3e55b9a1f2b86b07318cc823a4169c55730b7f37366028d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.9 MB (544877316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db590246bc60971db355a306d691f31f6f791668f115cd64f5f930cb676296b7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfaeed02d926d856000abe4d8db10c1eb84530e4cf95177d739fca840844123`  
		Last Modified: Mon, 15 Apr 2024 17:51:14 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1c916a88f38f8fdfae4addc23aa1b1788a9d0499fb5ac36cbc24a87546527c`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ce8d0c209068dd3485e886fa5f7346cdaf0e320b6019a4dc79b8425ec575b5`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 381.3 MB (381283460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8ac0de2f84a62d87a8a1381efd3e060fcb6cc68dd436958ad1228b00bbf0e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c371570f6e09477f6baaf17e4df2d5ce796e3bbe59a6dcf3968bdbe365331f3`

```dockerfile
```

-	Layers:
	-	`sha256:cb65ba41f986cad2e3e579670622dcfe895b5b7ddba8190b219b2f6f75a9f0b5`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 5.6 MB (5587018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ff2ff8f9ac2445155647932d693945e0ef8266a01990ba8cd74f9c6d044557`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 20.5 KB (20484 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:637a8197ff99fa0f906f6c26256e9eb4c8de6ba5ccca019e539281754afc238f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.1 MB (543067694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02901e3022acd57191950a629b2ca5f90c3c66e497feca9dac1f7ec1bd256447`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae80cbe3ca198d4d11e7962fae14ee788722cb5a8ca5f903c72f87193ef956bc`  
		Last Modified: Mon, 15 Apr 2024 19:10:21 GMT  
		Size: 381.3 MB (381283496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e26dfdcee33177fcf234925e568baa937631fb46005a572606b34800e84042a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5580321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1506341da924059aeac7173abdf1023cf5629b771b6df5200571d1f1cbbde4d4`

```dockerfile
```

-	Layers:
	-	`sha256:8926afc3c6e0024c1a13aaf4563d391042c634e16f7b3d96d9fafb3af7eacb6c`  
		Last Modified: Mon, 15 Apr 2024 19:10:08 GMT  
		Size: 5.6 MB (5559994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48cd796aff86e8bbc276190abe5bb73daeddc61e99c43911d07fce103c94248`  
		Last Modified: Mon, 15 Apr 2024 19:10:08 GMT  
		Size: 20.3 KB (20327 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19-ubi9`

```console
$ docker pull neo4j@sha256:6ff60303020e2096e531b9f51b3dd4214048f1a5ddb18567a432b4b915a699b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f149a16096b268dba8e37ed6e5d24fe7ac5c6983968fc0125c3fbb359618a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286420831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc3b6882253ce210505f75e486545939729b369eb5643d02191d30f97629eaf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4d548f72423b629fc299dd261f4722d402412e8b4fe61875ab8d63480ce46`  
		Last Modified: Mon, 15 Apr 2024 17:51:01 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1723d6bcbed903f837fd473590884bc58b375b65328ab1359931d92c64b182`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aff705976fd86083b61ee67758825c9bef2e45d006bab49f519579437fa65d`  
		Last Modified: Mon, 15 Apr 2024 17:50:58 GMT  
		Size: 122.8 MB (122826975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:65d53bd3ea916b64914691c4aeb5591f528c7aee6e809227a6e953db61d70c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27723c9613aea064ae328dee8559c26636b684c83b537ec17070f0bd044be331`

```dockerfile
```

-	Layers:
	-	`sha256:823b61534db2c0ed114afeb0c6c28f81e7f81514c9556fb6def3631e5ae348b5`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 5.4 MB (5417885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdb4df3706050afec01c3e6274d4cdb10abfd677e5ea961643ae9afefc41e09`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6368437fd3773a1050545de70c20bca7b013814bf8e36f7d55467c122a836840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284611216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702e579745fc2a928a87cd021296f4cdf936dfcf1129836e1e07a677b9df0c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6187c7fd1c1e727d5c371663cfb33e4c89e37e22e341428081690910bba081b`  
		Last Modified: Mon, 15 Apr 2024 19:09:15 GMT  
		Size: 122.8 MB (122827018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:6b3f019f726265bd69cc5651c1345829ad30a9766b73c6803bef06b30b2b63ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6d1d3b0b9316c7ee553eb668c978392e59125770c1b5438c65a0bdf0abaed1`

```dockerfile
```

-	Layers:
	-	`sha256:88cb64c2418306d7250b6cc02741291917bfd7f472fc80e1da16d0206268378a`  
		Last Modified: Mon, 15 Apr 2024 19:09:12 GMT  
		Size: 5.4 MB (5390869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448970127a68a3cc956ee123dba4233fad905999643583fa9b89e2418bd1c1df`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 21.7 KB (21680 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-bullseye`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-community`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-community-bullseye`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-community-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-community-ubi9`

```console
$ docker pull neo4j@sha256:6ff60303020e2096e531b9f51b3dd4214048f1a5ddb18567a432b4b915a699b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f149a16096b268dba8e37ed6e5d24fe7ac5c6983968fc0125c3fbb359618a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286420831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc3b6882253ce210505f75e486545939729b369eb5643d02191d30f97629eaf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4d548f72423b629fc299dd261f4722d402412e8b4fe61875ab8d63480ce46`  
		Last Modified: Mon, 15 Apr 2024 17:51:01 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1723d6bcbed903f837fd473590884bc58b375b65328ab1359931d92c64b182`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aff705976fd86083b61ee67758825c9bef2e45d006bab49f519579437fa65d`  
		Last Modified: Mon, 15 Apr 2024 17:50:58 GMT  
		Size: 122.8 MB (122826975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:65d53bd3ea916b64914691c4aeb5591f528c7aee6e809227a6e953db61d70c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27723c9613aea064ae328dee8559c26636b684c83b537ec17070f0bd044be331`

```dockerfile
```

-	Layers:
	-	`sha256:823b61534db2c0ed114afeb0c6c28f81e7f81514c9556fb6def3631e5ae348b5`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 5.4 MB (5417885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdb4df3706050afec01c3e6274d4cdb10abfd677e5ea961643ae9afefc41e09`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6368437fd3773a1050545de70c20bca7b013814bf8e36f7d55467c122a836840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284611216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702e579745fc2a928a87cd021296f4cdf936dfcf1129836e1e07a677b9df0c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6187c7fd1c1e727d5c371663cfb33e4c89e37e22e341428081690910bba081b`  
		Last Modified: Mon, 15 Apr 2024 19:09:15 GMT  
		Size: 122.8 MB (122827018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:6b3f019f726265bd69cc5651c1345829ad30a9766b73c6803bef06b30b2b63ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6d1d3b0b9316c7ee553eb668c978392e59125770c1b5438c65a0bdf0abaed1`

```dockerfile
```

-	Layers:
	-	`sha256:88cb64c2418306d7250b6cc02741291917bfd7f472fc80e1da16d0206268378a`  
		Last Modified: Mon, 15 Apr 2024 19:09:12 GMT  
		Size: 5.4 MB (5390869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448970127a68a3cc956ee123dba4233fad905999643583fa9b89e2418bd1c1df`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 21.7 KB (21680 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-enterprise`

```console
$ docker pull neo4j@sha256:4f291adffe0ec129df6caf0cc9be605c57c05085893a8b4589ff93ceaaa120d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8c1e19ad0b1e883111bb89141d19fecfc6e281bca8973c46251e430cab68840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560550562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ad53fda496550bb00b4817ba143f311ad16b871f7c01298a6b9ead22daf4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d045914fdd85147feef4c27332ccedc71c3625d48be84d4e1448030e7db861f`  
		Last Modified: Tue, 16 Apr 2024 05:57:33 GMT  
		Size: 144.9 MB (144893027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b34be4f734d57d2efbc55dc282f3c78576fce72c513b1b412af0216b522020`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193e685bc96219f8a854cc2a5d86e6e02b2333a740f268994faacd43a83331f`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe524bfd946cd8309231f1f5198be4d67ca9a0bea79dca975b8b63cef0e64355`  
		Last Modified: Tue, 16 Apr 2024 05:57:38 GMT  
		Size: 384.2 MB (384216386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:047686ec5f426106154399ec07a654b829585a378764fd93d365657bc691b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64159ef276bf73183baefc169377c967eab58197d2a43a6d26d4dd996cc2ddfd`

```dockerfile
```

-	Layers:
	-	`sha256:35b27975db30bd3b2a0355408fd1898403025317dbb84e598a0457a5616f6b84`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.1 MB (3126524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3dcd552532dcb80666569c6e18bd89683ee201efbbf3e706877ffd9703910`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8799880179071a8027ab15ad95033a286b30879174c455c292f8bf0973a31d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557992776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d011ea593ca5bde711d08805b50b2117adc3a3868cbc00d62fe875d33ff531e1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b683ac2451b67f0da52a6304839840ee13e6f54e9b1a63fd4853e2e17e9b86`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8144829e7b285c8018aa0453e0ccec7d5703a294919e1e8c3974941be1c8beb1`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70d1603b7a10dd3241687a08a21b9411285fcf2e42d313fe3814a96f41b50f8`  
		Last Modified: Tue, 16 Apr 2024 15:55:11 GMT  
		Size: 384.2 MB (384182650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:baf973a97e5a7ede6ed6ce9106629967231220f6adc03e918600da42134f1e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ce9b907cd05a6a237e87e598a73d903da33bda427927090dc654fadc8d4530`

```dockerfile
```

-	Layers:
	-	`sha256:b29993de27c66d7391d637f9d01da43c110d1fe91e54ebee49418c8eea56a536`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.1 MB (3126752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb18ec9846983c4e38dc062d0a6041cac3158c768c8167591bffb3b23a69cab`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4f291adffe0ec129df6caf0cc9be605c57c05085893a8b4589ff93ceaaa120d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8c1e19ad0b1e883111bb89141d19fecfc6e281bca8973c46251e430cab68840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560550562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ad53fda496550bb00b4817ba143f311ad16b871f7c01298a6b9ead22daf4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d045914fdd85147feef4c27332ccedc71c3625d48be84d4e1448030e7db861f`  
		Last Modified: Tue, 16 Apr 2024 05:57:33 GMT  
		Size: 144.9 MB (144893027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b34be4f734d57d2efbc55dc282f3c78576fce72c513b1b412af0216b522020`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193e685bc96219f8a854cc2a5d86e6e02b2333a740f268994faacd43a83331f`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe524bfd946cd8309231f1f5198be4d67ca9a0bea79dca975b8b63cef0e64355`  
		Last Modified: Tue, 16 Apr 2024 05:57:38 GMT  
		Size: 384.2 MB (384216386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:047686ec5f426106154399ec07a654b829585a378764fd93d365657bc691b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64159ef276bf73183baefc169377c967eab58197d2a43a6d26d4dd996cc2ddfd`

```dockerfile
```

-	Layers:
	-	`sha256:35b27975db30bd3b2a0355408fd1898403025317dbb84e598a0457a5616f6b84`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.1 MB (3126524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3dcd552532dcb80666569c6e18bd89683ee201efbbf3e706877ffd9703910`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8799880179071a8027ab15ad95033a286b30879174c455c292f8bf0973a31d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557992776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d011ea593ca5bde711d08805b50b2117adc3a3868cbc00d62fe875d33ff531e1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b683ac2451b67f0da52a6304839840ee13e6f54e9b1a63fd4853e2e17e9b86`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8144829e7b285c8018aa0453e0ccec7d5703a294919e1e8c3974941be1c8beb1`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70d1603b7a10dd3241687a08a21b9411285fcf2e42d313fe3814a96f41b50f8`  
		Last Modified: Tue, 16 Apr 2024 15:55:11 GMT  
		Size: 384.2 MB (384182650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:baf973a97e5a7ede6ed6ce9106629967231220f6adc03e918600da42134f1e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ce9b907cd05a6a237e87e598a73d903da33bda427927090dc654fadc8d4530`

```dockerfile
```

-	Layers:
	-	`sha256:b29993de27c66d7391d637f9d01da43c110d1fe91e54ebee49418c8eea56a536`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.1 MB (3126752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb18ec9846983c4e38dc062d0a6041cac3158c768c8167591bffb3b23a69cab`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4b46fa568dd07658aa91edb82a39cd6ab1da29594e85f0e64a7b6b34852cdb71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:89e66e370b953867865ec42529f549e6592bd6218dde1eb6b2d4b9e3a8fa8e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572789982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8741b07b1bd0088bf10a2a4d0b0dfd7b475bf61efd57b0426f836afda8c7dd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761328989f6454fc52ab4a6325c234c252505728a21baaf4fa876ccdf1a6286`  
		Last Modified: Mon, 15 Apr 2024 17:51:29 GMT  
		Size: 152.2 MB (152193909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca229d35f3a54ebb7e89ddc8aabb118af7271a43866409a70c90c848d2de7d4`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c6f275388aedb4cac2a7c6bac0015549e72a024a89d9b84a60dcd176905ef0`  
		Last Modified: Mon, 15 Apr 2024 17:51:34 GMT  
		Size: 381.3 MB (381283989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:49193bd409ec39194cdd4cb019da5aa44e6e4760e9a98253687ffaeeefc28245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fac76f47059c8b9555a247ddc0bc909f2d230031ef54c4d3897a458cfbb6b`

```dockerfile
```

-	Layers:
	-	`sha256:6f52a794f1410c61aad221842f37232750fce9db4900157073061108086a959d`  
		Last Modified: Mon, 15 Apr 2024 17:51:28 GMT  
		Size: 10.5 MB (10476665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6754a719bbbc73035667d9f73ef8a9854e85f89807d09e098d8779a08919b23`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb19dc31dcc014978d6df364433a477ff72aa14005a732d684a5435a02975369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569756380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c286a5b4dc9711136965c77cf1e54bd96b7726da0fcf41bfca3d7fd3466be21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cdc4ba88fa17faa117469b03cc7a82a8d4f6066b952764949edb2dfd272266`  
		Last Modified: Mon, 15 Apr 2024 20:18:30 GMT  
		Size: 381.3 MB (381284101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:f6d89a6dc4cb0617fc906b8507a2821d6bc944256f3ee4b12d3ccf96343acb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b2347fb030d4e4077a59bd469395607e522560486095e9cf9bcfdffe7fc0e5`

```dockerfile
```

-	Layers:
	-	`sha256:b557b2be4aa277741aecb0989e315a06fc1aa63e569a423b23513ef0e92ff682`  
		Last Modified: Mon, 15 Apr 2024 20:18:24 GMT  
		Size: 10.5 MB (10474203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95428b7beb425e0a9adc2f040a930e9ad237ab51eacceedf6454e3700c54ff49`  
		Last Modified: Mon, 15 Apr 2024 20:18:22 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9af1902ed24cc018c4e56563ef0e8920db365d30feaaf5fd00973a63fac77c44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fc6f5a67872c09b3e55b9a1f2b86b07318cc823a4169c55730b7f37366028d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.9 MB (544877316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db590246bc60971db355a306d691f31f6f791668f115cd64f5f930cb676296b7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfaeed02d926d856000abe4d8db10c1eb84530e4cf95177d739fca840844123`  
		Last Modified: Mon, 15 Apr 2024 17:51:14 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1c916a88f38f8fdfae4addc23aa1b1788a9d0499fb5ac36cbc24a87546527c`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ce8d0c209068dd3485e886fa5f7346cdaf0e320b6019a4dc79b8425ec575b5`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 381.3 MB (381283460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8ac0de2f84a62d87a8a1381efd3e060fcb6cc68dd436958ad1228b00bbf0e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c371570f6e09477f6baaf17e4df2d5ce796e3bbe59a6dcf3968bdbe365331f3`

```dockerfile
```

-	Layers:
	-	`sha256:cb65ba41f986cad2e3e579670622dcfe895b5b7ddba8190b219b2f6f75a9f0b5`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 5.6 MB (5587018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ff2ff8f9ac2445155647932d693945e0ef8266a01990ba8cd74f9c6d044557`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 20.5 KB (20484 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:637a8197ff99fa0f906f6c26256e9eb4c8de6ba5ccca019e539281754afc238f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.1 MB (543067694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02901e3022acd57191950a629b2ca5f90c3c66e497feca9dac1f7ec1bd256447`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae80cbe3ca198d4d11e7962fae14ee788722cb5a8ca5f903c72f87193ef956bc`  
		Last Modified: Mon, 15 Apr 2024 19:10:21 GMT  
		Size: 381.3 MB (381283496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e26dfdcee33177fcf234925e568baa937631fb46005a572606b34800e84042a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5580321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1506341da924059aeac7173abdf1023cf5629b771b6df5200571d1f1cbbde4d4`

```dockerfile
```

-	Layers:
	-	`sha256:8926afc3c6e0024c1a13aaf4563d391042c634e16f7b3d96d9fafb3af7eacb6c`  
		Last Modified: Mon, 15 Apr 2024 19:10:08 GMT  
		Size: 5.6 MB (5559994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48cd796aff86e8bbc276190abe5bb73daeddc61e99c43911d07fce103c94248`  
		Last Modified: Mon, 15 Apr 2024 19:10:08 GMT  
		Size: 20.3 KB (20327 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.19.0-ubi9`

```console
$ docker pull neo4j@sha256:6ff60303020e2096e531b9f51b3dd4214048f1a5ddb18567a432b4b915a699b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.19.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f149a16096b268dba8e37ed6e5d24fe7ac5c6983968fc0125c3fbb359618a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286420831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc3b6882253ce210505f75e486545939729b369eb5643d02191d30f97629eaf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4d548f72423b629fc299dd261f4722d402412e8b4fe61875ab8d63480ce46`  
		Last Modified: Mon, 15 Apr 2024 17:51:01 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1723d6bcbed903f837fd473590884bc58b375b65328ab1359931d92c64b182`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aff705976fd86083b61ee67758825c9bef2e45d006bab49f519579437fa65d`  
		Last Modified: Mon, 15 Apr 2024 17:50:58 GMT  
		Size: 122.8 MB (122826975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:65d53bd3ea916b64914691c4aeb5591f528c7aee6e809227a6e953db61d70c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27723c9613aea064ae328dee8559c26636b684c83b537ec17070f0bd044be331`

```dockerfile
```

-	Layers:
	-	`sha256:823b61534db2c0ed114afeb0c6c28f81e7f81514c9556fb6def3631e5ae348b5`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 5.4 MB (5417885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdb4df3706050afec01c3e6274d4cdb10abfd677e5ea961643ae9afefc41e09`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.19.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6368437fd3773a1050545de70c20bca7b013814bf8e36f7d55467c122a836840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284611216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702e579745fc2a928a87cd021296f4cdf936dfcf1129836e1e07a677b9df0c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6187c7fd1c1e727d5c371663cfb33e4c89e37e22e341428081690910bba081b`  
		Last Modified: Mon, 15 Apr 2024 19:09:15 GMT  
		Size: 122.8 MB (122827018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.19.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:6b3f019f726265bd69cc5651c1345829ad30a9766b73c6803bef06b30b2b63ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6d1d3b0b9316c7ee553eb668c978392e59125770c1b5438c65a0bdf0abaed1`

```dockerfile
```

-	Layers:
	-	`sha256:88cb64c2418306d7250b6cc02741291917bfd7f472fc80e1da16d0206268378a`  
		Last Modified: Mon, 15 Apr 2024 19:09:12 GMT  
		Size: 5.4 MB (5390869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448970127a68a3cc956ee123dba4233fad905999643583fa9b89e2418bd1c1df`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 21.7 KB (21680 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:6ff60303020e2096e531b9f51b3dd4214048f1a5ddb18567a432b4b915a699b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f149a16096b268dba8e37ed6e5d24fe7ac5c6983968fc0125c3fbb359618a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286420831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc3b6882253ce210505f75e486545939729b369eb5643d02191d30f97629eaf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4d548f72423b629fc299dd261f4722d402412e8b4fe61875ab8d63480ce46`  
		Last Modified: Mon, 15 Apr 2024 17:51:01 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1723d6bcbed903f837fd473590884bc58b375b65328ab1359931d92c64b182`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aff705976fd86083b61ee67758825c9bef2e45d006bab49f519579437fa65d`  
		Last Modified: Mon, 15 Apr 2024 17:50:58 GMT  
		Size: 122.8 MB (122826975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:65d53bd3ea916b64914691c4aeb5591f528c7aee6e809227a6e953db61d70c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27723c9613aea064ae328dee8559c26636b684c83b537ec17070f0bd044be331`

```dockerfile
```

-	Layers:
	-	`sha256:823b61534db2c0ed114afeb0c6c28f81e7f81514c9556fb6def3631e5ae348b5`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 5.4 MB (5417885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdb4df3706050afec01c3e6274d4cdb10abfd677e5ea961643ae9afefc41e09`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6368437fd3773a1050545de70c20bca7b013814bf8e36f7d55467c122a836840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284611216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702e579745fc2a928a87cd021296f4cdf936dfcf1129836e1e07a677b9df0c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6187c7fd1c1e727d5c371663cfb33e4c89e37e22e341428081690910bba081b`  
		Last Modified: Mon, 15 Apr 2024 19:09:15 GMT  
		Size: 122.8 MB (122827018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:6b3f019f726265bd69cc5651c1345829ad30a9766b73c6803bef06b30b2b63ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6d1d3b0b9316c7ee553eb668c978392e59125770c1b5438c65a0bdf0abaed1`

```dockerfile
```

-	Layers:
	-	`sha256:88cb64c2418306d7250b6cc02741291917bfd7f472fc80e1da16d0206268378a`  
		Last Modified: Mon, 15 Apr 2024 19:09:12 GMT  
		Size: 5.4 MB (5390869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448970127a68a3cc956ee123dba4233fad905999643583fa9b89e2418bd1c1df`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 21.7 KB (21680 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:4f291adffe0ec129df6caf0cc9be605c57c05085893a8b4589ff93ceaaa120d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8c1e19ad0b1e883111bb89141d19fecfc6e281bca8973c46251e430cab68840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560550562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ad53fda496550bb00b4817ba143f311ad16b871f7c01298a6b9ead22daf4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d045914fdd85147feef4c27332ccedc71c3625d48be84d4e1448030e7db861f`  
		Last Modified: Tue, 16 Apr 2024 05:57:33 GMT  
		Size: 144.9 MB (144893027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b34be4f734d57d2efbc55dc282f3c78576fce72c513b1b412af0216b522020`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193e685bc96219f8a854cc2a5d86e6e02b2333a740f268994faacd43a83331f`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe524bfd946cd8309231f1f5198be4d67ca9a0bea79dca975b8b63cef0e64355`  
		Last Modified: Tue, 16 Apr 2024 05:57:38 GMT  
		Size: 384.2 MB (384216386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:047686ec5f426106154399ec07a654b829585a378764fd93d365657bc691b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64159ef276bf73183baefc169377c967eab58197d2a43a6d26d4dd996cc2ddfd`

```dockerfile
```

-	Layers:
	-	`sha256:35b27975db30bd3b2a0355408fd1898403025317dbb84e598a0457a5616f6b84`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.1 MB (3126524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3dcd552532dcb80666569c6e18bd89683ee201efbbf3e706877ffd9703910`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8799880179071a8027ab15ad95033a286b30879174c455c292f8bf0973a31d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557992776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d011ea593ca5bde711d08805b50b2117adc3a3868cbc00d62fe875d33ff531e1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b683ac2451b67f0da52a6304839840ee13e6f54e9b1a63fd4853e2e17e9b86`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8144829e7b285c8018aa0453e0ccec7d5703a294919e1e8c3974941be1c8beb1`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70d1603b7a10dd3241687a08a21b9411285fcf2e42d313fe3814a96f41b50f8`  
		Last Modified: Tue, 16 Apr 2024 15:55:11 GMT  
		Size: 384.2 MB (384182650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:baf973a97e5a7ede6ed6ce9106629967231220f6adc03e918600da42134f1e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ce9b907cd05a6a237e87e598a73d903da33bda427927090dc654fadc8d4530`

```dockerfile
```

-	Layers:
	-	`sha256:b29993de27c66d7391d637f9d01da43c110d1fe91e54ebee49418c8eea56a536`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.1 MB (3126752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb18ec9846983c4e38dc062d0a6041cac3158c768c8167591bffb3b23a69cab`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:4f291adffe0ec129df6caf0cc9be605c57c05085893a8b4589ff93ceaaa120d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8c1e19ad0b1e883111bb89141d19fecfc6e281bca8973c46251e430cab68840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.6 MB (560550562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90ad53fda496550bb00b4817ba143f311ad16b871f7c01298a6b9ead22daf4f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d045914fdd85147feef4c27332ccedc71c3625d48be84d4e1448030e7db861f`  
		Last Modified: Tue, 16 Apr 2024 05:57:33 GMT  
		Size: 144.9 MB (144893027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b34be4f734d57d2efbc55dc282f3c78576fce72c513b1b412af0216b522020`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.8 KB (3842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193e685bc96219f8a854cc2a5d86e6e02b2333a740f268994faacd43a83331f`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe524bfd946cd8309231f1f5198be4d67ca9a0bea79dca975b8b63cef0e64355`  
		Last Modified: Tue, 16 Apr 2024 05:57:38 GMT  
		Size: 384.2 MB (384216386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:047686ec5f426106154399ec07a654b829585a378764fd93d365657bc691b1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64159ef276bf73183baefc169377c967eab58197d2a43a6d26d4dd996cc2ddfd`

```dockerfile
```

-	Layers:
	-	`sha256:35b27975db30bd3b2a0355408fd1898403025317dbb84e598a0457a5616f6b84`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 3.1 MB (3126524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a3dcd552532dcb80666569c6e18bd89683ee201efbbf3e706877ffd9703910`  
		Last Modified: Tue, 16 Apr 2024 05:57:31 GMT  
		Size: 21.9 KB (21892 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8799880179071a8027ab15ad95033a286b30879174c455c292f8bf0973a31d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.0 MB (557992776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d011ea593ca5bde711d08805b50b2117adc3a3868cbc00d62fe875d33ff531e1`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b683ac2451b67f0da52a6304839840ee13e6f54e9b1a63fd4853e2e17e9b86`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8144829e7b285c8018aa0453e0ccec7d5703a294919e1e8c3974941be1c8beb1`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70d1603b7a10dd3241687a08a21b9411285fcf2e42d313fe3814a96f41b50f8`  
		Last Modified: Tue, 16 Apr 2024 15:55:11 GMT  
		Size: 384.2 MB (384182650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:baf973a97e5a7ede6ed6ce9106629967231220f6adc03e918600da42134f1e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ce9b907cd05a6a237e87e598a73d903da33bda427927090dc654fadc8d4530`

```dockerfile
```

-	Layers:
	-	`sha256:b29993de27c66d7391d637f9d01da43c110d1fe91e54ebee49418c8eea56a536`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 3.1 MB (3126752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb18ec9846983c4e38dc062d0a6041cac3158c768c8167591bffb3b23a69cab`  
		Last Modified: Tue, 16 Apr 2024 15:55:03 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4b46fa568dd07658aa91edb82a39cd6ab1da29594e85f0e64a7b6b34852cdb71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:89e66e370b953867865ec42529f549e6592bd6218dde1eb6b2d4b9e3a8fa8e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.8 MB (572789982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8741b07b1bd0088bf10a2a4d0b0dfd7b475bf61efd57b0426f836afda8c7dd7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761328989f6454fc52ab4a6325c234c252505728a21baaf4fa876ccdf1a6286`  
		Last Modified: Mon, 15 Apr 2024 17:51:29 GMT  
		Size: 152.2 MB (152193909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca229d35f3a54ebb7e89ddc8aabb118af7271a43866409a70c90c848d2de7d4`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c6f275388aedb4cac2a7c6bac0015549e72a024a89d9b84a60dcd176905ef0`  
		Last Modified: Mon, 15 Apr 2024 17:51:34 GMT  
		Size: 381.3 MB (381283989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:49193bd409ec39194cdd4cb019da5aa44e6e4760e9a98253687ffaeeefc28245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5fac76f47059c8b9555a247ddc0bc909f2d230031ef54c4d3897a458cfbb6b`

```dockerfile
```

-	Layers:
	-	`sha256:6f52a794f1410c61aad221842f37232750fce9db4900157073061108086a959d`  
		Last Modified: Mon, 15 Apr 2024 17:51:28 GMT  
		Size: 10.5 MB (10476665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6754a719bbbc73035667d9f73ef8a9854e85f89807d09e098d8779a08919b23`  
		Last Modified: Mon, 15 Apr 2024 17:51:27 GMT  
		Size: 20.5 KB (20458 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cb19dc31dcc014978d6df364433a477ff72aa14005a732d684a5435a02975369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **569.8 MB (569756380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c286a5b4dc9711136965c77cf1e54bd96b7726da0fcf41bfca3d7fd3466be21`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cdc4ba88fa17faa117469b03cc7a82a8d4f6066b952764949edb2dfd272266`  
		Last Modified: Mon, 15 Apr 2024 20:18:30 GMT  
		Size: 381.3 MB (381284101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:f6d89a6dc4cb0617fc906b8507a2821d6bc944256f3ee4b12d3ccf96343acb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b2347fb030d4e4077a59bd469395607e522560486095e9cf9bcfdffe7fc0e5`

```dockerfile
```

-	Layers:
	-	`sha256:b557b2be4aa277741aecb0989e315a06fc1aa63e569a423b23513ef0e92ff682`  
		Last Modified: Mon, 15 Apr 2024 20:18:24 GMT  
		Size: 10.5 MB (10474203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95428b7beb425e0a9adc2f040a930e9ad237ab51eacceedf6454e3700c54ff49`  
		Last Modified: Mon, 15 Apr 2024 20:18:22 GMT  
		Size: 20.3 KB (20300 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9af1902ed24cc018c4e56563ef0e8920db365d30feaaf5fd00973a63fac77c44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fc6f5a67872c09b3e55b9a1f2b86b07318cc823a4169c55730b7f37366028d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.9 MB (544877316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db590246bc60971db355a306d691f31f6f791668f115cd64f5f930cb676296b7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfaeed02d926d856000abe4d8db10c1eb84530e4cf95177d739fca840844123`  
		Last Modified: Mon, 15 Apr 2024 17:51:14 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1c916a88f38f8fdfae4addc23aa1b1788a9d0499fb5ac36cbc24a87546527c`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ce8d0c209068dd3485e886fa5f7346cdaf0e320b6019a4dc79b8425ec575b5`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 381.3 MB (381283460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a8ac0de2f84a62d87a8a1381efd3e060fcb6cc68dd436958ad1228b00bbf0e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c371570f6e09477f6baaf17e4df2d5ce796e3bbe59a6dcf3968bdbe365331f3`

```dockerfile
```

-	Layers:
	-	`sha256:cb65ba41f986cad2e3e579670622dcfe895b5b7ddba8190b219b2f6f75a9f0b5`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 5.6 MB (5587018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6ff2ff8f9ac2445155647932d693945e0ef8266a01990ba8cd74f9c6d044557`  
		Last Modified: Mon, 15 Apr 2024 17:51:10 GMT  
		Size: 20.5 KB (20484 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:637a8197ff99fa0f906f6c26256e9eb4c8de6ba5ccca019e539281754afc238f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **543.1 MB (543067694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02901e3022acd57191950a629b2ca5f90c3c66e497feca9dac1f7ec1bd256447`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=6dc5af32f8e01f1cb8f8618d1314d91713172db14f53c695b77ca733ff504356 NEO4J_TARBALL=neo4j-enterprise-5.19.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae80cbe3ca198d4d11e7962fae14ee788722cb5a8ca5f903c72f87193ef956bc`  
		Last Modified: Mon, 15 Apr 2024 19:10:21 GMT  
		Size: 381.3 MB (381283496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e26dfdcee33177fcf234925e568baa937631fb46005a572606b34800e84042a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5580321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1506341da924059aeac7173abdf1023cf5629b771b6df5200571d1f1cbbde4d4`

```dockerfile
```

-	Layers:
	-	`sha256:8926afc3c6e0024c1a13aaf4563d391042c634e16f7b3d96d9fafb3af7eacb6c`  
		Last Modified: Mon, 15 Apr 2024 19:10:08 GMT  
		Size: 5.6 MB (5559994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48cd796aff86e8bbc276190abe5bb73daeddc61e99c43911d07fce103c94248`  
		Last Modified: Mon, 15 Apr 2024 19:10:08 GMT  
		Size: 20.3 KB (20327 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:276114b1d8a1934f96baf91d377a85ab81df747a8f82704f4fdd7dd6abadd185
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:a73e52d5207e4bc7952158742ed7b3534a41813eadaef47ecd9ac7bb729fbed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302092560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2865447891559c231ffb1848236a66752351a32473f733a1fe7f3e047f8bc5d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d32022c38413ff94ca4e6fc5d75ae897c2ec6a0489a96a7833885af9e64de12`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 144.9 MB (144893042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a9957b51c12d051cdb465fd6954b6b92de2702c6032b98bf5df24c54341932`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42502fbd0b54239f78a355bdf245326c34fc83f111a336351d0a3400e7c0f4bb`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54570c3eeb94264819d213c70d23ea47b921c5cd9086873d8c18b22c149e4d8d`  
		Last Modified: Tue, 16 Apr 2024 05:57:25 GMT  
		Size: 125.8 MB (125758369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:9db0627de082a560b7fc4fb03ca38732de126af716bae2be4d04a5a14b90422c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2982846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33534431a6b63aaf0292f48de6ae6a08232e6398cfdc9c1e7e4fb21dedacf35e`

```dockerfile
```

-	Layers:
	-	`sha256:0ce782c6052acc91bd0d7110f4ca52ec5a7c2aa57510981d9e61bd642d3dba5d`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 3.0 MB (2958585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9bdc5a7090c6de181093d31a63f73275826a38e26959687e45c741dd36ae84`  
		Last Modified: Tue, 16 Apr 2024 05:57:22 GMT  
		Size: 24.3 KB (24261 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4609501f4a68375e5095fe5eca67a795a0680ff6358a9cd4f175e18dbca14f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 MB (299531061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1ba4653d3749cc5d7bac2c5f8a9deb8bf111b4d217e32624795a6401a71361`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Apr 2024 11:14:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34607ecd87ee1321fe73af36c7f3a85eb8e748f9fcff655b86b7e42a2a4b79`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 143.7 MB (143720375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca19128475e73ab6e233697dfdb22eb14b2243a69dda68bb7908ee453aaa6206`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4280f66c1b004cffa2212594975f2e21fd2d0b6bbea98d39231d4f2b7d6b66ce`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b478b13db318c956e56f47ae2753445add4ae378487612b32602c5c15125284e`  
		Last Modified: Tue, 16 Apr 2024 15:53:48 GMT  
		Size: 125.7 MB (125720931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:82141ddf1c29fb983b9951204bb16618bbe2f24a23076129d2323a7cc4c2bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247d4fe285cf29de4e2e650c050c0e1fac119019a0c46157f1224ed3748150bb`

```dockerfile
```

-	Layers:
	-	`sha256:751ec30e0551c2d7539979ac8da88342233c831254a8134f410742098da82080`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 3.0 MB (2958829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c89544e82bb2a637c802bce477e9efbdcdc0690349c49272ad794f06b0b463`  
		Last Modified: Tue, 16 Apr 2024 15:53:45 GMT  
		Size: 22.5 KB (22480 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:0267d4720d41d912ce9026d1ac59f705c4fde0a76bd14b6a6b9584e8e7f55d4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:891868692fa13b977550634de8b4e1a561b90fb0d84e064a6a44623e4f1c879c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314332914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5284f2fcdacc1c1709ccdcab06a7e1ebcd7df6f8aaa62069c08124f3ae53d36`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:95eb79941a03d83910cc9acb8e3e38d22b90990089e0cb77bcaed3a5dd8644cd in / 
# Wed, 27 Mar 2024 02:22:33 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:33 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:33 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:33 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:34 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:1118ec7f864d2e2c1b6c66eabed90396af13f230921e05643064fb7390bcc479 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:34 GMT
ADD file:d804511757411e79b6c0386103538245cf9968ea1ba311c66c59a9cd5bc39ea7 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:34 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:458deefb34fd5ebe4d61ee921d46e7c8994065680078e8c671d4f4bac3b10ec3`  
		Last Modified: Tue, 02 Apr 2024 18:09:25 GMT  
		Size: 39.3 MB (39302356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72ac592c4930225390d5c6b7b352b3e64998905670f3daf2aed7d01d065b17`  
		Last Modified: Mon, 15 Apr 2024 17:51:19 GMT  
		Size: 152.2 MB (152193668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57776219bc2152e268af9cef8b841586332c1920703bdef5de90dd37d0e69ddb`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619d8498dccc970bd7035b3a26b523c0111574bfc975aed3a4a583e4b3344218`  
		Last Modified: Mon, 15 Apr 2024 17:51:18 GMT  
		Size: 122.8 MB (122827162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:c8e52ef4ccbf1a2202762f8603fdcee972769c54a3aaa454af853ef16dc64c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312c562ba53c5e87b165f1a651d10d68a0e9f198b697956caf026b388569b99f`

```dockerfile
```

-	Layers:
	-	`sha256:e9c16d5a296729a5e25b17afb7dd5101b8a9e61afc0aef04a4802205ba9d14fc`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 10.3 MB (10307532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd88bfb91255cbeb9c5a56c64e17cb976bd9e309cb71595c59d8cc192f0340c2`  
		Last Modified: Mon, 15 Apr 2024 17:51:17 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b4f77953f8e9014e232bd28a403613db8182466275d5758aeac93ab21fba650d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311299469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b77b6005358fbe0f53aec0fac4a7b5f856209d12a191df82264d5423d402d60`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 27 Mar 2024 02:22:31 GMT
ADD file:5e475a5ac78f2dc167defdef4698c5ffd32df46bc45f1b8831a6301902fbcb32 in / 
# Wed, 27 Mar 2024 02:22:32 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 27 Mar 2024 02:22:32 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Wed, 27 Mar 2024 02:22:32 GMT
ADD multi:8d9f0a1a40be53261a5af974e166478a8bff2424b1408baed1f59ea95b0e5a35 in /etc/yum.repos.d/ 
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 Mar 2024 02:22:32 GMT
LABEL io.openshift.tags="minimal rhel8"
# Wed, 27 Mar 2024 02:22:32 GMT
ENV container oci
# Wed, 27 Mar 2024 02:22:32 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Mar 2024 02:22:32 GMT
CMD ["/bin/bash"]
# Wed, 27 Mar 2024 02:22:33 GMT
RUN rm -rf /var/log/*
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL release=1161
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:29eb98835b0998596f28947888784f8b0e1edb077d79ae0c6d6dd4aacbfe92da in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1161.json 
# Wed, 27 Mar 2024 02:22:33 GMT
ADD file:b280235b81c5045e893644d138d521d6ff7460ac874cca8bb64bad39b732d8f8 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1161 
# Wed, 27 Mar 2024 02:22:33 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-03-27T02:10:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1161"
# Wed, 27 Mar 2024 02:22:35 GMT
RUN rm -f '/etc/yum.repos.d/repo-92821.repo' '/etc/yum.repos.d/repo-1876c.repo'
# Wed, 27 Mar 2024 02:22:36 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 27 Mar 2024 02:22:37 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
ENV JAVA_HOME=/usr
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0117dee8e815188cd7730b6fcd34a97b4e46a81ee9295f2b8988ea6cb636372d`  
		Last Modified: Tue, 02 Apr 2024 18:59:21 GMT  
		Size: 37.7 MB (37739954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1efb5b3e566e21dce41aa0201d50663c7333e0f78f5f6afa8a3db6cd2551a9`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 150.7 MB (150722595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6621aabbc65f263d88fa27e9abfdf39916fb2cdc1a80c24739e71a81e7f64bd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 9.7 KB (9698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bd58448df484e65afa039ec2877fea347400c4580efa4eb38dc4d1850e6589`  
		Last Modified: Mon, 15 Apr 2024 19:35:40 GMT  
		Size: 122.8 MB (122827190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a556bc54416b1526ed49b499320eb302255927b0077eb0b214c2f77299593a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10326732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0c25743b62c1f1516c7392d1ea8ca5b2067942fc9c12a16ec3daeeb9839a5`

```dockerfile
```

-	Layers:
	-	`sha256:ce9f4aff6e292522216da7a20422e6f40973871bca1043a19fa82db520461cfd`  
		Last Modified: Mon, 15 Apr 2024 19:35:37 GMT  
		Size: 10.3 MB (10305078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da29eaa0b11b45447ab41f6dd4947bfe7e1a0d19180c9505082c08bbce629dd`  
		Last Modified: Mon, 15 Apr 2024 19:35:36 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:6ff60303020e2096e531b9f51b3dd4214048f1a5ddb18567a432b4b915a699b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f149a16096b268dba8e37ed6e5d24fe7ac5c6983968fc0125c3fbb359618a585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286420831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc3b6882253ce210505f75e486545939729b369eb5643d02191d30f97629eaf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:45 GMT
ADD file:68e24d23b5f22084b226415d33dd1fcc53f68b0b3949e70fad3179e338fc8077 in / 
# Thu, 29 Feb 2024 14:19:46 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:46 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:46 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:46 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:46 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:46 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:96798c96d3dfcbd827cc4604cb7c680f64dbd1730ae16ef972d4c8c1724e5dfb in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:47 GMT
ADD file:77a2a326b0f16be9a06e11649cf96f606502d3b242d11c8f6562a4f7c2b91d9d in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:47 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:48 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:49 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2895d6faeea81934722a9a23efd8814ca51c1af558a3a70983ad2f7a412cdbe8`  
		Last Modified: Tue, 05 Mar 2024 21:18:08 GMT  
		Size: 37.7 MB (37695188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b4d548f72423b629fc299dd261f4722d402412e8b4fe61875ab8d63480ce46`  
		Last Modified: Mon, 15 Apr 2024 17:51:01 GMT  
		Size: 125.9 MB (125889097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1723d6bcbed903f837fd473590884bc58b375b65328ab1359931d92c64b182`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aff705976fd86083b61ee67758825c9bef2e45d006bab49f519579437fa65d`  
		Last Modified: Mon, 15 Apr 2024 17:50:58 GMT  
		Size: 122.8 MB (122826975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:65d53bd3ea916b64914691c4aeb5591f528c7aee6e809227a6e953db61d70c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27723c9613aea064ae328dee8559c26636b684c83b537ec17070f0bd044be331`

```dockerfile
```

-	Layers:
	-	`sha256:823b61534db2c0ed114afeb0c6c28f81e7f81514c9556fb6def3631e5ae348b5`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 5.4 MB (5417885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdb4df3706050afec01c3e6274d4cdb10abfd677e5ea961643ae9afefc41e09`  
		Last Modified: Mon, 15 Apr 2024 17:50:55 GMT  
		Size: 21.7 KB (21662 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6368437fd3773a1050545de70c20bca7b013814bf8e36f7d55467c122a836840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284611216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702e579745fc2a928a87cd021296f4cdf936dfcf1129836e1e07a677b9df0c3`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 29 Feb 2024 14:19:42 GMT
ADD file:437369795a208dae019ad106a8100166db532f040a1b0872857a6e2765904923 in / 
# Thu, 29 Feb 2024 14:19:43 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 29 Feb 2024 14:19:43 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 29 Feb 2024 14:19:43 GMT
ADD multi:76ed2bd9c036240d42925ff871f73866e886bea98859bc8c40c9fb05e07b6fb9 in /etc/yum.repos.d/ 
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.expose-services=""
# Thu, 29 Feb 2024 14:19:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 29 Feb 2024 14:19:43 GMT
ENV container oci
# Thu, 29 Feb 2024 14:19:43 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 14:19:43 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 14:19:44 GMT
RUN rm -rf /var/log/*
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL release=1612
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:96d801555bcde0b213796fa230f06bd442ea605a02a35260236e9b419cfd729d in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1612.json 
# Thu, 29 Feb 2024 14:19:44 GMT
ADD file:ae24bc70d71374ac8bbfcf5164284b94f4587f14ff3b75af2fe02d3bc797deac in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1612 
# Thu, 29 Feb 2024 14:19:44 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-29T14:02:27" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1612"
# Thu, 29 Feb 2024 14:19:45 GMT
RUN rm -f '/etc/yum.repos.d/repo-3cf8a.repo' '/etc/yum.repos.d/repo-e6c6f.repo'
# Thu, 29 Feb 2024 14:19:47 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 29 Feb 2024 14:19:48 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Fri, 12 Apr 2024 11:14:18 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc;     microdnf clean all # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV NEO4J_SHA256=30f4eb3156ebdd7905ce2775146c802b9b1104c08c331b1d6ca126aaff5a00d9 NEO4J_TARBALL=neo4j-community-5.19.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
# Fri, 12 Apr 2024 11:14:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.19.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Fri, 12 Apr 2024 11:14:18 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 11:14:18 GMT
WORKDIR /var/lib/neo4j
# Fri, 12 Apr 2024 11:14:18 GMT
VOLUME [/data /logs]
# Fri, 12 Apr 2024 11:14:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 12 Apr 2024 11:14:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 12 Apr 2024 11:14:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:29e2333f8e0bceaa897a773c4379290a140a34c907a4e38ccf82a09fe20181bd`  
		Last Modified: Tue, 05 Mar 2024 21:53:06 GMT  
		Size: 36.0 MB (35983791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05729221f1df11ee52ea302ac11c5938b4574c05ab775c545afa8968ee072b48`  
		Last Modified: Mon, 15 Apr 2024 19:09:14 GMT  
		Size: 125.8 MB (125790836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8434b644101c7e796e641622b4351c98c1b2fb70a138a760bc99521e98e0e8d2`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6187c7fd1c1e727d5c371663cfb33e4c89e37e22e341428081690910bba081b`  
		Last Modified: Mon, 15 Apr 2024 19:09:15 GMT  
		Size: 122.8 MB (122827018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:6b3f019f726265bd69cc5651c1345829ad30a9766b73c6803bef06b30b2b63ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6d1d3b0b9316c7ee553eb668c978392e59125770c1b5438c65a0bdf0abaed1`

```dockerfile
```

-	Layers:
	-	`sha256:88cb64c2418306d7250b6cc02741291917bfd7f472fc80e1da16d0206268378a`  
		Last Modified: Mon, 15 Apr 2024 19:09:12 GMT  
		Size: 5.4 MB (5390869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448970127a68a3cc956ee123dba4233fad905999643583fa9b89e2418bd1c1df`  
		Last Modified: Mon, 15 Apr 2024 19:09:11 GMT  
		Size: 21.7 KB (21680 bytes)  
		MIME: application/vnd.in-toto+json
