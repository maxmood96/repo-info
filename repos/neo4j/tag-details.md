<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.34`](#neo4j4434)
-	[`neo4j:4.4.34-community`](#neo4j4434-community)
-	[`neo4j:4.4.34-enterprise`](#neo4j4434-enterprise)
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
-	[`neo4j:5.20`](#neo4j520)
-	[`neo4j:5.20-bullseye`](#neo4j520-bullseye)
-	[`neo4j:5.20-community`](#neo4j520-community)
-	[`neo4j:5.20-community-bullseye`](#neo4j520-community-bullseye)
-	[`neo4j:5.20-community-ubi8`](#neo4j520-community-ubi8)
-	[`neo4j:5.20-community-ubi9`](#neo4j520-community-ubi9)
-	[`neo4j:5.20-enterprise`](#neo4j520-enterprise)
-	[`neo4j:5.20-enterprise-bullseye`](#neo4j520-enterprise-bullseye)
-	[`neo4j:5.20-enterprise-ubi8`](#neo4j520-enterprise-ubi8)
-	[`neo4j:5.20-enterprise-ubi9`](#neo4j520-enterprise-ubi9)
-	[`neo4j:5.20-ubi8`](#neo4j520-ubi8)
-	[`neo4j:5.20-ubi9`](#neo4j520-ubi9)
-	[`neo4j:5.20.0`](#neo4j5200)
-	[`neo4j:5.20.0-bullseye`](#neo4j5200-bullseye)
-	[`neo4j:5.20.0-community`](#neo4j5200-community)
-	[`neo4j:5.20.0-community-bullseye`](#neo4j5200-community-bullseye)
-	[`neo4j:5.20.0-community-ubi8`](#neo4j5200-community-ubi8)
-	[`neo4j:5.20.0-community-ubi9`](#neo4j5200-community-ubi9)
-	[`neo4j:5.20.0-enterprise`](#neo4j5200-enterprise)
-	[`neo4j:5.20.0-enterprise-bullseye`](#neo4j5200-enterprise-bullseye)
-	[`neo4j:5.20.0-enterprise-ubi8`](#neo4j5200-enterprise-ubi8)
-	[`neo4j:5.20.0-enterprise-ubi9`](#neo4j5200-enterprise-ubi9)
-	[`neo4j:5.20.0-ubi8`](#neo4j5200-ubi8)
-	[`neo4j:5.20.0-ubi9`](#neo4j5200-ubi9)
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
$ docker pull neo4j@sha256:96ec50ab72660c8cb117c44618009f29e76c4224da6112b5b95451bbf1e0d251
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:12e568e5ec091c34fd15db01548e579553915582233ff56f6bc123dc1fcb6bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298276114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1164a2171a695250f97d5e376d509c09f100f0d8f2dd1cd5efb10e69b749128d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=18f792e50d6022984ce40012dfe5525a91fca21fa657a84a0a1a0f8d6104cd30 NEO4J_TARBALL=neo4j-community-4.4.34-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b98c91b8b375b048349a88c7779c14b9feb9e75e14dde045600e91028479665`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 145.5 MB (145505174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10768960b67fb0b9629772fe3ac2992a34bc1b3849c0793f50f05b6fe878c4`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6425aeac6be9b91fcd81f727f348579cf5ea7b23ee5542fa1629b83d239b515a`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31276f4b2d5f468d6af6fe9344069181d512dc328c3eecd603c0f0cebb6ff84b`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 121.3 MB (121323583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf29b4f6bd76d9b660b18311759c23da21b9a77bb8eee1377581243812b40683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9607fe398d6a9e54dfae5619f69e5159c98469c0e9ac79eae20df84d6e0a6f2`

```dockerfile
```

-	Layers:
	-	`sha256:5761a1f6066a66c830ba76eafe22f2d56ede939f79b5ed4c60c4ff19e5c170f2`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 2.9 MB (2940153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e5aafeaaf3adf0ef0ff9b466bd679cfa664a345bbd8833f97383fbb859acd1`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 19.5 KB (19536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ff862946f5c18a377d9e3715bb00d5b965f43ec3a07459ff5dbc86f95e0e1bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293691025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b9fc058ee90fd5515284a83061c55fbccfe2ebb845e4f799d734a52a7812cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=18f792e50d6022984ce40012dfe5525a91fca21fa657a84a0a1a0f8d6104cd30 NEO4J_TARBALL=neo4j-community-4.4.34-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b615d2e033765b16f83af4bb16b6c4ab39650e60b28da6210875ae2de4aebb26`  
		Last Modified: Thu, 13 Jun 2024 19:33:35 GMT  
		Size: 142.3 MB (142304113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117386c8b5a998200706cd7d9f157f4807cd12105cc9ff340aa980f654aa29d`  
		Last Modified: Thu, 13 Jun 2024 19:33:27 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e3d7769748d7423b1be785e87c6c730e165d276a9f16a8f9ac402c7959e332`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6051538e3ace4e5a5ac35fe11516d1244ba99cc4c535fc669881dd943cee22`  
		Last Modified: Thu, 13 Jun 2024 19:33:31 GMT  
		Size: 121.3 MB (121286591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:008ec2f1ac1f6ad9d942df62230cd92f34e89a1943f55313523da6fda3a21e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db487364b245683f9e04a95612128edeeaad94b645ed4a931abc0115b35176f`

```dockerfile
```

-	Layers:
	-	`sha256:45724786f87e192bdab87a4150462a4bd9bb8fc725d0c1b500e83727c957ea44`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 2.9 MB (2940416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d4d57236df91204c571d6e11aee3ff18d466c8c395158c232fc58d52e1b329`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 20.1 KB (20089 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:96ec50ab72660c8cb117c44618009f29e76c4224da6112b5b95451bbf1e0d251
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:12e568e5ec091c34fd15db01548e579553915582233ff56f6bc123dc1fcb6bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298276114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1164a2171a695250f97d5e376d509c09f100f0d8f2dd1cd5efb10e69b749128d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=18f792e50d6022984ce40012dfe5525a91fca21fa657a84a0a1a0f8d6104cd30 NEO4J_TARBALL=neo4j-community-4.4.34-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b98c91b8b375b048349a88c7779c14b9feb9e75e14dde045600e91028479665`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 145.5 MB (145505174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10768960b67fb0b9629772fe3ac2992a34bc1b3849c0793f50f05b6fe878c4`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6425aeac6be9b91fcd81f727f348579cf5ea7b23ee5542fa1629b83d239b515a`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31276f4b2d5f468d6af6fe9344069181d512dc328c3eecd603c0f0cebb6ff84b`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 121.3 MB (121323583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf29b4f6bd76d9b660b18311759c23da21b9a77bb8eee1377581243812b40683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9607fe398d6a9e54dfae5619f69e5159c98469c0e9ac79eae20df84d6e0a6f2`

```dockerfile
```

-	Layers:
	-	`sha256:5761a1f6066a66c830ba76eafe22f2d56ede939f79b5ed4c60c4ff19e5c170f2`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 2.9 MB (2940153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e5aafeaaf3adf0ef0ff9b466bd679cfa664a345bbd8833f97383fbb859acd1`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 19.5 KB (19536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ff862946f5c18a377d9e3715bb00d5b965f43ec3a07459ff5dbc86f95e0e1bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293691025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b9fc058ee90fd5515284a83061c55fbccfe2ebb845e4f799d734a52a7812cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=18f792e50d6022984ce40012dfe5525a91fca21fa657a84a0a1a0f8d6104cd30 NEO4J_TARBALL=neo4j-community-4.4.34-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b615d2e033765b16f83af4bb16b6c4ab39650e60b28da6210875ae2de4aebb26`  
		Last Modified: Thu, 13 Jun 2024 19:33:35 GMT  
		Size: 142.3 MB (142304113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117386c8b5a998200706cd7d9f157f4807cd12105cc9ff340aa980f654aa29d`  
		Last Modified: Thu, 13 Jun 2024 19:33:27 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e3d7769748d7423b1be785e87c6c730e165d276a9f16a8f9ac402c7959e332`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6051538e3ace4e5a5ac35fe11516d1244ba99cc4c535fc669881dd943cee22`  
		Last Modified: Thu, 13 Jun 2024 19:33:31 GMT  
		Size: 121.3 MB (121286591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:008ec2f1ac1f6ad9d942df62230cd92f34e89a1943f55313523da6fda3a21e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db487364b245683f9e04a95612128edeeaad94b645ed4a931abc0115b35176f`

```dockerfile
```

-	Layers:
	-	`sha256:45724786f87e192bdab87a4150462a4bd9bb8fc725d0c1b500e83727c957ea44`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 2.9 MB (2940416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d4d57236df91204c571d6e11aee3ff18d466c8c395158c232fc58d52e1b329`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 20.1 KB (20089 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:c1774b03b5c584ac79cdb568ce927d9f9b2d67b289f3f03e07d96afd6c6e6579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:93eb19e297896f09f379f1c6765af58909fe827e799b4ca63d57e6e9e9edcb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (402986458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d963f800bf61e1a71e608ca124d9c80346e6e878b46d6e02735f1ca4e2d96d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb44390774e4107279e9a5d392fd8e59a9413e28efacec845b492d4e4879b6ab NEO4J_TARBALL=neo4j-enterprise-4.4.34-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01c1f6004353f82617fbd9148988d65f3015bd66047fba42f35fff83c18ca5`  
		Last Modified: Thu, 13 Jun 2024 18:29:39 GMT  
		Size: 145.5 MB (145505192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797f1f3d71d460a4064fbd4553ec71fa75d41952ec7579340ae82fe582d2655c`  
		Last Modified: Thu, 13 Jun 2024 18:29:37 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586f7aed5ce5ec4841fcb07e494966b8d020b690717e020045e1f9110cc48437`  
		Last Modified: Thu, 13 Jun 2024 18:29:37 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eefd66418570ab833dc26574c4a4bb60c3526202c89e50aa53512cf02da2da0`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 226.0 MB (226033908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b77420b7c6f22ac67aa556e4f1adf730596ec76d3cf0ea087c27476619b86c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62349069bfa203d3248169ed7f304061f574e332f5428f73ad2e21c146371192`

```dockerfile
```

-	Layers:
	-	`sha256:963502274b85b05f428ea789f8a45bf92db3fc8adde1e912b4dd83469994335a`  
		Last Modified: Thu, 13 Jun 2024 18:29:37 GMT  
		Size: 3.1 MB (3069463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:157eab736fcc01b8c11932e7e1c4582628efd20167de7d74af10a291ddf055bc`  
		Last Modified: Thu, 13 Jun 2024 18:29:37 GMT  
		Size: 19.0 KB (18967 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5e611e35929371296d3c161763a9a3108147a07610a69315d0ef15682796cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398406555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd29109e79ace9e0c0eb66c393b6f35a3e75090467c36ede7101ed7a0bdfdf5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb44390774e4107279e9a5d392fd8e59a9413e28efacec845b492d4e4879b6ab NEO4J_TARBALL=neo4j-enterprise-4.4.34-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b615d2e033765b16f83af4bb16b6c4ab39650e60b28da6210875ae2de4aebb26`  
		Last Modified: Thu, 13 Jun 2024 19:33:35 GMT  
		Size: 142.3 MB (142304113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2518dbc4632f68bebea3045ae322564b33e5455e0561e207f54add40cf76e70c`  
		Last Modified: Thu, 13 Jun 2024 19:34:37 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222b10743b1f86690423f179c280e6e56d50c4c6ba9b4fac8f8685239a584317`  
		Last Modified: Thu, 13 Jun 2024 19:34:37 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbcc56ed38610b8257d4eca1d0ae76b5d20aa4d5894d77cce7afcfff565fc61`  
		Last Modified: Thu, 13 Jun 2024 19:34:42 GMT  
		Size: 226.0 MB (226002120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:367cf6ee8f845893bf04f1fe263fbe404f63f841acd425a6aad7ea64f5210214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7a5c22c2ca8f7e782f83e25f593254e5d440c1f97f5f9d8eaef20860d2ca2c`

```dockerfile
```

-	Layers:
	-	`sha256:054608a062728f054a731d6e99e1eb92bf94e7e2cb50b9450dbefba05e5660e6`  
		Last Modified: Thu, 13 Jun 2024 19:34:37 GMT  
		Size: 3.1 MB (3069702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42291cbe8b84027a14f06b09c2241d76d8350fa4fcc8d9836c1680f8a4b6441`  
		Last Modified: Thu, 13 Jun 2024 19:34:37 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.34`

```console
$ docker pull neo4j@sha256:96ec50ab72660c8cb117c44618009f29e76c4224da6112b5b95451bbf1e0d251
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.34` - linux; amd64

```console
$ docker pull neo4j@sha256:12e568e5ec091c34fd15db01548e579553915582233ff56f6bc123dc1fcb6bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298276114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1164a2171a695250f97d5e376d509c09f100f0d8f2dd1cd5efb10e69b749128d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=18f792e50d6022984ce40012dfe5525a91fca21fa657a84a0a1a0f8d6104cd30 NEO4J_TARBALL=neo4j-community-4.4.34-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b98c91b8b375b048349a88c7779c14b9feb9e75e14dde045600e91028479665`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 145.5 MB (145505174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10768960b67fb0b9629772fe3ac2992a34bc1b3849c0793f50f05b6fe878c4`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6425aeac6be9b91fcd81f727f348579cf5ea7b23ee5542fa1629b83d239b515a`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31276f4b2d5f468d6af6fe9344069181d512dc328c3eecd603c0f0cebb6ff84b`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 121.3 MB (121323583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf29b4f6bd76d9b660b18311759c23da21b9a77bb8eee1377581243812b40683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9607fe398d6a9e54dfae5619f69e5159c98469c0e9ac79eae20df84d6e0a6f2`

```dockerfile
```

-	Layers:
	-	`sha256:5761a1f6066a66c830ba76eafe22f2d56ede939f79b5ed4c60c4ff19e5c170f2`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 2.9 MB (2940153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e5aafeaaf3adf0ef0ff9b466bd679cfa664a345bbd8833f97383fbb859acd1`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 19.5 KB (19536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.34` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ff862946f5c18a377d9e3715bb00d5b965f43ec3a07459ff5dbc86f95e0e1bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293691025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b9fc058ee90fd5515284a83061c55fbccfe2ebb845e4f799d734a52a7812cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=18f792e50d6022984ce40012dfe5525a91fca21fa657a84a0a1a0f8d6104cd30 NEO4J_TARBALL=neo4j-community-4.4.34-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b615d2e033765b16f83af4bb16b6c4ab39650e60b28da6210875ae2de4aebb26`  
		Last Modified: Thu, 13 Jun 2024 19:33:35 GMT  
		Size: 142.3 MB (142304113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117386c8b5a998200706cd7d9f157f4807cd12105cc9ff340aa980f654aa29d`  
		Last Modified: Thu, 13 Jun 2024 19:33:27 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e3d7769748d7423b1be785e87c6c730e165d276a9f16a8f9ac402c7959e332`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6051538e3ace4e5a5ac35fe11516d1244ba99cc4c535fc669881dd943cee22`  
		Last Modified: Thu, 13 Jun 2024 19:33:31 GMT  
		Size: 121.3 MB (121286591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34` - unknown; unknown

```console
$ docker pull neo4j@sha256:008ec2f1ac1f6ad9d942df62230cd92f34e89a1943f55313523da6fda3a21e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db487364b245683f9e04a95612128edeeaad94b645ed4a931abc0115b35176f`

```dockerfile
```

-	Layers:
	-	`sha256:45724786f87e192bdab87a4150462a4bd9bb8fc725d0c1b500e83727c957ea44`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 2.9 MB (2940416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d4d57236df91204c571d6e11aee3ff18d466c8c395158c232fc58d52e1b329`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 20.1 KB (20089 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.34-community`

```console
$ docker pull neo4j@sha256:96ec50ab72660c8cb117c44618009f29e76c4224da6112b5b95451bbf1e0d251
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.34-community` - linux; amd64

```console
$ docker pull neo4j@sha256:12e568e5ec091c34fd15db01548e579553915582233ff56f6bc123dc1fcb6bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298276114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1164a2171a695250f97d5e376d509c09f100f0d8f2dd1cd5efb10e69b749128d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=18f792e50d6022984ce40012dfe5525a91fca21fa657a84a0a1a0f8d6104cd30 NEO4J_TARBALL=neo4j-community-4.4.34-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b98c91b8b375b048349a88c7779c14b9feb9e75e14dde045600e91028479665`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 145.5 MB (145505174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb10768960b67fb0b9629772fe3ac2992a34bc1b3849c0793f50f05b6fe878c4`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6425aeac6be9b91fcd81f727f348579cf5ea7b23ee5542fa1629b83d239b515a`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31276f4b2d5f468d6af6fe9344069181d512dc328c3eecd603c0f0cebb6ff84b`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 121.3 MB (121323583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf29b4f6bd76d9b660b18311759c23da21b9a77bb8eee1377581243812b40683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9607fe398d6a9e54dfae5619f69e5159c98469c0e9ac79eae20df84d6e0a6f2`

```dockerfile
```

-	Layers:
	-	`sha256:5761a1f6066a66c830ba76eafe22f2d56ede939f79b5ed4c60c4ff19e5c170f2`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 2.9 MB (2940153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e5aafeaaf3adf0ef0ff9b466bd679cfa664a345bbd8833f97383fbb859acd1`  
		Last Modified: Thu, 13 Jun 2024 18:29:43 GMT  
		Size: 19.5 KB (19536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.34-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ff862946f5c18a377d9e3715bb00d5b965f43ec3a07459ff5dbc86f95e0e1bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293691025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b9fc058ee90fd5515284a83061c55fbccfe2ebb845e4f799d734a52a7812cd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=18f792e50d6022984ce40012dfe5525a91fca21fa657a84a0a1a0f8d6104cd30 NEO4J_TARBALL=neo4j-community-4.4.34-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b615d2e033765b16f83af4bb16b6c4ab39650e60b28da6210875ae2de4aebb26`  
		Last Modified: Thu, 13 Jun 2024 19:33:35 GMT  
		Size: 142.3 MB (142304113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117386c8b5a998200706cd7d9f157f4807cd12105cc9ff340aa980f654aa29d`  
		Last Modified: Thu, 13 Jun 2024 19:33:27 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e3d7769748d7423b1be785e87c6c730e165d276a9f16a8f9ac402c7959e332`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6051538e3ace4e5a5ac35fe11516d1244ba99cc4c535fc669881dd943cee22`  
		Last Modified: Thu, 13 Jun 2024 19:33:31 GMT  
		Size: 121.3 MB (121286591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:008ec2f1ac1f6ad9d942df62230cd92f34e89a1943f55313523da6fda3a21e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db487364b245683f9e04a95612128edeeaad94b645ed4a931abc0115b35176f`

```dockerfile
```

-	Layers:
	-	`sha256:45724786f87e192bdab87a4150462a4bd9bb8fc725d0c1b500e83727c957ea44`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 2.9 MB (2940416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d4d57236df91204c571d6e11aee3ff18d466c8c395158c232fc58d52e1b329`  
		Last Modified: Thu, 13 Jun 2024 19:33:28 GMT  
		Size: 20.1 KB (20089 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.34-enterprise`

```console
$ docker pull neo4j@sha256:c1774b03b5c584ac79cdb568ce927d9f9b2d67b289f3f03e07d96afd6c6e6579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.34-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:93eb19e297896f09f379f1c6765af58909fe827e799b4ca63d57e6e9e9edcb5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (402986458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d963f800bf61e1a71e608ca124d9c80346e6e878b46d6e02735f1ca4e2d96d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb44390774e4107279e9a5d392fd8e59a9413e28efacec845b492d4e4879b6ab NEO4J_TARBALL=neo4j-enterprise-4.4.34-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b01c1f6004353f82617fbd9148988d65f3015bd66047fba42f35fff83c18ca5`  
		Last Modified: Thu, 13 Jun 2024 18:29:39 GMT  
		Size: 145.5 MB (145505192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797f1f3d71d460a4064fbd4553ec71fa75d41952ec7579340ae82fe582d2655c`  
		Last Modified: Thu, 13 Jun 2024 18:29:37 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586f7aed5ce5ec4841fcb07e494966b8d020b690717e020045e1f9110cc48437`  
		Last Modified: Thu, 13 Jun 2024 18:29:37 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eefd66418570ab833dc26574c4a4bb60c3526202c89e50aa53512cf02da2da0`  
		Last Modified: Thu, 13 Jun 2024 18:29:45 GMT  
		Size: 226.0 MB (226033908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b77420b7c6f22ac67aa556e4f1adf730596ec76d3cf0ea087c27476619b86c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62349069bfa203d3248169ed7f304061f574e332f5428f73ad2e21c146371192`

```dockerfile
```

-	Layers:
	-	`sha256:963502274b85b05f428ea789f8a45bf92db3fc8adde1e912b4dd83469994335a`  
		Last Modified: Thu, 13 Jun 2024 18:29:37 GMT  
		Size: 3.1 MB (3069463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:157eab736fcc01b8c11932e7e1c4582628efd20167de7d74af10a291ddf055bc`  
		Last Modified: Thu, 13 Jun 2024 18:29:37 GMT  
		Size: 19.0 KB (18967 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.34-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5e611e35929371296d3c161763a9a3108147a07610a69315d0ef15682796cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398406555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd29109e79ace9e0c0eb66c393b6f35a3e75090467c36ede7101ed7a0bdfdf5b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 14 May 2024 12:22:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 12:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 12:22:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=cb44390774e4107279e9a5d392fd8e59a9413e28efacec845b492d4e4879b6ab NEO4J_TARBALL=neo4j-enterprise-4.4.34-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 14 May 2024 12:22:43 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 14 May 2024 12:22:43 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.34-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 14 May 2024 12:22:43 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 12:22:43 GMT
WORKDIR /var/lib/neo4j
# Tue, 14 May 2024 12:22:43 GMT
VOLUME [/data /logs]
# Tue, 14 May 2024 12:22:43 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 14 May 2024 12:22:43 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 14 May 2024 12:22:43 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b615d2e033765b16f83af4bb16b6c4ab39650e60b28da6210875ae2de4aebb26`  
		Last Modified: Thu, 13 Jun 2024 19:33:35 GMT  
		Size: 142.3 MB (142304113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2518dbc4632f68bebea3045ae322564b33e5455e0561e207f54add40cf76e70c`  
		Last Modified: Thu, 13 Jun 2024 19:34:37 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222b10743b1f86690423f179c280e6e56d50c4c6ba9b4fac8f8685239a584317`  
		Last Modified: Thu, 13 Jun 2024 19:34:37 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbcc56ed38610b8257d4eca1d0ae76b5d20aa4d5894d77cce7afcfff565fc61`  
		Last Modified: Thu, 13 Jun 2024 19:34:42 GMT  
		Size: 226.0 MB (226002120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:367cf6ee8f845893bf04f1fe263fbe404f63f841acd425a6aad7ea64f5210214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7a5c22c2ca8f7e782f83e25f593254e5d440c1f97f5f9d8eaef20860d2ca2c`

```dockerfile
```

-	Layers:
	-	`sha256:054608a062728f054a731d6e99e1eb92bf94e7e2cb50b9450dbefba05e5660e6`  
		Last Modified: Thu, 13 Jun 2024 19:34:37 GMT  
		Size: 3.1 MB (3069702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42291cbe8b84027a14f06b09c2241d76d8350fa4fcc8d9836c1680f8a4b6441`  
		Last Modified: Thu, 13 Jun 2024 19:34:37 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:8e33d796eb9f2a6a303160c44d541862eeba22687a81e8feda037a917747b666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c67119f30d5c02a61f583f666750e162e41c28c81e0feb04fd04668de753962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318834401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210401846b51433bc4aa55acc910de0bcb4aa20942d5b7d92ebb75cc5676cf0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f332e8cb9c975e78cc0b9ad29cb7f4c8749c838e72d8ccc5e5d17404fecfb`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 153.0 MB (153000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944aee8cc9dac5f0ee64ce41a8d6cc17782fbe671aab4962907d6b2a4e5a7d9e`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cf6c887e111051de71f4a913467e2bd0413354bb0759d13e8f6d7f510d600`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 126.4 MB (126437735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:af6d873a85c169ee64624544ddb31b0ffb44176305ec0e44bb9b4043adb7f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1392bfbbc89674fd1867b33be716d20fd87a0d622c652b73946628eda5c0276`

```dockerfile
```

-	Layers:
	-	`sha256:d8e7b92ac5052d265f290524cb075c23a34e36a7afd9b6ef115ad7c2dec1831a`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 10.3 MB (10309835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277925c58de032f6b19bebbb438481d276993faa9632c4a45cfdc69fe716eb21`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:97015da3955b89f281e46af22b111313fa5f5b55a6a2ddfbf03d058b2e2ca753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e08a24c38b839b2131ec40488146a3d08bbdd33ab2c9d8f123fb7b65dd9330`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf165894ad1ef9493d70620125cd22248290f9e16e92c1fded276d7501d91d6`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 126.4 MB (126437770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca12143b135aa69ddb3a99df1d41f9b64f3ebc13f5d99855d443fedfb51b4363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dabd327c92dbfd7675e367a743c6703c54b0df0a1b2114a2ce7f9182348f47`

```dockerfile
```

-	Layers:
	-	`sha256:150521840ca507febbc31fb4866cd590da4dbc26a209307466c087bc47610b6c`  
		Last Modified: Fri, 07 Jun 2024 06:04:45 GMT  
		Size: 10.3 MB (10307466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645d743a5057e1f257d24f7c9c2ca8db8d9d504044fbeea2c8ba62294a6a2ae8`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 21.9 KB (21878 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:afb1bbdeb147b691bb3b14ebaa14e45ac849a70a642cea4b52572f5eac69a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c4c79286b1288776032350dd23badd3cbdc34216630bd60c49b53bcd6e2118a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290456398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5d0776d61578fdf0770e44afdb54a236464ef5a8367eec4eb79523d51488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce0767c60b019717d362c02999dc97c3e731cd9847a03459eb3b7ec3b39bfc`  
		Last Modified: Thu, 13 Jun 2024 19:11:50 GMT  
		Size: 125.2 MB (125156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc8ba6e6295079c2f178f7455877f49e17a7a1da092b22db158f499c86c31a`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970dcfa4ad5b646e40207fc178d8025b7c08bb30d6a2b250e48f1a113e2ec5f`  
		Last Modified: Thu, 13 Jun 2024 19:11:49 GMT  
		Size: 126.4 MB (126437857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8095026740ade1dd2fd42e3b9351f5e94355c5565aff5ddd53615c1634ff04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b51b0743b342bf10a4dcd1bfe2ef48353eaab55aff6698fa5a0a9ccd0fff6e`

```dockerfile
```

-	Layers:
	-	`sha256:91df6a28513b41acda6c873f3f9bc3b5acacf9006e36ee94786aac3c2a1df430`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 5.0 MB (5048371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518ec33c589dafad3fb099061cf5e706c6a083a170f7839a7f7dd0b627a7cee4`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 21.6 KB (21646 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8cedd6cc1c6168b1aa2273af47d3c4594cc710387595c812061a788f24b4e079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474e8a1b443970c65639279b101cba282007db0c8f320d9d5ee06c7416be8c40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6b80028ce30dd885d9a0c535b5c5da95037e662ce42e36b6cce464f6f8474`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 126.4 MB (126437828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:299e5d05cd789a0c6d66171061dc7b772814830cf5ecdf31ae0f282fa1434d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd782037ab751a316963c63195cecc94397e6b493fcb67401e9f481054e4e41f`

```dockerfile
```

-	Layers:
	-	`sha256:1ec40fc9bdcf2ae5018eeb6a182e97bfddc743d6df1ad0b53d1afa22c7470c1c`  
		Last Modified: Fri, 14 Jun 2024 04:00:14 GMT  
		Size: 5.0 MB (5027707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84095becd03e6aec7616dfa43b8447b1b5756db5145b0c0a1005d13ea067735`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:5b9acd415009c72a907450b25419caff319f398f1195efb70849bf2d8b0101f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5396d211d879bab3304b98645df9f1bdae44c6c09e7a683c5eeabae84e2a04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b423e3650571732ce1b03908a9f3539393d6294493a59376f2b13d1127a1fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c87b552991cf2d5033648ff7ab4db56a9c6727738dfa5d713cff5f2341ce79`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94613cc6429b1d77f6a35329e3955fa9087cb8cc447460b6e9e4bc59b01af945`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a6f8b56be1174d55bb5e2a3226fb20ec06e65f1e8b307909361f716a4f9e9`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a9abda355c801b110ea0264176cbfe13f7e564b9df83036d1a577d1165c49f`  
		Last Modified: Thu, 13 Jun 2024 18:30:47 GMT  
		Size: 378.0 MB (377982656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b204699602d898d428e9adbb8395ddef68bbf29bd44a998d214cf937d3555581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f280ce3e502c89b5efa7a5005fca7b8063ba49c7da23740dd31a6d51e26976`

```dockerfile
```

-	Layers:
	-	`sha256:6919be721a7957ae5bd9ce6a5874df1b984e8e5205a614c88896e9ac0a2a3638`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.1 MB (3133587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d8d4e7dce72ef2ef21c9c7d392ed6ac3392ba6613999a2f1a36ec323a77ee1`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:221e2fa985aa7c4daa776938a5707f9b519331f58a5147f4cd0100c8aba9e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e77d681490d0bf6fe479807c4eb12a7edc384f0475e46f997e159402a2c10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5616767fa4cbc4fc191447cc4c22863cc4dd8a4e39b13f1e37ba7a3ec022c`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabfd6a56d642009d405652fef55bdfe2f376366a74b47c389f0af97a837bcc`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb699162c081b5f3a0b748b57b3f2571201e98bfb7e7879e37efd46f7e34c178`  
		Last Modified: Thu, 13 Jun 2024 19:31:59 GMT  
		Size: 377.9 MB (377944491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:94240005fd042203bbc746549a05636903e78855b79047f22ddf3a8c8f8a006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50263d291ddd0a2f1ea55a611614774a4c413e707c5925492af8393aaee16862`

```dockerfile
```

-	Layers:
	-	`sha256:c3cba07c3ea026b6e1c9f478c73079da7519a5ee4c8d1a0fc63804c9f5c7ee99`  
		Last Modified: Thu, 13 Jun 2024 19:31:52 GMT  
		Size: 3.1 MB (3133898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c6d9124715d26ee27296aa36e91b2c25bfd4fb538561eefd9104246074942`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5b9acd415009c72a907450b25419caff319f398f1195efb70849bf2d8b0101f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5396d211d879bab3304b98645df9f1bdae44c6c09e7a683c5eeabae84e2a04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b423e3650571732ce1b03908a9f3539393d6294493a59376f2b13d1127a1fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c87b552991cf2d5033648ff7ab4db56a9c6727738dfa5d713cff5f2341ce79`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94613cc6429b1d77f6a35329e3955fa9087cb8cc447460b6e9e4bc59b01af945`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a6f8b56be1174d55bb5e2a3226fb20ec06e65f1e8b307909361f716a4f9e9`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a9abda355c801b110ea0264176cbfe13f7e564b9df83036d1a577d1165c49f`  
		Last Modified: Thu, 13 Jun 2024 18:30:47 GMT  
		Size: 378.0 MB (377982656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b204699602d898d428e9adbb8395ddef68bbf29bd44a998d214cf937d3555581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f280ce3e502c89b5efa7a5005fca7b8063ba49c7da23740dd31a6d51e26976`

```dockerfile
```

-	Layers:
	-	`sha256:6919be721a7957ae5bd9ce6a5874df1b984e8e5205a614c88896e9ac0a2a3638`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.1 MB (3133587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d8d4e7dce72ef2ef21c9c7d392ed6ac3392ba6613999a2f1a36ec323a77ee1`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:221e2fa985aa7c4daa776938a5707f9b519331f58a5147f4cd0100c8aba9e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e77d681490d0bf6fe479807c4eb12a7edc384f0475e46f997e159402a2c10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5616767fa4cbc4fc191447cc4c22863cc4dd8a4e39b13f1e37ba7a3ec022c`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabfd6a56d642009d405652fef55bdfe2f376366a74b47c389f0af97a837bcc`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb699162c081b5f3a0b748b57b3f2571201e98bfb7e7879e37efd46f7e34c178`  
		Last Modified: Thu, 13 Jun 2024 19:31:59 GMT  
		Size: 377.9 MB (377944491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:94240005fd042203bbc746549a05636903e78855b79047f22ddf3a8c8f8a006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50263d291ddd0a2f1ea55a611614774a4c413e707c5925492af8393aaee16862`

```dockerfile
```

-	Layers:
	-	`sha256:c3cba07c3ea026b6e1c9f478c73079da7519a5ee4c8d1a0fc63804c9f5c7ee99`  
		Last Modified: Thu, 13 Jun 2024 19:31:52 GMT  
		Size: 3.1 MB (3133898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c6d9124715d26ee27296aa36e91b2c25bfd4fb538561eefd9104246074942`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:ec560a1209bac84f4962e1da1886e321fe5e90d898f42b243e15d63fb550bf69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:d3235a690b5168eea3292c284c1f7cf205f781c5c873a28aad52c1e3de9a1019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.4 MB (567441150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bd110b3b2423808a50813f89b3f6739d506a1a6a1b27f2425fa0b9e484df42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99646ded8c03f270d1a85183a6ae3aa330891d5b30a83f2d04c15bc45d0a0f4b`  
		Last Modified: Fri, 07 Jun 2024 01:03:19 GMT  
		Size: 153.0 MB (153000750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd1a8a74f7a8b13b5c1e76db3878fb62e3b502b880c68cf264c9e45a457ef2`  
		Last Modified: Fri, 07 Jun 2024 01:03:17 GMT  
		Size: 9.7 KB (9723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17941bacb7d38399d0602c33481629a86bfe21d5a8dcabcf0f9874ff408df3e1`  
		Last Modified: Fri, 07 Jun 2024 01:03:23 GMT  
		Size: 375.0 MB (375044302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:288f4e8e59919f60de3133b7bf064b461e1bd604a6da024bd9e3eaabdeafe631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61be33cdb48c332d83e02c62c3bfed94f9e7c81b3dca050462a38929615abff`

```dockerfile
```

-	Layers:
	-	`sha256:77bfdd09262938c1730dc8209b30edd65bac6a34e4aba868f7fce2eafc1e6234`  
		Last Modified: Fri, 07 Jun 2024 01:03:18 GMT  
		Size: 10.5 MB (10481798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb7aa476d803d7556b71961a1a12b1d534a1b005566ac50a682ab556eaa05b2`  
		Last Modified: Fri, 07 Jun 2024 01:03:17 GMT  
		Size: 20.3 KB (20344 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:832d21c6fb6632fdd0f4a56249b9e327d15fb90fd5c049ad344a9a087ddf48e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564343053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432d8222848174efc0784d1c156431ee5950a9f8585a380ef3885c2ca41bb3d2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78caa250005821cfc628fb3cc1aabac5b54a1c1d95a076237921f944aac6fc8f`  
		Last Modified: Fri, 07 Jun 2024 06:05:59 GMT  
		Size: 375.0 MB (375044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2255974210b9ce4e5a1fb0bb957cc6772b1efd13228b4f83ba8eadce41366672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10500033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4454b73bf6210078fdbe29405244d11e774f7d1b92fc1317bcef91981b7564`

```dockerfile
```

-	Layers:
	-	`sha256:996d171da6e7986477546b0b61539b226965ab7be033b82462a0591ea54cb4df`  
		Last Modified: Fri, 07 Jun 2024 06:05:52 GMT  
		Size: 10.5 MB (10479381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3711c9e55b183cdfa13fb16a044417f174410b984f4b7dadbff4316fda1d7a4f`  
		Last Modified: Fri, 07 Jun 2024 06:05:51 GMT  
		Size: 20.7 KB (20652 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:618fd59365c2334709f41c82af22bfe7fd43912539393fe0a0051e0178386796
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ee2195c23aae0548f25df64784c48b833337cc9108c3ebd7234274a6340cbed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.1 MB (539062797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55626e187a4d90fb826fa30334e825248915140d8f416fe0730704c25040bf4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0b1f959d93ed8ecb2ab2ba688344883ab77f9d22d22335ead8bbe02ecbadcd`  
		Last Modified: Thu, 13 Jun 2024 19:12:18 GMT  
		Size: 125.2 MB (125156389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52597a01544c4872598373c3c7615b55958057b5d88ca74baf669f78bcc549c2`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a6e45f4e4d0cc7fbaf0e04c7b831a40ed18d4002ac51eb2daf8389aca8a0a5`  
		Last Modified: Thu, 13 Jun 2024 19:12:23 GMT  
		Size: 375.0 MB (375044516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:9bd09474fef0e70c7be430697e6a2af997d72355febe6c199447186da092608e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910875db9710fb0428ce643eb3e3dca706a9c53aa672e145e3934cf044802ab4`

```dockerfile
```

-	Layers:
	-	`sha256:78d4fddb82bc78c37ad0a18e6aaaefd5130028e25f63639eb6e7c62ef1dab414`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 5.2 MB (5220334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d52bf2abd9bd2bdf100f0bf6ccc6e5d3333aade421f559e0f581c27128234b25`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2109e958524f37692a19328bf7f6731b6c8ca653a3764ad720e296028a46383a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.3 MB (537325860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4890fe09b03e2d35d70258ab21ae94d517a84b032ccd9d21a224203c12991b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2227b7a60ffe9cdc89b296632a7a50c0124d0f82d5db6b094ceda75675cfc384`  
		Last Modified: Fri, 14 Jun 2024 04:01:18 GMT  
		Size: 375.0 MB (375044557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:bfbfcdc86a85d94a7e9fdd364c247197016297f5a693da24d2e0e23835b958a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a5736ffb584bff8359b0bbe0de15187d049bedae87f9c45b6e9ecc075519a5`

```dockerfile
```

-	Layers:
	-	`sha256:490fcb35a4f118b051b881d97f9c70f23c983d0cdc6a8ec8344484882a65b1dd`  
		Last Modified: Fri, 14 Jun 2024 04:01:10 GMT  
		Size: 5.2 MB (5199622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d001066d500c7a1c9f15456b21e57c645f730a65ff09d5e9de20fd9a2ea0126`  
		Last Modified: Fri, 14 Jun 2024 04:01:09 GMT  
		Size: 20.8 KB (20775 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:8e33d796eb9f2a6a303160c44d541862eeba22687a81e8feda037a917747b666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c67119f30d5c02a61f583f666750e162e41c28c81e0feb04fd04668de753962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318834401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210401846b51433bc4aa55acc910de0bcb4aa20942d5b7d92ebb75cc5676cf0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f332e8cb9c975e78cc0b9ad29cb7f4c8749c838e72d8ccc5e5d17404fecfb`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 153.0 MB (153000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944aee8cc9dac5f0ee64ce41a8d6cc17782fbe671aab4962907d6b2a4e5a7d9e`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cf6c887e111051de71f4a913467e2bd0413354bb0759d13e8f6d7f510d600`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 126.4 MB (126437735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:af6d873a85c169ee64624544ddb31b0ffb44176305ec0e44bb9b4043adb7f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1392bfbbc89674fd1867b33be716d20fd87a0d622c652b73946628eda5c0276`

```dockerfile
```

-	Layers:
	-	`sha256:d8e7b92ac5052d265f290524cb075c23a34e36a7afd9b6ef115ad7c2dec1831a`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 10.3 MB (10309835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277925c58de032f6b19bebbb438481d276993faa9632c4a45cfdc69fe716eb21`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:97015da3955b89f281e46af22b111313fa5f5b55a6a2ddfbf03d058b2e2ca753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e08a24c38b839b2131ec40488146a3d08bbdd33ab2c9d8f123fb7b65dd9330`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf165894ad1ef9493d70620125cd22248290f9e16e92c1fded276d7501d91d6`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 126.4 MB (126437770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca12143b135aa69ddb3a99df1d41f9b64f3ebc13f5d99855d443fedfb51b4363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dabd327c92dbfd7675e367a743c6703c54b0df0a1b2114a2ce7f9182348f47`

```dockerfile
```

-	Layers:
	-	`sha256:150521840ca507febbc31fb4866cd590da4dbc26a209307466c087bc47610b6c`  
		Last Modified: Fri, 07 Jun 2024 06:04:45 GMT  
		Size: 10.3 MB (10307466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645d743a5057e1f257d24f7c9c2ca8db8d9d504044fbeea2c8ba62294a6a2ae8`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 21.9 KB (21878 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:afb1bbdeb147b691bb3b14ebaa14e45ac849a70a642cea4b52572f5eac69a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c4c79286b1288776032350dd23badd3cbdc34216630bd60c49b53bcd6e2118a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290456398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5d0776d61578fdf0770e44afdb54a236464ef5a8367eec4eb79523d51488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce0767c60b019717d362c02999dc97c3e731cd9847a03459eb3b7ec3b39bfc`  
		Last Modified: Thu, 13 Jun 2024 19:11:50 GMT  
		Size: 125.2 MB (125156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc8ba6e6295079c2f178f7455877f49e17a7a1da092b22db158f499c86c31a`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970dcfa4ad5b646e40207fc178d8025b7c08bb30d6a2b250e48f1a113e2ec5f`  
		Last Modified: Thu, 13 Jun 2024 19:11:49 GMT  
		Size: 126.4 MB (126437857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8095026740ade1dd2fd42e3b9351f5e94355c5565aff5ddd53615c1634ff04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b51b0743b342bf10a4dcd1bfe2ef48353eaab55aff6698fa5a0a9ccd0fff6e`

```dockerfile
```

-	Layers:
	-	`sha256:91df6a28513b41acda6c873f3f9bc3b5acacf9006e36ee94786aac3c2a1df430`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 5.0 MB (5048371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518ec33c589dafad3fb099061cf5e706c6a083a170f7839a7f7dd0b627a7cee4`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 21.6 KB (21646 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8cedd6cc1c6168b1aa2273af47d3c4594cc710387595c812061a788f24b4e079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474e8a1b443970c65639279b101cba282007db0c8f320d9d5ee06c7416be8c40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6b80028ce30dd885d9a0c535b5c5da95037e662ce42e36b6cce464f6f8474`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 126.4 MB (126437828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:299e5d05cd789a0c6d66171061dc7b772814830cf5ecdf31ae0f282fa1434d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd782037ab751a316963c63195cecc94397e6b493fcb67401e9f481054e4e41f`

```dockerfile
```

-	Layers:
	-	`sha256:1ec40fc9bdcf2ae5018eeb6a182e97bfddc743d6df1ad0b53d1afa22c7470c1c`  
		Last Modified: Fri, 14 Jun 2024 04:00:14 GMT  
		Size: 5.0 MB (5027707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84095becd03e6aec7616dfa43b8447b1b5756db5145b0c0a1005d13ea067735`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-bullseye`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-community`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-community` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-community-bullseye`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-community-ubi8`

```console
$ docker pull neo4j@sha256:8e33d796eb9f2a6a303160c44d541862eeba22687a81e8feda037a917747b666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c67119f30d5c02a61f583f666750e162e41c28c81e0feb04fd04668de753962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318834401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210401846b51433bc4aa55acc910de0bcb4aa20942d5b7d92ebb75cc5676cf0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f332e8cb9c975e78cc0b9ad29cb7f4c8749c838e72d8ccc5e5d17404fecfb`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 153.0 MB (153000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944aee8cc9dac5f0ee64ce41a8d6cc17782fbe671aab4962907d6b2a4e5a7d9e`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cf6c887e111051de71f4a913467e2bd0413354bb0759d13e8f6d7f510d600`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 126.4 MB (126437735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:af6d873a85c169ee64624544ddb31b0ffb44176305ec0e44bb9b4043adb7f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1392bfbbc89674fd1867b33be716d20fd87a0d622c652b73946628eda5c0276`

```dockerfile
```

-	Layers:
	-	`sha256:d8e7b92ac5052d265f290524cb075c23a34e36a7afd9b6ef115ad7c2dec1831a`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 10.3 MB (10309835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277925c58de032f6b19bebbb438481d276993faa9632c4a45cfdc69fe716eb21`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:97015da3955b89f281e46af22b111313fa5f5b55a6a2ddfbf03d058b2e2ca753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e08a24c38b839b2131ec40488146a3d08bbdd33ab2c9d8f123fb7b65dd9330`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf165894ad1ef9493d70620125cd22248290f9e16e92c1fded276d7501d91d6`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 126.4 MB (126437770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca12143b135aa69ddb3a99df1d41f9b64f3ebc13f5d99855d443fedfb51b4363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dabd327c92dbfd7675e367a743c6703c54b0df0a1b2114a2ce7f9182348f47`

```dockerfile
```

-	Layers:
	-	`sha256:150521840ca507febbc31fb4866cd590da4dbc26a209307466c087bc47610b6c`  
		Last Modified: Fri, 07 Jun 2024 06:04:45 GMT  
		Size: 10.3 MB (10307466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645d743a5057e1f257d24f7c9c2ca8db8d9d504044fbeea2c8ba62294a6a2ae8`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 21.9 KB (21878 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-community-ubi9`

```console
$ docker pull neo4j@sha256:afb1bbdeb147b691bb3b14ebaa14e45ac849a70a642cea4b52572f5eac69a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c4c79286b1288776032350dd23badd3cbdc34216630bd60c49b53bcd6e2118a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290456398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5d0776d61578fdf0770e44afdb54a236464ef5a8367eec4eb79523d51488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce0767c60b019717d362c02999dc97c3e731cd9847a03459eb3b7ec3b39bfc`  
		Last Modified: Thu, 13 Jun 2024 19:11:50 GMT  
		Size: 125.2 MB (125156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc8ba6e6295079c2f178f7455877f49e17a7a1da092b22db158f499c86c31a`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970dcfa4ad5b646e40207fc178d8025b7c08bb30d6a2b250e48f1a113e2ec5f`  
		Last Modified: Thu, 13 Jun 2024 19:11:49 GMT  
		Size: 126.4 MB (126437857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8095026740ade1dd2fd42e3b9351f5e94355c5565aff5ddd53615c1634ff04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b51b0743b342bf10a4dcd1bfe2ef48353eaab55aff6698fa5a0a9ccd0fff6e`

```dockerfile
```

-	Layers:
	-	`sha256:91df6a28513b41acda6c873f3f9bc3b5acacf9006e36ee94786aac3c2a1df430`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 5.0 MB (5048371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518ec33c589dafad3fb099061cf5e706c6a083a170f7839a7f7dd0b627a7cee4`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 21.6 KB (21646 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8cedd6cc1c6168b1aa2273af47d3c4594cc710387595c812061a788f24b4e079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474e8a1b443970c65639279b101cba282007db0c8f320d9d5ee06c7416be8c40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6b80028ce30dd885d9a0c535b5c5da95037e662ce42e36b6cce464f6f8474`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 126.4 MB (126437828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:299e5d05cd789a0c6d66171061dc7b772814830cf5ecdf31ae0f282fa1434d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd782037ab751a316963c63195cecc94397e6b493fcb67401e9f481054e4e41f`

```dockerfile
```

-	Layers:
	-	`sha256:1ec40fc9bdcf2ae5018eeb6a182e97bfddc743d6df1ad0b53d1afa22c7470c1c`  
		Last Modified: Fri, 14 Jun 2024 04:00:14 GMT  
		Size: 5.0 MB (5027707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84095becd03e6aec7616dfa43b8447b1b5756db5145b0c0a1005d13ea067735`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-enterprise`

```console
$ docker pull neo4j@sha256:5b9acd415009c72a907450b25419caff319f398f1195efb70849bf2d8b0101f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5396d211d879bab3304b98645df9f1bdae44c6c09e7a683c5eeabae84e2a04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b423e3650571732ce1b03908a9f3539393d6294493a59376f2b13d1127a1fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c87b552991cf2d5033648ff7ab4db56a9c6727738dfa5d713cff5f2341ce79`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94613cc6429b1d77f6a35329e3955fa9087cb8cc447460b6e9e4bc59b01af945`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a6f8b56be1174d55bb5e2a3226fb20ec06e65f1e8b307909361f716a4f9e9`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a9abda355c801b110ea0264176cbfe13f7e564b9df83036d1a577d1165c49f`  
		Last Modified: Thu, 13 Jun 2024 18:30:47 GMT  
		Size: 378.0 MB (377982656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b204699602d898d428e9adbb8395ddef68bbf29bd44a998d214cf937d3555581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f280ce3e502c89b5efa7a5005fca7b8063ba49c7da23740dd31a6d51e26976`

```dockerfile
```

-	Layers:
	-	`sha256:6919be721a7957ae5bd9ce6a5874df1b984e8e5205a614c88896e9ac0a2a3638`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.1 MB (3133587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d8d4e7dce72ef2ef21c9c7d392ed6ac3392ba6613999a2f1a36ec323a77ee1`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:221e2fa985aa7c4daa776938a5707f9b519331f58a5147f4cd0100c8aba9e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e77d681490d0bf6fe479807c4eb12a7edc384f0475e46f997e159402a2c10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5616767fa4cbc4fc191447cc4c22863cc4dd8a4e39b13f1e37ba7a3ec022c`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabfd6a56d642009d405652fef55bdfe2f376366a74b47c389f0af97a837bcc`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb699162c081b5f3a0b748b57b3f2571201e98bfb7e7879e37efd46f7e34c178`  
		Last Modified: Thu, 13 Jun 2024 19:31:59 GMT  
		Size: 377.9 MB (377944491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:94240005fd042203bbc746549a05636903e78855b79047f22ddf3a8c8f8a006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50263d291ddd0a2f1ea55a611614774a4c413e707c5925492af8393aaee16862`

```dockerfile
```

-	Layers:
	-	`sha256:c3cba07c3ea026b6e1c9f478c73079da7519a5ee4c8d1a0fc63804c9f5c7ee99`  
		Last Modified: Thu, 13 Jun 2024 19:31:52 GMT  
		Size: 3.1 MB (3133898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c6d9124715d26ee27296aa36e91b2c25bfd4fb538561eefd9104246074942`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5b9acd415009c72a907450b25419caff319f398f1195efb70849bf2d8b0101f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5396d211d879bab3304b98645df9f1bdae44c6c09e7a683c5eeabae84e2a04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b423e3650571732ce1b03908a9f3539393d6294493a59376f2b13d1127a1fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c87b552991cf2d5033648ff7ab4db56a9c6727738dfa5d713cff5f2341ce79`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94613cc6429b1d77f6a35329e3955fa9087cb8cc447460b6e9e4bc59b01af945`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a6f8b56be1174d55bb5e2a3226fb20ec06e65f1e8b307909361f716a4f9e9`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a9abda355c801b110ea0264176cbfe13f7e564b9df83036d1a577d1165c49f`  
		Last Modified: Thu, 13 Jun 2024 18:30:47 GMT  
		Size: 378.0 MB (377982656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b204699602d898d428e9adbb8395ddef68bbf29bd44a998d214cf937d3555581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f280ce3e502c89b5efa7a5005fca7b8063ba49c7da23740dd31a6d51e26976`

```dockerfile
```

-	Layers:
	-	`sha256:6919be721a7957ae5bd9ce6a5874df1b984e8e5205a614c88896e9ac0a2a3638`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.1 MB (3133587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d8d4e7dce72ef2ef21c9c7d392ed6ac3392ba6613999a2f1a36ec323a77ee1`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:221e2fa985aa7c4daa776938a5707f9b519331f58a5147f4cd0100c8aba9e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e77d681490d0bf6fe479807c4eb12a7edc384f0475e46f997e159402a2c10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5616767fa4cbc4fc191447cc4c22863cc4dd8a4e39b13f1e37ba7a3ec022c`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabfd6a56d642009d405652fef55bdfe2f376366a74b47c389f0af97a837bcc`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb699162c081b5f3a0b748b57b3f2571201e98bfb7e7879e37efd46f7e34c178`  
		Last Modified: Thu, 13 Jun 2024 19:31:59 GMT  
		Size: 377.9 MB (377944491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:94240005fd042203bbc746549a05636903e78855b79047f22ddf3a8c8f8a006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50263d291ddd0a2f1ea55a611614774a4c413e707c5925492af8393aaee16862`

```dockerfile
```

-	Layers:
	-	`sha256:c3cba07c3ea026b6e1c9f478c73079da7519a5ee4c8d1a0fc63804c9f5c7ee99`  
		Last Modified: Thu, 13 Jun 2024 19:31:52 GMT  
		Size: 3.1 MB (3133898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c6d9124715d26ee27296aa36e91b2c25bfd4fb538561eefd9104246074942`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:ec560a1209bac84f4962e1da1886e321fe5e90d898f42b243e15d63fb550bf69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:d3235a690b5168eea3292c284c1f7cf205f781c5c873a28aad52c1e3de9a1019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.4 MB (567441150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bd110b3b2423808a50813f89b3f6739d506a1a6a1b27f2425fa0b9e484df42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99646ded8c03f270d1a85183a6ae3aa330891d5b30a83f2d04c15bc45d0a0f4b`  
		Last Modified: Fri, 07 Jun 2024 01:03:19 GMT  
		Size: 153.0 MB (153000750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd1a8a74f7a8b13b5c1e76db3878fb62e3b502b880c68cf264c9e45a457ef2`  
		Last Modified: Fri, 07 Jun 2024 01:03:17 GMT  
		Size: 9.7 KB (9723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17941bacb7d38399d0602c33481629a86bfe21d5a8dcabcf0f9874ff408df3e1`  
		Last Modified: Fri, 07 Jun 2024 01:03:23 GMT  
		Size: 375.0 MB (375044302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:288f4e8e59919f60de3133b7bf064b461e1bd604a6da024bd9e3eaabdeafe631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61be33cdb48c332d83e02c62c3bfed94f9e7c81b3dca050462a38929615abff`

```dockerfile
```

-	Layers:
	-	`sha256:77bfdd09262938c1730dc8209b30edd65bac6a34e4aba868f7fce2eafc1e6234`  
		Last Modified: Fri, 07 Jun 2024 01:03:18 GMT  
		Size: 10.5 MB (10481798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb7aa476d803d7556b71961a1a12b1d534a1b005566ac50a682ab556eaa05b2`  
		Last Modified: Fri, 07 Jun 2024 01:03:17 GMT  
		Size: 20.3 KB (20344 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:832d21c6fb6632fdd0f4a56249b9e327d15fb90fd5c049ad344a9a087ddf48e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564343053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432d8222848174efc0784d1c156431ee5950a9f8585a380ef3885c2ca41bb3d2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78caa250005821cfc628fb3cc1aabac5b54a1c1d95a076237921f944aac6fc8f`  
		Last Modified: Fri, 07 Jun 2024 06:05:59 GMT  
		Size: 375.0 MB (375044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2255974210b9ce4e5a1fb0bb957cc6772b1efd13228b4f83ba8eadce41366672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10500033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4454b73bf6210078fdbe29405244d11e774f7d1b92fc1317bcef91981b7564`

```dockerfile
```

-	Layers:
	-	`sha256:996d171da6e7986477546b0b61539b226965ab7be033b82462a0591ea54cb4df`  
		Last Modified: Fri, 07 Jun 2024 06:05:52 GMT  
		Size: 10.5 MB (10479381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3711c9e55b183cdfa13fb16a044417f174410b984f4b7dadbff4316fda1d7a4f`  
		Last Modified: Fri, 07 Jun 2024 06:05:51 GMT  
		Size: 20.7 KB (20652 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:618fd59365c2334709f41c82af22bfe7fd43912539393fe0a0051e0178386796
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ee2195c23aae0548f25df64784c48b833337cc9108c3ebd7234274a6340cbed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.1 MB (539062797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55626e187a4d90fb826fa30334e825248915140d8f416fe0730704c25040bf4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0b1f959d93ed8ecb2ab2ba688344883ab77f9d22d22335ead8bbe02ecbadcd`  
		Last Modified: Thu, 13 Jun 2024 19:12:18 GMT  
		Size: 125.2 MB (125156389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52597a01544c4872598373c3c7615b55958057b5d88ca74baf669f78bcc549c2`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a6e45f4e4d0cc7fbaf0e04c7b831a40ed18d4002ac51eb2daf8389aca8a0a5`  
		Last Modified: Thu, 13 Jun 2024 19:12:23 GMT  
		Size: 375.0 MB (375044516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:9bd09474fef0e70c7be430697e6a2af997d72355febe6c199447186da092608e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910875db9710fb0428ce643eb3e3dca706a9c53aa672e145e3934cf044802ab4`

```dockerfile
```

-	Layers:
	-	`sha256:78d4fddb82bc78c37ad0a18e6aaaefd5130028e25f63639eb6e7c62ef1dab414`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 5.2 MB (5220334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d52bf2abd9bd2bdf100f0bf6ccc6e5d3333aade421f559e0f581c27128234b25`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2109e958524f37692a19328bf7f6731b6c8ca653a3764ad720e296028a46383a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.3 MB (537325860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4890fe09b03e2d35d70258ab21ae94d517a84b032ccd9d21a224203c12991b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2227b7a60ffe9cdc89b296632a7a50c0124d0f82d5db6b094ceda75675cfc384`  
		Last Modified: Fri, 14 Jun 2024 04:01:18 GMT  
		Size: 375.0 MB (375044557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:bfbfcdc86a85d94a7e9fdd364c247197016297f5a693da24d2e0e23835b958a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a5736ffb584bff8359b0bbe0de15187d049bedae87f9c45b6e9ecc075519a5`

```dockerfile
```

-	Layers:
	-	`sha256:490fcb35a4f118b051b881d97f9c70f23c983d0cdc6a8ec8344484882a65b1dd`  
		Last Modified: Fri, 14 Jun 2024 04:01:10 GMT  
		Size: 5.2 MB (5199622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d001066d500c7a1c9f15456b21e57c645f730a65ff09d5e9de20fd9a2ea0126`  
		Last Modified: Fri, 14 Jun 2024 04:01:09 GMT  
		Size: 20.8 KB (20775 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-ubi8`

```console
$ docker pull neo4j@sha256:8e33d796eb9f2a6a303160c44d541862eeba22687a81e8feda037a917747b666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c67119f30d5c02a61f583f666750e162e41c28c81e0feb04fd04668de753962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318834401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210401846b51433bc4aa55acc910de0bcb4aa20942d5b7d92ebb75cc5676cf0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f332e8cb9c975e78cc0b9ad29cb7f4c8749c838e72d8ccc5e5d17404fecfb`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 153.0 MB (153000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944aee8cc9dac5f0ee64ce41a8d6cc17782fbe671aab4962907d6b2a4e5a7d9e`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cf6c887e111051de71f4a913467e2bd0413354bb0759d13e8f6d7f510d600`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 126.4 MB (126437735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:af6d873a85c169ee64624544ddb31b0ffb44176305ec0e44bb9b4043adb7f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1392bfbbc89674fd1867b33be716d20fd87a0d622c652b73946628eda5c0276`

```dockerfile
```

-	Layers:
	-	`sha256:d8e7b92ac5052d265f290524cb075c23a34e36a7afd9b6ef115ad7c2dec1831a`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 10.3 MB (10309835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277925c58de032f6b19bebbb438481d276993faa9632c4a45cfdc69fe716eb21`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:97015da3955b89f281e46af22b111313fa5f5b55a6a2ddfbf03d058b2e2ca753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e08a24c38b839b2131ec40488146a3d08bbdd33ab2c9d8f123fb7b65dd9330`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf165894ad1ef9493d70620125cd22248290f9e16e92c1fded276d7501d91d6`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 126.4 MB (126437770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca12143b135aa69ddb3a99df1d41f9b64f3ebc13f5d99855d443fedfb51b4363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dabd327c92dbfd7675e367a743c6703c54b0df0a1b2114a2ce7f9182348f47`

```dockerfile
```

-	Layers:
	-	`sha256:150521840ca507febbc31fb4866cd590da4dbc26a209307466c087bc47610b6c`  
		Last Modified: Fri, 07 Jun 2024 06:04:45 GMT  
		Size: 10.3 MB (10307466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645d743a5057e1f257d24f7c9c2ca8db8d9d504044fbeea2c8ba62294a6a2ae8`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 21.9 KB (21878 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-ubi9`

```console
$ docker pull neo4j@sha256:afb1bbdeb147b691bb3b14ebaa14e45ac849a70a642cea4b52572f5eac69a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c4c79286b1288776032350dd23badd3cbdc34216630bd60c49b53bcd6e2118a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290456398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5d0776d61578fdf0770e44afdb54a236464ef5a8367eec4eb79523d51488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce0767c60b019717d362c02999dc97c3e731cd9847a03459eb3b7ec3b39bfc`  
		Last Modified: Thu, 13 Jun 2024 19:11:50 GMT  
		Size: 125.2 MB (125156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc8ba6e6295079c2f178f7455877f49e17a7a1da092b22db158f499c86c31a`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970dcfa4ad5b646e40207fc178d8025b7c08bb30d6a2b250e48f1a113e2ec5f`  
		Last Modified: Thu, 13 Jun 2024 19:11:49 GMT  
		Size: 126.4 MB (126437857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8095026740ade1dd2fd42e3b9351f5e94355c5565aff5ddd53615c1634ff04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b51b0743b342bf10a4dcd1bfe2ef48353eaab55aff6698fa5a0a9ccd0fff6e`

```dockerfile
```

-	Layers:
	-	`sha256:91df6a28513b41acda6c873f3f9bc3b5acacf9006e36ee94786aac3c2a1df430`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 5.0 MB (5048371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518ec33c589dafad3fb099061cf5e706c6a083a170f7839a7f7dd0b627a7cee4`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 21.6 KB (21646 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8cedd6cc1c6168b1aa2273af47d3c4594cc710387595c812061a788f24b4e079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474e8a1b443970c65639279b101cba282007db0c8f320d9d5ee06c7416be8c40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6b80028ce30dd885d9a0c535b5c5da95037e662ce42e36b6cce464f6f8474`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 126.4 MB (126437828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:299e5d05cd789a0c6d66171061dc7b772814830cf5ecdf31ae0f282fa1434d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd782037ab751a316963c63195cecc94397e6b493fcb67401e9f481054e4e41f`

```dockerfile
```

-	Layers:
	-	`sha256:1ec40fc9bdcf2ae5018eeb6a182e97bfddc743d6df1ad0b53d1afa22c7470c1c`  
		Last Modified: Fri, 14 Jun 2024 04:00:14 GMT  
		Size: 5.0 MB (5027707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84095becd03e6aec7616dfa43b8447b1b5756db5145b0c0a1005d13ea067735`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-bullseye`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-community`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-community-bullseye`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-community-ubi8`

```console
$ docker pull neo4j@sha256:8e33d796eb9f2a6a303160c44d541862eeba22687a81e8feda037a917747b666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c67119f30d5c02a61f583f666750e162e41c28c81e0feb04fd04668de753962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318834401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210401846b51433bc4aa55acc910de0bcb4aa20942d5b7d92ebb75cc5676cf0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f332e8cb9c975e78cc0b9ad29cb7f4c8749c838e72d8ccc5e5d17404fecfb`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 153.0 MB (153000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944aee8cc9dac5f0ee64ce41a8d6cc17782fbe671aab4962907d6b2a4e5a7d9e`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cf6c887e111051de71f4a913467e2bd0413354bb0759d13e8f6d7f510d600`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 126.4 MB (126437735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:af6d873a85c169ee64624544ddb31b0ffb44176305ec0e44bb9b4043adb7f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1392bfbbc89674fd1867b33be716d20fd87a0d622c652b73946628eda5c0276`

```dockerfile
```

-	Layers:
	-	`sha256:d8e7b92ac5052d265f290524cb075c23a34e36a7afd9b6ef115ad7c2dec1831a`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 10.3 MB (10309835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277925c58de032f6b19bebbb438481d276993faa9632c4a45cfdc69fe716eb21`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:97015da3955b89f281e46af22b111313fa5f5b55a6a2ddfbf03d058b2e2ca753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e08a24c38b839b2131ec40488146a3d08bbdd33ab2c9d8f123fb7b65dd9330`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf165894ad1ef9493d70620125cd22248290f9e16e92c1fded276d7501d91d6`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 126.4 MB (126437770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca12143b135aa69ddb3a99df1d41f9b64f3ebc13f5d99855d443fedfb51b4363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dabd327c92dbfd7675e367a743c6703c54b0df0a1b2114a2ce7f9182348f47`

```dockerfile
```

-	Layers:
	-	`sha256:150521840ca507febbc31fb4866cd590da4dbc26a209307466c087bc47610b6c`  
		Last Modified: Fri, 07 Jun 2024 06:04:45 GMT  
		Size: 10.3 MB (10307466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645d743a5057e1f257d24f7c9c2ca8db8d9d504044fbeea2c8ba62294a6a2ae8`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 21.9 KB (21878 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-community-ubi9`

```console
$ docker pull neo4j@sha256:afb1bbdeb147b691bb3b14ebaa14e45ac849a70a642cea4b52572f5eac69a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c4c79286b1288776032350dd23badd3cbdc34216630bd60c49b53bcd6e2118a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290456398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5d0776d61578fdf0770e44afdb54a236464ef5a8367eec4eb79523d51488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce0767c60b019717d362c02999dc97c3e731cd9847a03459eb3b7ec3b39bfc`  
		Last Modified: Thu, 13 Jun 2024 19:11:50 GMT  
		Size: 125.2 MB (125156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc8ba6e6295079c2f178f7455877f49e17a7a1da092b22db158f499c86c31a`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970dcfa4ad5b646e40207fc178d8025b7c08bb30d6a2b250e48f1a113e2ec5f`  
		Last Modified: Thu, 13 Jun 2024 19:11:49 GMT  
		Size: 126.4 MB (126437857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8095026740ade1dd2fd42e3b9351f5e94355c5565aff5ddd53615c1634ff04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b51b0743b342bf10a4dcd1bfe2ef48353eaab55aff6698fa5a0a9ccd0fff6e`

```dockerfile
```

-	Layers:
	-	`sha256:91df6a28513b41acda6c873f3f9bc3b5acacf9006e36ee94786aac3c2a1df430`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 5.0 MB (5048371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518ec33c589dafad3fb099061cf5e706c6a083a170f7839a7f7dd0b627a7cee4`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 21.6 KB (21646 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8cedd6cc1c6168b1aa2273af47d3c4594cc710387595c812061a788f24b4e079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474e8a1b443970c65639279b101cba282007db0c8f320d9d5ee06c7416be8c40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6b80028ce30dd885d9a0c535b5c5da95037e662ce42e36b6cce464f6f8474`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 126.4 MB (126437828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:299e5d05cd789a0c6d66171061dc7b772814830cf5ecdf31ae0f282fa1434d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd782037ab751a316963c63195cecc94397e6b493fcb67401e9f481054e4e41f`

```dockerfile
```

-	Layers:
	-	`sha256:1ec40fc9bdcf2ae5018eeb6a182e97bfddc743d6df1ad0b53d1afa22c7470c1c`  
		Last Modified: Fri, 14 Jun 2024 04:00:14 GMT  
		Size: 5.0 MB (5027707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84095becd03e6aec7616dfa43b8447b1b5756db5145b0c0a1005d13ea067735`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-enterprise`

```console
$ docker pull neo4j@sha256:5b9acd415009c72a907450b25419caff319f398f1195efb70849bf2d8b0101f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5396d211d879bab3304b98645df9f1bdae44c6c09e7a683c5eeabae84e2a04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b423e3650571732ce1b03908a9f3539393d6294493a59376f2b13d1127a1fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c87b552991cf2d5033648ff7ab4db56a9c6727738dfa5d713cff5f2341ce79`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94613cc6429b1d77f6a35329e3955fa9087cb8cc447460b6e9e4bc59b01af945`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a6f8b56be1174d55bb5e2a3226fb20ec06e65f1e8b307909361f716a4f9e9`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a9abda355c801b110ea0264176cbfe13f7e564b9df83036d1a577d1165c49f`  
		Last Modified: Thu, 13 Jun 2024 18:30:47 GMT  
		Size: 378.0 MB (377982656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b204699602d898d428e9adbb8395ddef68bbf29bd44a998d214cf937d3555581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f280ce3e502c89b5efa7a5005fca7b8063ba49c7da23740dd31a6d51e26976`

```dockerfile
```

-	Layers:
	-	`sha256:6919be721a7957ae5bd9ce6a5874df1b984e8e5205a614c88896e9ac0a2a3638`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.1 MB (3133587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d8d4e7dce72ef2ef21c9c7d392ed6ac3392ba6613999a2f1a36ec323a77ee1`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:221e2fa985aa7c4daa776938a5707f9b519331f58a5147f4cd0100c8aba9e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e77d681490d0bf6fe479807c4eb12a7edc384f0475e46f997e159402a2c10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5616767fa4cbc4fc191447cc4c22863cc4dd8a4e39b13f1e37ba7a3ec022c`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabfd6a56d642009d405652fef55bdfe2f376366a74b47c389f0af97a837bcc`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb699162c081b5f3a0b748b57b3f2571201e98bfb7e7879e37efd46f7e34c178`  
		Last Modified: Thu, 13 Jun 2024 19:31:59 GMT  
		Size: 377.9 MB (377944491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:94240005fd042203bbc746549a05636903e78855b79047f22ddf3a8c8f8a006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50263d291ddd0a2f1ea55a611614774a4c413e707c5925492af8393aaee16862`

```dockerfile
```

-	Layers:
	-	`sha256:c3cba07c3ea026b6e1c9f478c73079da7519a5ee4c8d1a0fc63804c9f5c7ee99`  
		Last Modified: Thu, 13 Jun 2024 19:31:52 GMT  
		Size: 3.1 MB (3133898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c6d9124715d26ee27296aa36e91b2c25bfd4fb538561eefd9104246074942`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5b9acd415009c72a907450b25419caff319f398f1195efb70849bf2d8b0101f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5396d211d879bab3304b98645df9f1bdae44c6c09e7a683c5eeabae84e2a04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b423e3650571732ce1b03908a9f3539393d6294493a59376f2b13d1127a1fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c87b552991cf2d5033648ff7ab4db56a9c6727738dfa5d713cff5f2341ce79`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94613cc6429b1d77f6a35329e3955fa9087cb8cc447460b6e9e4bc59b01af945`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a6f8b56be1174d55bb5e2a3226fb20ec06e65f1e8b307909361f716a4f9e9`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a9abda355c801b110ea0264176cbfe13f7e564b9df83036d1a577d1165c49f`  
		Last Modified: Thu, 13 Jun 2024 18:30:47 GMT  
		Size: 378.0 MB (377982656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b204699602d898d428e9adbb8395ddef68bbf29bd44a998d214cf937d3555581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f280ce3e502c89b5efa7a5005fca7b8063ba49c7da23740dd31a6d51e26976`

```dockerfile
```

-	Layers:
	-	`sha256:6919be721a7957ae5bd9ce6a5874df1b984e8e5205a614c88896e9ac0a2a3638`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.1 MB (3133587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d8d4e7dce72ef2ef21c9c7d392ed6ac3392ba6613999a2f1a36ec323a77ee1`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:221e2fa985aa7c4daa776938a5707f9b519331f58a5147f4cd0100c8aba9e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e77d681490d0bf6fe479807c4eb12a7edc384f0475e46f997e159402a2c10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5616767fa4cbc4fc191447cc4c22863cc4dd8a4e39b13f1e37ba7a3ec022c`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabfd6a56d642009d405652fef55bdfe2f376366a74b47c389f0af97a837bcc`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb699162c081b5f3a0b748b57b3f2571201e98bfb7e7879e37efd46f7e34c178`  
		Last Modified: Thu, 13 Jun 2024 19:31:59 GMT  
		Size: 377.9 MB (377944491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:94240005fd042203bbc746549a05636903e78855b79047f22ddf3a8c8f8a006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50263d291ddd0a2f1ea55a611614774a4c413e707c5925492af8393aaee16862`

```dockerfile
```

-	Layers:
	-	`sha256:c3cba07c3ea026b6e1c9f478c73079da7519a5ee4c8d1a0fc63804c9f5c7ee99`  
		Last Modified: Thu, 13 Jun 2024 19:31:52 GMT  
		Size: 3.1 MB (3133898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c6d9124715d26ee27296aa36e91b2c25bfd4fb538561eefd9104246074942`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:ec560a1209bac84f4962e1da1886e321fe5e90d898f42b243e15d63fb550bf69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:d3235a690b5168eea3292c284c1f7cf205f781c5c873a28aad52c1e3de9a1019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.4 MB (567441150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bd110b3b2423808a50813f89b3f6739d506a1a6a1b27f2425fa0b9e484df42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99646ded8c03f270d1a85183a6ae3aa330891d5b30a83f2d04c15bc45d0a0f4b`  
		Last Modified: Fri, 07 Jun 2024 01:03:19 GMT  
		Size: 153.0 MB (153000750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd1a8a74f7a8b13b5c1e76db3878fb62e3b502b880c68cf264c9e45a457ef2`  
		Last Modified: Fri, 07 Jun 2024 01:03:17 GMT  
		Size: 9.7 KB (9723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17941bacb7d38399d0602c33481629a86bfe21d5a8dcabcf0f9874ff408df3e1`  
		Last Modified: Fri, 07 Jun 2024 01:03:23 GMT  
		Size: 375.0 MB (375044302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:288f4e8e59919f60de3133b7bf064b461e1bd604a6da024bd9e3eaabdeafe631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61be33cdb48c332d83e02c62c3bfed94f9e7c81b3dca050462a38929615abff`

```dockerfile
```

-	Layers:
	-	`sha256:77bfdd09262938c1730dc8209b30edd65bac6a34e4aba868f7fce2eafc1e6234`  
		Last Modified: Fri, 07 Jun 2024 01:03:18 GMT  
		Size: 10.5 MB (10481798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb7aa476d803d7556b71961a1a12b1d534a1b005566ac50a682ab556eaa05b2`  
		Last Modified: Fri, 07 Jun 2024 01:03:17 GMT  
		Size: 20.3 KB (20344 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:832d21c6fb6632fdd0f4a56249b9e327d15fb90fd5c049ad344a9a087ddf48e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564343053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432d8222848174efc0784d1c156431ee5950a9f8585a380ef3885c2ca41bb3d2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78caa250005821cfc628fb3cc1aabac5b54a1c1d95a076237921f944aac6fc8f`  
		Last Modified: Fri, 07 Jun 2024 06:05:59 GMT  
		Size: 375.0 MB (375044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2255974210b9ce4e5a1fb0bb957cc6772b1efd13228b4f83ba8eadce41366672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10500033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4454b73bf6210078fdbe29405244d11e774f7d1b92fc1317bcef91981b7564`

```dockerfile
```

-	Layers:
	-	`sha256:996d171da6e7986477546b0b61539b226965ab7be033b82462a0591ea54cb4df`  
		Last Modified: Fri, 07 Jun 2024 06:05:52 GMT  
		Size: 10.5 MB (10479381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3711c9e55b183cdfa13fb16a044417f174410b984f4b7dadbff4316fda1d7a4f`  
		Last Modified: Fri, 07 Jun 2024 06:05:51 GMT  
		Size: 20.7 KB (20652 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:618fd59365c2334709f41c82af22bfe7fd43912539393fe0a0051e0178386796
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ee2195c23aae0548f25df64784c48b833337cc9108c3ebd7234274a6340cbed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.1 MB (539062797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55626e187a4d90fb826fa30334e825248915140d8f416fe0730704c25040bf4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0b1f959d93ed8ecb2ab2ba688344883ab77f9d22d22335ead8bbe02ecbadcd`  
		Last Modified: Thu, 13 Jun 2024 19:12:18 GMT  
		Size: 125.2 MB (125156389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52597a01544c4872598373c3c7615b55958057b5d88ca74baf669f78bcc549c2`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a6e45f4e4d0cc7fbaf0e04c7b831a40ed18d4002ac51eb2daf8389aca8a0a5`  
		Last Modified: Thu, 13 Jun 2024 19:12:23 GMT  
		Size: 375.0 MB (375044516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:9bd09474fef0e70c7be430697e6a2af997d72355febe6c199447186da092608e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910875db9710fb0428ce643eb3e3dca706a9c53aa672e145e3934cf044802ab4`

```dockerfile
```

-	Layers:
	-	`sha256:78d4fddb82bc78c37ad0a18e6aaaefd5130028e25f63639eb6e7c62ef1dab414`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 5.2 MB (5220334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d52bf2abd9bd2bdf100f0bf6ccc6e5d3333aade421f559e0f581c27128234b25`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2109e958524f37692a19328bf7f6731b6c8ca653a3764ad720e296028a46383a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.3 MB (537325860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4890fe09b03e2d35d70258ab21ae94d517a84b032ccd9d21a224203c12991b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2227b7a60ffe9cdc89b296632a7a50c0124d0f82d5db6b094ceda75675cfc384`  
		Last Modified: Fri, 14 Jun 2024 04:01:18 GMT  
		Size: 375.0 MB (375044557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:bfbfcdc86a85d94a7e9fdd364c247197016297f5a693da24d2e0e23835b958a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a5736ffb584bff8359b0bbe0de15187d049bedae87f9c45b6e9ecc075519a5`

```dockerfile
```

-	Layers:
	-	`sha256:490fcb35a4f118b051b881d97f9c70f23c983d0cdc6a8ec8344484882a65b1dd`  
		Last Modified: Fri, 14 Jun 2024 04:01:10 GMT  
		Size: 5.2 MB (5199622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d001066d500c7a1c9f15456b21e57c645f730a65ff09d5e9de20fd9a2ea0126`  
		Last Modified: Fri, 14 Jun 2024 04:01:09 GMT  
		Size: 20.8 KB (20775 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-ubi8`

```console
$ docker pull neo4j@sha256:8e33d796eb9f2a6a303160c44d541862eeba22687a81e8feda037a917747b666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c67119f30d5c02a61f583f666750e162e41c28c81e0feb04fd04668de753962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318834401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210401846b51433bc4aa55acc910de0bcb4aa20942d5b7d92ebb75cc5676cf0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f332e8cb9c975e78cc0b9ad29cb7f4c8749c838e72d8ccc5e5d17404fecfb`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 153.0 MB (153000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944aee8cc9dac5f0ee64ce41a8d6cc17782fbe671aab4962907d6b2a4e5a7d9e`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cf6c887e111051de71f4a913467e2bd0413354bb0759d13e8f6d7f510d600`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 126.4 MB (126437735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:af6d873a85c169ee64624544ddb31b0ffb44176305ec0e44bb9b4043adb7f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1392bfbbc89674fd1867b33be716d20fd87a0d622c652b73946628eda5c0276`

```dockerfile
```

-	Layers:
	-	`sha256:d8e7b92ac5052d265f290524cb075c23a34e36a7afd9b6ef115ad7c2dec1831a`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 10.3 MB (10309835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277925c58de032f6b19bebbb438481d276993faa9632c4a45cfdc69fe716eb21`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:97015da3955b89f281e46af22b111313fa5f5b55a6a2ddfbf03d058b2e2ca753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e08a24c38b839b2131ec40488146a3d08bbdd33ab2c9d8f123fb7b65dd9330`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf165894ad1ef9493d70620125cd22248290f9e16e92c1fded276d7501d91d6`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 126.4 MB (126437770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca12143b135aa69ddb3a99df1d41f9b64f3ebc13f5d99855d443fedfb51b4363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dabd327c92dbfd7675e367a743c6703c54b0df0a1b2114a2ce7f9182348f47`

```dockerfile
```

-	Layers:
	-	`sha256:150521840ca507febbc31fb4866cd590da4dbc26a209307466c087bc47610b6c`  
		Last Modified: Fri, 07 Jun 2024 06:04:45 GMT  
		Size: 10.3 MB (10307466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645d743a5057e1f257d24f7c9c2ca8db8d9d504044fbeea2c8ba62294a6a2ae8`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 21.9 KB (21878 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-ubi9`

```console
$ docker pull neo4j@sha256:afb1bbdeb147b691bb3b14ebaa14e45ac849a70a642cea4b52572f5eac69a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c4c79286b1288776032350dd23badd3cbdc34216630bd60c49b53bcd6e2118a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290456398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5d0776d61578fdf0770e44afdb54a236464ef5a8367eec4eb79523d51488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce0767c60b019717d362c02999dc97c3e731cd9847a03459eb3b7ec3b39bfc`  
		Last Modified: Thu, 13 Jun 2024 19:11:50 GMT  
		Size: 125.2 MB (125156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc8ba6e6295079c2f178f7455877f49e17a7a1da092b22db158f499c86c31a`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970dcfa4ad5b646e40207fc178d8025b7c08bb30d6a2b250e48f1a113e2ec5f`  
		Last Modified: Thu, 13 Jun 2024 19:11:49 GMT  
		Size: 126.4 MB (126437857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8095026740ade1dd2fd42e3b9351f5e94355c5565aff5ddd53615c1634ff04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b51b0743b342bf10a4dcd1bfe2ef48353eaab55aff6698fa5a0a9ccd0fff6e`

```dockerfile
```

-	Layers:
	-	`sha256:91df6a28513b41acda6c873f3f9bc3b5acacf9006e36ee94786aac3c2a1df430`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 5.0 MB (5048371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518ec33c589dafad3fb099061cf5e706c6a083a170f7839a7f7dd0b627a7cee4`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 21.6 KB (21646 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8cedd6cc1c6168b1aa2273af47d3c4594cc710387595c812061a788f24b4e079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474e8a1b443970c65639279b101cba282007db0c8f320d9d5ee06c7416be8c40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6b80028ce30dd885d9a0c535b5c5da95037e662ce42e36b6cce464f6f8474`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 126.4 MB (126437828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:299e5d05cd789a0c6d66171061dc7b772814830cf5ecdf31ae0f282fa1434d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd782037ab751a316963c63195cecc94397e6b493fcb67401e9f481054e4e41f`

```dockerfile
```

-	Layers:
	-	`sha256:1ec40fc9bdcf2ae5018eeb6a182e97bfddc743d6df1ad0b53d1afa22c7470c1c`  
		Last Modified: Fri, 14 Jun 2024 04:00:14 GMT  
		Size: 5.0 MB (5027707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84095becd03e6aec7616dfa43b8447b1b5756db5145b0c0a1005d13ea067735`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:8e33d796eb9f2a6a303160c44d541862eeba22687a81e8feda037a917747b666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c67119f30d5c02a61f583f666750e162e41c28c81e0feb04fd04668de753962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318834401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210401846b51433bc4aa55acc910de0bcb4aa20942d5b7d92ebb75cc5676cf0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f332e8cb9c975e78cc0b9ad29cb7f4c8749c838e72d8ccc5e5d17404fecfb`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 153.0 MB (153000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944aee8cc9dac5f0ee64ce41a8d6cc17782fbe671aab4962907d6b2a4e5a7d9e`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cf6c887e111051de71f4a913467e2bd0413354bb0759d13e8f6d7f510d600`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 126.4 MB (126437735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:af6d873a85c169ee64624544ddb31b0ffb44176305ec0e44bb9b4043adb7f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1392bfbbc89674fd1867b33be716d20fd87a0d622c652b73946628eda5c0276`

```dockerfile
```

-	Layers:
	-	`sha256:d8e7b92ac5052d265f290524cb075c23a34e36a7afd9b6ef115ad7c2dec1831a`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 10.3 MB (10309835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277925c58de032f6b19bebbb438481d276993faa9632c4a45cfdc69fe716eb21`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:97015da3955b89f281e46af22b111313fa5f5b55a6a2ddfbf03d058b2e2ca753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e08a24c38b839b2131ec40488146a3d08bbdd33ab2c9d8f123fb7b65dd9330`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf165894ad1ef9493d70620125cd22248290f9e16e92c1fded276d7501d91d6`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 126.4 MB (126437770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca12143b135aa69ddb3a99df1d41f9b64f3ebc13f5d99855d443fedfb51b4363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dabd327c92dbfd7675e367a743c6703c54b0df0a1b2114a2ce7f9182348f47`

```dockerfile
```

-	Layers:
	-	`sha256:150521840ca507febbc31fb4866cd590da4dbc26a209307466c087bc47610b6c`  
		Last Modified: Fri, 07 Jun 2024 06:04:45 GMT  
		Size: 10.3 MB (10307466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645d743a5057e1f257d24f7c9c2ca8db8d9d504044fbeea2c8ba62294a6a2ae8`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 21.9 KB (21878 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:afb1bbdeb147b691bb3b14ebaa14e45ac849a70a642cea4b52572f5eac69a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c4c79286b1288776032350dd23badd3cbdc34216630bd60c49b53bcd6e2118a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290456398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5d0776d61578fdf0770e44afdb54a236464ef5a8367eec4eb79523d51488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce0767c60b019717d362c02999dc97c3e731cd9847a03459eb3b7ec3b39bfc`  
		Last Modified: Thu, 13 Jun 2024 19:11:50 GMT  
		Size: 125.2 MB (125156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc8ba6e6295079c2f178f7455877f49e17a7a1da092b22db158f499c86c31a`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970dcfa4ad5b646e40207fc178d8025b7c08bb30d6a2b250e48f1a113e2ec5f`  
		Last Modified: Thu, 13 Jun 2024 19:11:49 GMT  
		Size: 126.4 MB (126437857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8095026740ade1dd2fd42e3b9351f5e94355c5565aff5ddd53615c1634ff04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b51b0743b342bf10a4dcd1bfe2ef48353eaab55aff6698fa5a0a9ccd0fff6e`

```dockerfile
```

-	Layers:
	-	`sha256:91df6a28513b41acda6c873f3f9bc3b5acacf9006e36ee94786aac3c2a1df430`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 5.0 MB (5048371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518ec33c589dafad3fb099061cf5e706c6a083a170f7839a7f7dd0b627a7cee4`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 21.6 KB (21646 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8cedd6cc1c6168b1aa2273af47d3c4594cc710387595c812061a788f24b4e079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474e8a1b443970c65639279b101cba282007db0c8f320d9d5ee06c7416be8c40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6b80028ce30dd885d9a0c535b5c5da95037e662ce42e36b6cce464f6f8474`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 126.4 MB (126437828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:299e5d05cd789a0c6d66171061dc7b772814830cf5ecdf31ae0f282fa1434d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd782037ab751a316963c63195cecc94397e6b493fcb67401e9f481054e4e41f`

```dockerfile
```

-	Layers:
	-	`sha256:1ec40fc9bdcf2ae5018eeb6a182e97bfddc743d6df1ad0b53d1afa22c7470c1c`  
		Last Modified: Fri, 14 Jun 2024 04:00:14 GMT  
		Size: 5.0 MB (5027707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84095becd03e6aec7616dfa43b8447b1b5756db5145b0c0a1005d13ea067735`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:5b9acd415009c72a907450b25419caff319f398f1195efb70849bf2d8b0101f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5396d211d879bab3304b98645df9f1bdae44c6c09e7a683c5eeabae84e2a04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b423e3650571732ce1b03908a9f3539393d6294493a59376f2b13d1127a1fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c87b552991cf2d5033648ff7ab4db56a9c6727738dfa5d713cff5f2341ce79`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94613cc6429b1d77f6a35329e3955fa9087cb8cc447460b6e9e4bc59b01af945`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a6f8b56be1174d55bb5e2a3226fb20ec06e65f1e8b307909361f716a4f9e9`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a9abda355c801b110ea0264176cbfe13f7e564b9df83036d1a577d1165c49f`  
		Last Modified: Thu, 13 Jun 2024 18:30:47 GMT  
		Size: 378.0 MB (377982656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b204699602d898d428e9adbb8395ddef68bbf29bd44a998d214cf937d3555581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f280ce3e502c89b5efa7a5005fca7b8063ba49c7da23740dd31a6d51e26976`

```dockerfile
```

-	Layers:
	-	`sha256:6919be721a7957ae5bd9ce6a5874df1b984e8e5205a614c88896e9ac0a2a3638`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.1 MB (3133587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d8d4e7dce72ef2ef21c9c7d392ed6ac3392ba6613999a2f1a36ec323a77ee1`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:221e2fa985aa7c4daa776938a5707f9b519331f58a5147f4cd0100c8aba9e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e77d681490d0bf6fe479807c4eb12a7edc384f0475e46f997e159402a2c10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5616767fa4cbc4fc191447cc4c22863cc4dd8a4e39b13f1e37ba7a3ec022c`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabfd6a56d642009d405652fef55bdfe2f376366a74b47c389f0af97a837bcc`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb699162c081b5f3a0b748b57b3f2571201e98bfb7e7879e37efd46f7e34c178`  
		Last Modified: Thu, 13 Jun 2024 19:31:59 GMT  
		Size: 377.9 MB (377944491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:94240005fd042203bbc746549a05636903e78855b79047f22ddf3a8c8f8a006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50263d291ddd0a2f1ea55a611614774a4c413e707c5925492af8393aaee16862`

```dockerfile
```

-	Layers:
	-	`sha256:c3cba07c3ea026b6e1c9f478c73079da7519a5ee4c8d1a0fc63804c9f5c7ee99`  
		Last Modified: Thu, 13 Jun 2024 19:31:52 GMT  
		Size: 3.1 MB (3133898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c6d9124715d26ee27296aa36e91b2c25bfd4fb538561eefd9104246074942`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5b9acd415009c72a907450b25419caff319f398f1195efb70849bf2d8b0101f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5396d211d879bab3304b98645df9f1bdae44c6c09e7a683c5eeabae84e2a04d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b423e3650571732ce1b03908a9f3539393d6294493a59376f2b13d1127a1fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c87b552991cf2d5033648ff7ab4db56a9c6727738dfa5d713cff5f2341ce79`  
		Last Modified: Thu, 13 Jun 2024 18:30:42 GMT  
		Size: 145.1 MB (145095076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94613cc6429b1d77f6a35329e3955fa9087cb8cc447460b6e9e4bc59b01af945`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32a6f8b56be1174d55bb5e2a3226fb20ec06e65f1e8b307909361f716a4f9e9`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 9.5 KB (9541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a9abda355c801b110ea0264176cbfe13f7e564b9df83036d1a577d1165c49f`  
		Last Modified: Thu, 13 Jun 2024 18:30:47 GMT  
		Size: 378.0 MB (377982656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b204699602d898d428e9adbb8395ddef68bbf29bd44a998d214cf937d3555581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f280ce3e502c89b5efa7a5005fca7b8063ba49c7da23740dd31a6d51e26976`

```dockerfile
```

-	Layers:
	-	`sha256:6919be721a7957ae5bd9ce6a5874df1b984e8e5205a614c88896e9ac0a2a3638`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 3.1 MB (3133587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d8d4e7dce72ef2ef21c9c7d392ed6ac3392ba6613999a2f1a36ec323a77ee1`  
		Last Modified: Thu, 13 Jun 2024 18:30:40 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:221e2fa985aa7c4daa776938a5707f9b519331f58a5147f4cd0100c8aba9e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e77d681490d0bf6fe479807c4eb12a7edc384f0475e46f997e159402a2c10`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5616767fa4cbc4fc191447cc4c22863cc4dd8a4e39b13f1e37ba7a3ec022c`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecabfd6a56d642009d405652fef55bdfe2f376366a74b47c389f0af97a837bcc`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb699162c081b5f3a0b748b57b3f2571201e98bfb7e7879e37efd46f7e34c178`  
		Last Modified: Thu, 13 Jun 2024 19:31:59 GMT  
		Size: 377.9 MB (377944491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:94240005fd042203bbc746549a05636903e78855b79047f22ddf3a8c8f8a006d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50263d291ddd0a2f1ea55a611614774a4c413e707c5925492af8393aaee16862`

```dockerfile
```

-	Layers:
	-	`sha256:c3cba07c3ea026b6e1c9f478c73079da7519a5ee4c8d1a0fc63804c9f5c7ee99`  
		Last Modified: Thu, 13 Jun 2024 19:31:52 GMT  
		Size: 3.1 MB (3133898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40c6d9124715d26ee27296aa36e91b2c25bfd4fb538561eefd9104246074942`  
		Last Modified: Thu, 13 Jun 2024 19:31:51 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:ec560a1209bac84f4962e1da1886e321fe5e90d898f42b243e15d63fb550bf69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:d3235a690b5168eea3292c284c1f7cf205f781c5c873a28aad52c1e3de9a1019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.4 MB (567441150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bd110b3b2423808a50813f89b3f6739d506a1a6a1b27f2425fa0b9e484df42`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99646ded8c03f270d1a85183a6ae3aa330891d5b30a83f2d04c15bc45d0a0f4b`  
		Last Modified: Fri, 07 Jun 2024 01:03:19 GMT  
		Size: 153.0 MB (153000750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd1a8a74f7a8b13b5c1e76db3878fb62e3b502b880c68cf264c9e45a457ef2`  
		Last Modified: Fri, 07 Jun 2024 01:03:17 GMT  
		Size: 9.7 KB (9723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17941bacb7d38399d0602c33481629a86bfe21d5a8dcabcf0f9874ff408df3e1`  
		Last Modified: Fri, 07 Jun 2024 01:03:23 GMT  
		Size: 375.0 MB (375044302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:288f4e8e59919f60de3133b7bf064b461e1bd604a6da024bd9e3eaabdeafe631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61be33cdb48c332d83e02c62c3bfed94f9e7c81b3dca050462a38929615abff`

```dockerfile
```

-	Layers:
	-	`sha256:77bfdd09262938c1730dc8209b30edd65bac6a34e4aba868f7fce2eafc1e6234`  
		Last Modified: Fri, 07 Jun 2024 01:03:18 GMT  
		Size: 10.5 MB (10481798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb7aa476d803d7556b71961a1a12b1d534a1b005566ac50a682ab556eaa05b2`  
		Last Modified: Fri, 07 Jun 2024 01:03:17 GMT  
		Size: 20.3 KB (20344 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:832d21c6fb6632fdd0f4a56249b9e327d15fb90fd5c049ad344a9a087ddf48e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **564.3 MB (564343053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432d8222848174efc0784d1c156431ee5950a9f8585a380ef3885c2ca41bb3d2`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78caa250005821cfc628fb3cc1aabac5b54a1c1d95a076237921f944aac6fc8f`  
		Last Modified: Fri, 07 Jun 2024 06:05:59 GMT  
		Size: 375.0 MB (375044262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2255974210b9ce4e5a1fb0bb957cc6772b1efd13228b4f83ba8eadce41366672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10500033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef4454b73bf6210078fdbe29405244d11e774f7d1b92fc1317bcef91981b7564`

```dockerfile
```

-	Layers:
	-	`sha256:996d171da6e7986477546b0b61539b226965ab7be033b82462a0591ea54cb4df`  
		Last Modified: Fri, 07 Jun 2024 06:05:52 GMT  
		Size: 10.5 MB (10479381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3711c9e55b183cdfa13fb16a044417f174410b984f4b7dadbff4316fda1d7a4f`  
		Last Modified: Fri, 07 Jun 2024 06:05:51 GMT  
		Size: 20.7 KB (20652 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:618fd59365c2334709f41c82af22bfe7fd43912539393fe0a0051e0178386796
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ee2195c23aae0548f25df64784c48b833337cc9108c3ebd7234274a6340cbed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.1 MB (539062797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55626e187a4d90fb826fa30334e825248915140d8f416fe0730704c25040bf4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0b1f959d93ed8ecb2ab2ba688344883ab77f9d22d22335ead8bbe02ecbadcd`  
		Last Modified: Thu, 13 Jun 2024 19:12:18 GMT  
		Size: 125.2 MB (125156389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52597a01544c4872598373c3c7615b55958057b5d88ca74baf669f78bcc549c2`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a6e45f4e4d0cc7fbaf0e04c7b831a40ed18d4002ac51eb2daf8389aca8a0a5`  
		Last Modified: Thu, 13 Jun 2024 19:12:23 GMT  
		Size: 375.0 MB (375044516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:9bd09474fef0e70c7be430697e6a2af997d72355febe6c199447186da092608e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910875db9710fb0428ce643eb3e3dca706a9c53aa672e145e3934cf044802ab4`

```dockerfile
```

-	Layers:
	-	`sha256:78d4fddb82bc78c37ad0a18e6aaaefd5130028e25f63639eb6e7c62ef1dab414`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 5.2 MB (5220334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d52bf2abd9bd2bdf100f0bf6ccc6e5d3333aade421f559e0f581c27128234b25`  
		Last Modified: Thu, 13 Jun 2024 19:12:14 GMT  
		Size: 20.5 KB (20468 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2109e958524f37692a19328bf7f6731b6c8ca653a3764ad720e296028a46383a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.3 MB (537325860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4890fe09b03e2d35d70258ab21ae94d517a84b032ccd9d21a224203c12991b0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=ba4c6236f822138f9e9034bbf50bfca98d3bf794add0731aa49841127c7aea1e NEO4J_TARBALL=neo4j-enterprise-5.20.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2227b7a60ffe9cdc89b296632a7a50c0124d0f82d5db6b094ceda75675cfc384`  
		Last Modified: Fri, 14 Jun 2024 04:01:18 GMT  
		Size: 375.0 MB (375044557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:bfbfcdc86a85d94a7e9fdd364c247197016297f5a693da24d2e0e23835b958a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a5736ffb584bff8359b0bbe0de15187d049bedae87f9c45b6e9ecc075519a5`

```dockerfile
```

-	Layers:
	-	`sha256:490fcb35a4f118b051b881d97f9c70f23c983d0cdc6a8ec8344484882a65b1dd`  
		Last Modified: Fri, 14 Jun 2024 04:01:10 GMT  
		Size: 5.2 MB (5199622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d001066d500c7a1c9f15456b21e57c645f730a65ff09d5e9de20fd9a2ea0126`  
		Last Modified: Fri, 14 Jun 2024 04:01:09 GMT  
		Size: 20.8 KB (20775 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:52d3dec8d45585b21edeca8517d752b2512e52aa94f80fc36a5788c88c95f8e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:99a767ef6f5573cd72d6d7f32c5266233af3c58efdc71577349a7c251d8ecb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bd42913597ec575976641bd4f853a7c230e14b38837e1063506131ed6de990`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0190aacfecb347294ce0013feb163151ce56d2471ce2d8e6cb4dc77606f82f6`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 145.1 MB (145095063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5c015b1a43c9ef47011d25053e38a43f514b577c30f120dc79bb76bc94e73`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b364804f8cc6f0c7a43b061d12c9837e8bfa7162b8afa2c875076c7d510782a2`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c03e3e4b4e5acfffaf7f7c49407d45136482b779319cce03e1d13bf548b1c1`  
		Last Modified: Thu, 13 Jun 2024 18:29:35 GMT  
		Size: 129.4 MB (129367592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f42b1e95b7e28efab2bf67eadd100f0e388c445433e3055a397591184fd8fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8dc2452158d3b788f5dfbd155309b41b16a7b57755a74a53d5d774299ff508`

```dockerfile
```

-	Layers:
	-	`sha256:a55741ba4bc398aaf540c11c46bed0ff3f3debd8e3bb93efa8feb4542e79c077`  
		Last Modified: Thu, 13 Jun 2024 18:29:32 GMT  
		Size: 3.0 MB (2962818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3098ff9192ad3cbe67db26f23d26783762cf8c795ff7bc970327862f12b66`  
		Last Modified: Thu, 13 Jun 2024 18:29:31 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e2c8afd384a82dcba3abede76525f355c0ad456958968f1a8d1d9f0d3d210830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe16909792ab5ebcac5f2066f9aa39825baef596af71cfb4f971e7c152687cbf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 23 May 2024 10:12:20 GMT
CMD ["bash"]
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 May 2024 10:12:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862444d8385e278b8215a3b8b928519198c91c9c4cb9088ab56c9cbf4ae1296d`  
		Last Modified: Thu, 13 Jun 2024 19:30:35 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db58bd6f94052a87a4ad51464bcc24f3d480a5d6a0f898972fe501e4081dda9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a424b41feca96b0dd599b87aa163d38aa99b21b7bdfad5b66229be5f3c525d9`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90406efe4064aa1176e5027ff3c788dc7c5ed68ebc045a5809e15f2ba160cd90`  
		Last Modified: Thu, 13 Jun 2024 19:30:34 GMT  
		Size: 129.3 MB (129333618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:244c1ef7505311132e068ce788f47ef847ac1fc2455d88d5113c7f146cfb4c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f708813f4ce0fd7156e51ad7640b7dbcf1ab9c54ff2568dc1c1456d3cfd7f961`

```dockerfile
```

-	Layers:
	-	`sha256:89f3579d81d5eb3c4791947d495a6606afa4b2f38249fbe8b1e7136187a5c3b3`  
		Last Modified: Thu, 13 Jun 2024 19:30:32 GMT  
		Size: 3.0 MB (2963225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d21f29cce1168c9e233e8736afe959384ba1c67d8715a2f917b38660fdcd50`  
		Last Modified: Thu, 13 Jun 2024 19:30:31 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:8e33d796eb9f2a6a303160c44d541862eeba22687a81e8feda037a917747b666
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c67119f30d5c02a61f583f666750e162e41c28c81e0feb04fd04668de753962e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318834401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a210401846b51433bc4aa55acc910de0bcb4aa20942d5b7d92ebb75cc5676cf0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:6fe415d8ed10b98dd4befb7882431823c084e3982ed3c876b0d9e355d9c77e52 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:d65db5c3c919c582bea22c86b20072060b152fc35ecf7dddba590052d543e6d5 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:50b8ae8537153f061b9b48f0ce2547d493cccba4d14294d4c13a66b2f98d2b7c in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8393debac2ec316f87eab40af5451d57df2863f844f545d40447e46e025c9663`  
		Last Modified: Thu, 06 Jun 2024 15:40:55 GMT  
		Size: 39.4 MB (39386343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9f332e8cb9c975e78cc0b9ad29cb7f4c8749c838e72d8ccc5e5d17404fecfb`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 153.0 MB (153000567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944aee8cc9dac5f0ee64ce41a8d6cc17782fbe671aab4962907d6b2a4e5a7d9e`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427cf6c887e111051de71f4a913467e2bd0413354bb0759d13e8f6d7f510d600`  
		Last Modified: Fri, 07 Jun 2024 01:03:09 GMT  
		Size: 126.4 MB (126437735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:af6d873a85c169ee64624544ddb31b0ffb44176305ec0e44bb9b4043adb7f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1392bfbbc89674fd1867b33be716d20fd87a0d622c652b73946628eda5c0276`

```dockerfile
```

-	Layers:
	-	`sha256:d8e7b92ac5052d265f290524cb075c23a34e36a7afd9b6ef115ad7c2dec1831a`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 10.3 MB (10309835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277925c58de032f6b19bebbb438481d276993faa9632c4a45cfdc69fe716eb21`  
		Last Modified: Fri, 07 Jun 2024 01:03:07 GMT  
		Size: 21.5 KB (21522 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:97015da3955b89f281e46af22b111313fa5f5b55a6a2ddfbf03d058b2e2ca753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315736561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e08a24c38b839b2131ec40488146a3d08bbdd33ab2c9d8f123fb7b65dd9330`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:9f0a629c67a178fd60383b4bb4b2f8d4abdf9dfd7a6098dfad00b352ed741c8d in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:7cb54aecc729e97f374805d4a2e2f2e7d9e74c12805c1493174654aec337c1ed in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
ADD file:c25915548408777b4dc5847c96fb08e6a3589d8eb59b718f46549c4a21f87c74 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1717584414.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:52086c080e013396be487681a539c05cdf5f55494039f22825674ba22b1251c3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1717584414 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1717584414" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-05T10:47:24" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1717584414"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3153934-80fdb.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
ENV JAVA_HOME=/usr
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi8/' $NEO4J_HOME/packaging_info;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8cdcb25add0cba4e1b34d0297304016cdd2f5e392f62ea5be7f6fd0244048e64`  
		Last Modified: Thu, 06 Jun 2024 15:43:57 GMT  
		Size: 37.7 MB (37690098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25144cbef240ddc99052eabee429bdf0e4c9ca630a713116d7f031efc7821dfd`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 151.6 MB (151598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ea2d83ccd51b1fb3f42c75ab108e06952d49069d63f5bb084465313cc117a1`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 9.7 KB (9725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf165894ad1ef9493d70620125cd22248290f9e16e92c1fded276d7501d91d6`  
		Last Modified: Fri, 07 Jun 2024 06:04:48 GMT  
		Size: 126.4 MB (126437770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca12143b135aa69ddb3a99df1d41f9b64f3ebc13f5d99855d443fedfb51b4363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10329344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dabd327c92dbfd7675e367a743c6703c54b0df0a1b2114a2ce7f9182348f47`

```dockerfile
```

-	Layers:
	-	`sha256:150521840ca507febbc31fb4866cd590da4dbc26a209307466c087bc47610b6c`  
		Last Modified: Fri, 07 Jun 2024 06:04:45 GMT  
		Size: 10.3 MB (10307466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:645d743a5057e1f257d24f7c9c2ca8db8d9d504044fbeea2c8ba62294a6a2ae8`  
		Last Modified: Fri, 07 Jun 2024 06:04:44 GMT  
		Size: 21.9 KB (21878 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:afb1bbdeb147b691bb3b14ebaa14e45ac849a70a642cea4b52572f5eac69a873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c4c79286b1288776032350dd23badd3cbdc34216630bd60c49b53bcd6e2118a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290456398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753b5d0776d61578fdf0770e44afdb54a236464ef5a8367eec4eb79523d51488`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0177c7dc75a5666fd7d839eb5a0fe92cceec6ce76ec113c5d876fdb57ce3b149 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:4163a5d830cc37221be507fb49bdb623672e7a59ca81defe42fc0122ff2067cc in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:0394409f6db7784d16a6bf3439e7470dbb324dc30ed9d4c8db797157e4501a3f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:e394ea8406c7ed85ddc862f882ec77dcfd3863de3cb90fd8006238d521d22d44`  
		Last Modified: Thu, 13 Jun 2024 09:01:28 GMT  
		Size: 38.9 MB (38852317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce0767c60b019717d362c02999dc97c3e731cd9847a03459eb3b7ec3b39bfc`  
		Last Modified: Thu, 13 Jun 2024 19:11:50 GMT  
		Size: 125.2 MB (125156648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc8ba6e6295079c2f178f7455877f49e17a7a1da092b22db158f499c86c31a`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970dcfa4ad5b646e40207fc178d8025b7c08bb30d6a2b250e48f1a113e2ec5f`  
		Last Modified: Thu, 13 Jun 2024 19:11:49 GMT  
		Size: 126.4 MB (126437857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8095026740ade1dd2fd42e3b9351f5e94355c5565aff5ddd53615c1634ff04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5070017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b51b0743b342bf10a4dcd1bfe2ef48353eaab55aff6698fa5a0a9ccd0fff6e`

```dockerfile
```

-	Layers:
	-	`sha256:91df6a28513b41acda6c873f3f9bc3b5acacf9006e36ee94786aac3c2a1df430`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 5.0 MB (5048371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:518ec33c589dafad3fb099061cf5e706c6a083a170f7839a7f7dd0b627a7cee4`  
		Last Modified: Thu, 13 Jun 2024 19:11:48 GMT  
		Size: 21.6 KB (21646 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8cedd6cc1c6168b1aa2273af47d3c4594cc710387595c812061a788f24b4e079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474e8a1b443970c65639279b101cba282007db0c8f320d9d5ee06c7416be8c40`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:a0eabcdf2ab69cce7aa1eb328b862afe9d22c644fe1194679f30c6f67e244c6b in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:171eafe5d6538aeb2cf5cf9f6e8618f56eddbc2d8e3acf65107d17c6cc9c35de in /etc/yum.repos.d/ 
# Thu, 23 May 2024 10:12:20 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 23 May 2024 10:12:20 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 23 May 2024 10:12:20 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 23 May 2024 10:12:20 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.expose-services=""
# Thu, 23 May 2024 10:12:20 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 23 May 2024 10:12:20 GMT
ENV container oci
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -rf /var/log/*
# Thu, 23 May 2024 10:12:20 GMT
LABEL release=1134
# Thu, 23 May 2024 10:12:20 GMT
ADD file:889f44042d0c51b9eda12ed533aa1fb117a8ffcf209c0ad0a329baaa81eac425 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1134.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:b6af28769ecb7942ba5cf7b0e1bbf054cd8a414727a87e4ff5ecb40886563b94 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1134 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-06-06T00:53:59" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1134"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/repo-d5140.repo' '/etc/yum.repos.d/repo-4f47a.repo'
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 23 May 2024 10:12:20 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV NEO4J_SHA256=203215748402702871e511c6dfff3c62f72587c4e80df703bf854085c436d066 NEO4J_TARBALL=neo4j-community-5.20.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
# Thu, 23 May 2024 10:12:20 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 23 May 2024 10:12:20 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.20.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 23 May 2024 10:12:20 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 May 2024 10:12:20 GMT
WORKDIR /var/lib/neo4j
# Thu, 23 May 2024 10:12:20 GMT
VOLUME [/data /logs]
# Thu, 23 May 2024 10:12:20 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 23 May 2024 10:12:20 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 23 May 2024 10:12:20 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c209fde2f4fc18de77579e9d71fef235b3cc367c0aba0c9948f4459779b6c9`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 125.2 MB (125153338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678c1ae8de5429bdb772bc81cd59307ad87b64f9b720cb621f66d294b7b4bd4`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6b80028ce30dd885d9a0c535b5c5da95037e662ce42e36b6cce464f6f8474`  
		Last Modified: Fri, 14 Jun 2024 04:00:17 GMT  
		Size: 126.4 MB (126437828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:299e5d05cd789a0c6d66171061dc7b772814830cf5ecdf31ae0f282fa1434d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd782037ab751a316963c63195cecc94397e6b493fcb67401e9f481054e4e41f`

```dockerfile
```

-	Layers:
	-	`sha256:1ec40fc9bdcf2ae5018eeb6a182e97bfddc743d6df1ad0b53d1afa22c7470c1c`  
		Last Modified: Fri, 14 Jun 2024 04:00:14 GMT  
		Size: 5.0 MB (5027707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84095becd03e6aec7616dfa43b8447b1b5756db5145b0c0a1005d13ea067735`  
		Last Modified: Fri, 14 Jun 2024 04:00:13 GMT  
		Size: 22.0 KB (22002 bytes)  
		MIME: application/vnd.in-toto+json
