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
-	[`neo4j:5.21.0`](#neo4j5210)
-	[`neo4j:5.21.0-bullseye`](#neo4j5210-bullseye)
-	[`neo4j:5.21.0-community`](#neo4j5210-community)
-	[`neo4j:5.21.0-community-bullseye`](#neo4j5210-community-bullseye)
-	[`neo4j:5.21.0-community-ubi9`](#neo4j5210-community-ubi9)
-	[`neo4j:5.21.0-enterprise`](#neo4j5210-enterprise)
-	[`neo4j:5.21.0-enterprise-bullseye`](#neo4j5210-enterprise-bullseye)
-	[`neo4j:5.21.0-enterprise-ubi9`](#neo4j5210-enterprise-ubi9)
-	[`neo4j:5.21.0-ubi9`](#neo4j5210-ubi9)
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
$ docker pull neo4j@sha256:0aa50a0fa11ecf7430758fb469968a8874d2c0d3e78c0094aace5395aa1da55c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:7f52694cf713ac0e4f10cb543913bb13e1a2e542604fd751625b6d121bacca01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298263071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38a5178b15dbdbac57c82ab9dcd8f3c1220bc7d0c11edb5cc0e9be85bc8ac41`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204b6503bdca46aa13282b6f3ae69702b1af3ff33e021243281347b9f1f2bb25`  
		Last Modified: Tue, 02 Jul 2024 03:04:33 GMT  
		Size: 145.5 MB (145505215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03c591ae0331f5c72d27ac69f45fda60c6c5c67d09d8e26932598872446d6cd`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0943ee76ad371090804f8faf2e54fac70958b89398222b2cd734446db82617`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8984db55e39c6370e720299fb8b8c0b8899866d15861589a3c7ef5ac7a480d39`  
		Last Modified: Tue, 02 Jul 2024 03:04:33 GMT  
		Size: 121.3 MB (121322262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:0417a5b7d4ee1ef38ae64491804acbee2851bddd85ea93f5a92f71d8f68f91a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7c08b4f89882eee2e17642d34e51b57b86e7061732cbb775aa17372a3c700`

```dockerfile
```

-	Layers:
	-	`sha256:3fe8c358a6758508b043a7902f6966e09414823cdf48c3ddbe742f041cfad8ed`  
		Last Modified: Tue, 02 Jul 2024 03:04:31 GMT  
		Size: 2.9 MB (2940156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73e27c8441e08883281635198a8e5fd9e0917895adc6f856f6fe8e27a60937b`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
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
$ docker pull neo4j@sha256:0aa50a0fa11ecf7430758fb469968a8874d2c0d3e78c0094aace5395aa1da55c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:7f52694cf713ac0e4f10cb543913bb13e1a2e542604fd751625b6d121bacca01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298263071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38a5178b15dbdbac57c82ab9dcd8f3c1220bc7d0c11edb5cc0e9be85bc8ac41`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204b6503bdca46aa13282b6f3ae69702b1af3ff33e021243281347b9f1f2bb25`  
		Last Modified: Tue, 02 Jul 2024 03:04:33 GMT  
		Size: 145.5 MB (145505215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03c591ae0331f5c72d27ac69f45fda60c6c5c67d09d8e26932598872446d6cd`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0943ee76ad371090804f8faf2e54fac70958b89398222b2cd734446db82617`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8984db55e39c6370e720299fb8b8c0b8899866d15861589a3c7ef5ac7a480d39`  
		Last Modified: Tue, 02 Jul 2024 03:04:33 GMT  
		Size: 121.3 MB (121322262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0417a5b7d4ee1ef38ae64491804acbee2851bddd85ea93f5a92f71d8f68f91a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7c08b4f89882eee2e17642d34e51b57b86e7061732cbb775aa17372a3c700`

```dockerfile
```

-	Layers:
	-	`sha256:3fe8c358a6758508b043a7902f6966e09414823cdf48c3ddbe742f041cfad8ed`  
		Last Modified: Tue, 02 Jul 2024 03:04:31 GMT  
		Size: 2.9 MB (2940156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73e27c8441e08883281635198a8e5fd9e0917895adc6f856f6fe8e27a60937b`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
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
$ docker pull neo4j@sha256:c88402c5b608dfa7a7f172887d2030311dd3ffc690d9c29d47d37e6b02e0356f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9e7cbb4478aebe911ae0480d1a8a4ae3176258048e51a92e066b507ba1fb599f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (402972505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a3e27e729487bf14c63aeccba7e5b0a77cbc64c27a8ed0360d53e50eea6e88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cdfad68f7be9d8fb1140165be67b8e1596d91dae5488b6dd750e523cc6288a`  
		Last Modified: Tue, 02 Jul 2024 03:20:30 GMT  
		Size: 145.5 MB (145505213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1333b415dcb566b7d6955314ba8e82901fa5cf4c9faa87b9fb9ed778d3e7949d`  
		Last Modified: Tue, 02 Jul 2024 03:20:28 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a124b33facfbbc1ee32d85670fa2a874f880e8edc75c9dee47196953048149fb`  
		Last Modified: Tue, 02 Jul 2024 03:20:28 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836c484c6e1260e7aa505d1e59928dacac9eee10b0a34cfcb6584faeac56a75e`  
		Last Modified: Tue, 02 Jul 2024 03:20:37 GMT  
		Size: 226.0 MB (226031696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:1827ca612ca5a01af3f604375b81a488435ad3723bde2de265e762ba2c2f8bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27eb2f10cf8e7a02166067ce4be4c23cf082b2aac2b095ff1eef4dc4a412cd2`

```dockerfile
```

-	Layers:
	-	`sha256:9b1478d13781559fddc68c09900363ba774b03fdcb945b6ed1af309b1f220b74`  
		Last Modified: Tue, 02 Jul 2024 03:20:28 GMT  
		Size: 3.1 MB (3069466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4302deedc27d113021b672b7b1538cc3475e0a372dc566a82f7b0d1aa9918bf4`  
		Last Modified: Tue, 02 Jul 2024 03:20:29 GMT  
		Size: 19.0 KB (18965 bytes)  
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
$ docker pull neo4j@sha256:0aa50a0fa11ecf7430758fb469968a8874d2c0d3e78c0094aace5395aa1da55c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.34` - linux; amd64

```console
$ docker pull neo4j@sha256:7f52694cf713ac0e4f10cb543913bb13e1a2e542604fd751625b6d121bacca01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298263071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38a5178b15dbdbac57c82ab9dcd8f3c1220bc7d0c11edb5cc0e9be85bc8ac41`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204b6503bdca46aa13282b6f3ae69702b1af3ff33e021243281347b9f1f2bb25`  
		Last Modified: Tue, 02 Jul 2024 03:04:33 GMT  
		Size: 145.5 MB (145505215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03c591ae0331f5c72d27ac69f45fda60c6c5c67d09d8e26932598872446d6cd`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0943ee76ad371090804f8faf2e54fac70958b89398222b2cd734446db82617`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8984db55e39c6370e720299fb8b8c0b8899866d15861589a3c7ef5ac7a480d39`  
		Last Modified: Tue, 02 Jul 2024 03:04:33 GMT  
		Size: 121.3 MB (121322262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34` - unknown; unknown

```console
$ docker pull neo4j@sha256:0417a5b7d4ee1ef38ae64491804acbee2851bddd85ea93f5a92f71d8f68f91a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7c08b4f89882eee2e17642d34e51b57b86e7061732cbb775aa17372a3c700`

```dockerfile
```

-	Layers:
	-	`sha256:3fe8c358a6758508b043a7902f6966e09414823cdf48c3ddbe742f041cfad8ed`  
		Last Modified: Tue, 02 Jul 2024 03:04:31 GMT  
		Size: 2.9 MB (2940156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73e27c8441e08883281635198a8e5fd9e0917895adc6f856f6fe8e27a60937b`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
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
$ docker pull neo4j@sha256:0aa50a0fa11ecf7430758fb469968a8874d2c0d3e78c0094aace5395aa1da55c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.34-community` - linux; amd64

```console
$ docker pull neo4j@sha256:7f52694cf713ac0e4f10cb543913bb13e1a2e542604fd751625b6d121bacca01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298263071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38a5178b15dbdbac57c82ab9dcd8f3c1220bc7d0c11edb5cc0e9be85bc8ac41`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204b6503bdca46aa13282b6f3ae69702b1af3ff33e021243281347b9f1f2bb25`  
		Last Modified: Tue, 02 Jul 2024 03:04:33 GMT  
		Size: 145.5 MB (145505215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03c591ae0331f5c72d27ac69f45fda60c6c5c67d09d8e26932598872446d6cd`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0943ee76ad371090804f8faf2e54fac70958b89398222b2cd734446db82617`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8984db55e39c6370e720299fb8b8c0b8899866d15861589a3c7ef5ac7a480d39`  
		Last Modified: Tue, 02 Jul 2024 03:04:33 GMT  
		Size: 121.3 MB (121322262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0417a5b7d4ee1ef38ae64491804acbee2851bddd85ea93f5a92f71d8f68f91a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a7c08b4f89882eee2e17642d34e51b57b86e7061732cbb775aa17372a3c700`

```dockerfile
```

-	Layers:
	-	`sha256:3fe8c358a6758508b043a7902f6966e09414823cdf48c3ddbe742f041cfad8ed`  
		Last Modified: Tue, 02 Jul 2024 03:04:31 GMT  
		Size: 2.9 MB (2940156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73e27c8441e08883281635198a8e5fd9e0917895adc6f856f6fe8e27a60937b`  
		Last Modified: Tue, 02 Jul 2024 03:04:30 GMT  
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
$ docker pull neo4j@sha256:c88402c5b608dfa7a7f172887d2030311dd3ffc690d9c29d47d37e6b02e0356f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.34-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:9e7cbb4478aebe911ae0480d1a8a4ae3176258048e51a92e066b507ba1fb599f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (402972505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a3e27e729487bf14c63aeccba7e5b0a77cbc64c27a8ed0360d53e50eea6e88`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 12:22:43 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cdfad68f7be9d8fb1140165be67b8e1596d91dae5488b6dd750e523cc6288a`  
		Last Modified: Tue, 02 Jul 2024 03:20:30 GMT  
		Size: 145.5 MB (145505213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1333b415dcb566b7d6955314ba8e82901fa5cf4c9faa87b9fb9ed778d3e7949d`  
		Last Modified: Tue, 02 Jul 2024 03:20:28 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a124b33facfbbc1ee32d85670fa2a874f880e8edc75c9dee47196953048149fb`  
		Last Modified: Tue, 02 Jul 2024 03:20:28 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836c484c6e1260e7aa505d1e59928dacac9eee10b0a34cfcb6584faeac56a75e`  
		Last Modified: Tue, 02 Jul 2024 03:20:37 GMT  
		Size: 226.0 MB (226031696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:1827ca612ca5a01af3f604375b81a488435ad3723bde2de265e762ba2c2f8bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3088431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27eb2f10cf8e7a02166067ce4be4c23cf082b2aac2b095ff1eef4dc4a412cd2`

```dockerfile
```

-	Layers:
	-	`sha256:9b1478d13781559fddc68c09900363ba774b03fdcb945b6ed1af309b1f220b74`  
		Last Modified: Tue, 02 Jul 2024 03:20:28 GMT  
		Size: 3.1 MB (3069466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4302deedc27d113021b672b7b1538cc3475e0a372dc566a82f7b0d1aa9918bf4`  
		Last Modified: Tue, 02 Jul 2024 03:20:29 GMT  
		Size: 19.0 KB (18965 bytes)  
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
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:e0ccbaa30614886d3e7bee45be3a60a162cb8ca2e518fc8edb9f82d5eff8d25d
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
$ docker pull neo4j@sha256:549108e9f1b3c78b404ab0b0c3591cb60bff978c6f9cf32f5a3bddd6a3925fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289229765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb8ab64aa1c1f2bec01ac5eae416815831ec9911e87bf52e4020be2ec10bfb`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348eefcb70b9d1dbda4c88ba7790edb7ab008799eefe96e3c06e12dbfb8ff41`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 127.0 MB (126972845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f4be64e9e4295aaa8511e4fb3480cd6399d00b1944dc16500543cfc82b38c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bfcc826d9f24aed24a32016ea3851acb2d47ef9c192f4427e9f5ecd0791d8`

```dockerfile
```

-	Layers:
	-	`sha256:2233495a237613e3fa6a9c8bff16dc87259ed4edadcdfbd6c0593ddd070d9c1a`  
		Last Modified: Thu, 27 Jun 2024 18:58:43 GMT  
		Size: 5.0 MB (5031689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5dc4e9cb5a4c309e116bd12ed324d366cb313abc8595bf9703d335a06cdf20`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:95a9f6a81621764c306d7db240a74e8db6e506a9d91a6de3ebd26ffb57921de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1885fc3993975f6e5294aa5a8350c6e136ba38fac44df858ee2f05f3cde5bbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4da94ae2dbf9cade7a3c1cab384b387431473be89ab9623a2bff3800711c605`
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
	-	`sha256:7ab61c61aa4493d4aa7bd7ec2af0850b2577ac9564fe54e1a11e90846bed09dd`  
		Last Modified: Tue, 02 Jul 2024 03:04:37 GMT  
		Size: 145.1 MB (145095133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7f380018685529bb822925deb452109e194f536cf769274cd75cc5ca8a396`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552a92cd3328215ba191d535b1b2b7547481ee0b019459b699636dba67bc81d`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847555bf22235039ce550af17d4e9f6f436996fd74d346bc3997763ade32426`  
		Last Modified: Tue, 02 Jul 2024 03:04:41 GMT  
		Size: 412.8 MB (412831201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e385e91a6740b359c2f454dc9f761e0e21f4be93b1b0089a077a4567133888ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e2b64e8ffa73fd8d54ebfa9c2e12aeee984423a67705c670ec810e98cdc0b`

```dockerfile
```

-	Layers:
	-	`sha256:6c15b45ebb7fc4d287a591abc1efc1e847026a798c468605538a427e06654c5a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee800270424fb8ee2e3188e7325590621ce4ad02c0ff9c7069efc07de82a42a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e0c213862d611e4f1d143f9d5591c60cea7f295f18df67715c8e9a64dd078c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e8a856e83bb0885865a55e47f032d8e355317e259c371cedc38700d2e881b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97dce02e215454cb5523c4dea5725359c02c51702f54d3a9e2f26f200c8838`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9bf342ee429c135b9074072ffb2fed5498f888fe4567989ced5b77dd6cdd6`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc613b8fbaccc1c6ab3b2a9deafaa840c8d8ab6ebffc31ff551d0a020bb339c0`  
		Last Modified: Thu, 27 Jun 2024 18:57:20 GMT  
		Size: 412.8 MB (412796340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6782b7f1422c1f7b2175cd58459940bdf5988080b6f17351e29708b5d7a4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc435f5f7b69e2234b02b874310ac58eceb4b5f9e4ccca48e845a4d3d57ada8`

```dockerfile
```

-	Layers:
	-	`sha256:d482a474c9e726206cfeeef0f3223399007687b8e82038f405c216e684dee206`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.2 MB (3188446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0925b8f9d4766ecdc8667be939868da8522dd244409ee41f5e833b325df5a056`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:95a9f6a81621764c306d7db240a74e8db6e506a9d91a6de3ebd26ffb57921de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1885fc3993975f6e5294aa5a8350c6e136ba38fac44df858ee2f05f3cde5bbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4da94ae2dbf9cade7a3c1cab384b387431473be89ab9623a2bff3800711c605`
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
	-	`sha256:7ab61c61aa4493d4aa7bd7ec2af0850b2577ac9564fe54e1a11e90846bed09dd`  
		Last Modified: Tue, 02 Jul 2024 03:04:37 GMT  
		Size: 145.1 MB (145095133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7f380018685529bb822925deb452109e194f536cf769274cd75cc5ca8a396`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552a92cd3328215ba191d535b1b2b7547481ee0b019459b699636dba67bc81d`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847555bf22235039ce550af17d4e9f6f436996fd74d346bc3997763ade32426`  
		Last Modified: Tue, 02 Jul 2024 03:04:41 GMT  
		Size: 412.8 MB (412831201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e385e91a6740b359c2f454dc9f761e0e21f4be93b1b0089a077a4567133888ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e2b64e8ffa73fd8d54ebfa9c2e12aeee984423a67705c670ec810e98cdc0b`

```dockerfile
```

-	Layers:
	-	`sha256:6c15b45ebb7fc4d287a591abc1efc1e847026a798c468605538a427e06654c5a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee800270424fb8ee2e3188e7325590621ce4ad02c0ff9c7069efc07de82a42a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e0c213862d611e4f1d143f9d5591c60cea7f295f18df67715c8e9a64dd078c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e8a856e83bb0885865a55e47f032d8e355317e259c371cedc38700d2e881b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97dce02e215454cb5523c4dea5725359c02c51702f54d3a9e2f26f200c8838`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9bf342ee429c135b9074072ffb2fed5498f888fe4567989ced5b77dd6cdd6`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc613b8fbaccc1c6ab3b2a9deafaa840c8d8ab6ebffc31ff551d0a020bb339c0`  
		Last Modified: Thu, 27 Jun 2024 18:57:20 GMT  
		Size: 412.8 MB (412796340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6782b7f1422c1f7b2175cd58459940bdf5988080b6f17351e29708b5d7a4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc435f5f7b69e2234b02b874310ac58eceb4b5f9e4ccca48e845a4d3d57ada8`

```dockerfile
```

-	Layers:
	-	`sha256:d482a474c9e726206cfeeef0f3223399007687b8e82038f405c216e684dee206`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.2 MB (3188446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0925b8f9d4766ecdc8667be939868da8522dd244409ee41f5e833b325df5a056`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:91ceeaecdf5eca4c4a3606b64901d34e1f2160f7a485dc13ef0ff61b707177d0
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
$ docker pull neo4j@sha256:a30563b37c9fcf0d1d6532fdf51bf6a2d2520dbf1aa7d19d2482c2d80d0d2e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.2 MB (572157378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e248f014e8cfc5b4b0af4e3e706a4920fac2c19fc1c8574af4a662a7f9e8d7b`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f09bd1a32a488176072aaa6dd0c3f1138ff0def895f0a18b45cfaabd3f608`  
		Last Modified: Thu, 27 Jun 2024 18:59:49 GMT  
		Size: 409.9 MB (409900458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:edff0992fd0ba986870fb3803eb7e500a8805c0167d59816163328f712fbaa63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92792e063117b1cf03353b0f9f6a671685742530f77b219c1303df28811a1fb`

```dockerfile
```

-	Layers:
	-	`sha256:224ab6e15b8556cff8e496c287c1c587b2bbbd6d989a59c1b5a9eb4f4ad86f15`  
		Last Modified: Thu, 27 Jun 2024 18:59:41 GMT  
		Size: 5.3 MB (5253082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8acfd2b76b8d54e617a9aec21cf48da3107ff2d47067fd20995572d5f05729`  
		Last Modified: Thu, 27 Jun 2024 18:59:40 GMT  
		Size: 20.9 KB (20851 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:e0ccbaa30614886d3e7bee45be3a60a162cb8ca2e518fc8edb9f82d5eff8d25d
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
$ docker pull neo4j@sha256:549108e9f1b3c78b404ab0b0c3591cb60bff978c6f9cf32f5a3bddd6a3925fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289229765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb8ab64aa1c1f2bec01ac5eae416815831ec9911e87bf52e4020be2ec10bfb`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348eefcb70b9d1dbda4c88ba7790edb7ab008799eefe96e3c06e12dbfb8ff41`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 127.0 MB (126972845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f4be64e9e4295aaa8511e4fb3480cd6399d00b1944dc16500543cfc82b38c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bfcc826d9f24aed24a32016ea3851acb2d47ef9c192f4427e9f5ecd0791d8`

```dockerfile
```

-	Layers:
	-	`sha256:2233495a237613e3fa6a9c8bff16dc87259ed4edadcdfbd6c0593ddd070d9c1a`  
		Last Modified: Thu, 27 Jun 2024 18:58:43 GMT  
		Size: 5.0 MB (5031689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5dc4e9cb5a4c309e116bd12ed324d366cb313abc8595bf9703d335a06cdf20`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-bullseye`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-community`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-community-bullseye`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-community-ubi9`

```console
$ docker pull neo4j@sha256:e0ccbaa30614886d3e7bee45be3a60a162cb8ca2e518fc8edb9f82d5eff8d25d
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
$ docker pull neo4j@sha256:549108e9f1b3c78b404ab0b0c3591cb60bff978c6f9cf32f5a3bddd6a3925fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289229765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb8ab64aa1c1f2bec01ac5eae416815831ec9911e87bf52e4020be2ec10bfb`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348eefcb70b9d1dbda4c88ba7790edb7ab008799eefe96e3c06e12dbfb8ff41`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 127.0 MB (126972845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f4be64e9e4295aaa8511e4fb3480cd6399d00b1944dc16500543cfc82b38c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bfcc826d9f24aed24a32016ea3851acb2d47ef9c192f4427e9f5ecd0791d8`

```dockerfile
```

-	Layers:
	-	`sha256:2233495a237613e3fa6a9c8bff16dc87259ed4edadcdfbd6c0593ddd070d9c1a`  
		Last Modified: Thu, 27 Jun 2024 18:58:43 GMT  
		Size: 5.0 MB (5031689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5dc4e9cb5a4c309e116bd12ed324d366cb313abc8595bf9703d335a06cdf20`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-enterprise`

```console
$ docker pull neo4j@sha256:95a9f6a81621764c306d7db240a74e8db6e506a9d91a6de3ebd26ffb57921de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1885fc3993975f6e5294aa5a8350c6e136ba38fac44df858ee2f05f3cde5bbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4da94ae2dbf9cade7a3c1cab384b387431473be89ab9623a2bff3800711c605`
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
	-	`sha256:7ab61c61aa4493d4aa7bd7ec2af0850b2577ac9564fe54e1a11e90846bed09dd`  
		Last Modified: Tue, 02 Jul 2024 03:04:37 GMT  
		Size: 145.1 MB (145095133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7f380018685529bb822925deb452109e194f536cf769274cd75cc5ca8a396`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552a92cd3328215ba191d535b1b2b7547481ee0b019459b699636dba67bc81d`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847555bf22235039ce550af17d4e9f6f436996fd74d346bc3997763ade32426`  
		Last Modified: Tue, 02 Jul 2024 03:04:41 GMT  
		Size: 412.8 MB (412831201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e385e91a6740b359c2f454dc9f761e0e21f4be93b1b0089a077a4567133888ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e2b64e8ffa73fd8d54ebfa9c2e12aeee984423a67705c670ec810e98cdc0b`

```dockerfile
```

-	Layers:
	-	`sha256:6c15b45ebb7fc4d287a591abc1efc1e847026a798c468605538a427e06654c5a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee800270424fb8ee2e3188e7325590621ce4ad02c0ff9c7069efc07de82a42a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e0c213862d611e4f1d143f9d5591c60cea7f295f18df67715c8e9a64dd078c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e8a856e83bb0885865a55e47f032d8e355317e259c371cedc38700d2e881b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97dce02e215454cb5523c4dea5725359c02c51702f54d3a9e2f26f200c8838`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9bf342ee429c135b9074072ffb2fed5498f888fe4567989ced5b77dd6cdd6`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc613b8fbaccc1c6ab3b2a9deafaa840c8d8ab6ebffc31ff551d0a020bb339c0`  
		Last Modified: Thu, 27 Jun 2024 18:57:20 GMT  
		Size: 412.8 MB (412796340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6782b7f1422c1f7b2175cd58459940bdf5988080b6f17351e29708b5d7a4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc435f5f7b69e2234b02b874310ac58eceb4b5f9e4ccca48e845a4d3d57ada8`

```dockerfile
```

-	Layers:
	-	`sha256:d482a474c9e726206cfeeef0f3223399007687b8e82038f405c216e684dee206`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.2 MB (3188446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0925b8f9d4766ecdc8667be939868da8522dd244409ee41f5e833b325df5a056`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:95a9f6a81621764c306d7db240a74e8db6e506a9d91a6de3ebd26ffb57921de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1885fc3993975f6e5294aa5a8350c6e136ba38fac44df858ee2f05f3cde5bbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4da94ae2dbf9cade7a3c1cab384b387431473be89ab9623a2bff3800711c605`
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
	-	`sha256:7ab61c61aa4493d4aa7bd7ec2af0850b2577ac9564fe54e1a11e90846bed09dd`  
		Last Modified: Tue, 02 Jul 2024 03:04:37 GMT  
		Size: 145.1 MB (145095133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7f380018685529bb822925deb452109e194f536cf769274cd75cc5ca8a396`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552a92cd3328215ba191d535b1b2b7547481ee0b019459b699636dba67bc81d`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847555bf22235039ce550af17d4e9f6f436996fd74d346bc3997763ade32426`  
		Last Modified: Tue, 02 Jul 2024 03:04:41 GMT  
		Size: 412.8 MB (412831201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e385e91a6740b359c2f454dc9f761e0e21f4be93b1b0089a077a4567133888ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e2b64e8ffa73fd8d54ebfa9c2e12aeee984423a67705c670ec810e98cdc0b`

```dockerfile
```

-	Layers:
	-	`sha256:6c15b45ebb7fc4d287a591abc1efc1e847026a798c468605538a427e06654c5a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee800270424fb8ee2e3188e7325590621ce4ad02c0ff9c7069efc07de82a42a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e0c213862d611e4f1d143f9d5591c60cea7f295f18df67715c8e9a64dd078c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e8a856e83bb0885865a55e47f032d8e355317e259c371cedc38700d2e881b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97dce02e215454cb5523c4dea5725359c02c51702f54d3a9e2f26f200c8838`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9bf342ee429c135b9074072ffb2fed5498f888fe4567989ced5b77dd6cdd6`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc613b8fbaccc1c6ab3b2a9deafaa840c8d8ab6ebffc31ff551d0a020bb339c0`  
		Last Modified: Thu, 27 Jun 2024 18:57:20 GMT  
		Size: 412.8 MB (412796340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6782b7f1422c1f7b2175cd58459940bdf5988080b6f17351e29708b5d7a4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc435f5f7b69e2234b02b874310ac58eceb4b5f9e4ccca48e845a4d3d57ada8`

```dockerfile
```

-	Layers:
	-	`sha256:d482a474c9e726206cfeeef0f3223399007687b8e82038f405c216e684dee206`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.2 MB (3188446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0925b8f9d4766ecdc8667be939868da8522dd244409ee41f5e833b325df5a056`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:91ceeaecdf5eca4c4a3606b64901d34e1f2160f7a485dc13ef0ff61b707177d0
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
$ docker pull neo4j@sha256:a30563b37c9fcf0d1d6532fdf51bf6a2d2520dbf1aa7d19d2482c2d80d0d2e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.2 MB (572157378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e248f014e8cfc5b4b0af4e3e706a4920fac2c19fc1c8574af4a662a7f9e8d7b`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f09bd1a32a488176072aaa6dd0c3f1138ff0def895f0a18b45cfaabd3f608`  
		Last Modified: Thu, 27 Jun 2024 18:59:49 GMT  
		Size: 409.9 MB (409900458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:edff0992fd0ba986870fb3803eb7e500a8805c0167d59816163328f712fbaa63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92792e063117b1cf03353b0f9f6a671685742530f77b219c1303df28811a1fb`

```dockerfile
```

-	Layers:
	-	`sha256:224ab6e15b8556cff8e496c287c1c587b2bbbd6d989a59c1b5a9eb4f4ad86f15`  
		Last Modified: Thu, 27 Jun 2024 18:59:41 GMT  
		Size: 5.3 MB (5253082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8acfd2b76b8d54e617a9aec21cf48da3107ff2d47067fd20995572d5f05729`  
		Last Modified: Thu, 27 Jun 2024 18:59:40 GMT  
		Size: 20.9 KB (20851 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21-ubi9`

```console
$ docker pull neo4j@sha256:e0ccbaa30614886d3e7bee45be3a60a162cb8ca2e518fc8edb9f82d5eff8d25d
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
$ docker pull neo4j@sha256:549108e9f1b3c78b404ab0b0c3591cb60bff978c6f9cf32f5a3bddd6a3925fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289229765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb8ab64aa1c1f2bec01ac5eae416815831ec9911e87bf52e4020be2ec10bfb`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348eefcb70b9d1dbda4c88ba7790edb7ab008799eefe96e3c06e12dbfb8ff41`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 127.0 MB (126972845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f4be64e9e4295aaa8511e4fb3480cd6399d00b1944dc16500543cfc82b38c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bfcc826d9f24aed24a32016ea3851acb2d47ef9c192f4427e9f5ecd0791d8`

```dockerfile
```

-	Layers:
	-	`sha256:2233495a237613e3fa6a9c8bff16dc87259ed4edadcdfbd6c0593ddd070d9c1a`  
		Last Modified: Thu, 27 Jun 2024 18:58:43 GMT  
		Size: 5.0 MB (5031689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5dc4e9cb5a4c309e116bd12ed324d366cb313abc8595bf9703d335a06cdf20`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.0`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.0` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.0-bullseye`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.0-community`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.0-community-bullseye`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.0-community-ubi9`

```console
$ docker pull neo4j@sha256:e0ccbaa30614886d3e7bee45be3a60a162cb8ca2e518fc8edb9f82d5eff8d25d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.0-community-ubi9` - linux; amd64

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

### `neo4j:5.21.0-community-ubi9` - unknown; unknown

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

### `neo4j:5.21.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:549108e9f1b3c78b404ab0b0c3591cb60bff978c6f9cf32f5a3bddd6a3925fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289229765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb8ab64aa1c1f2bec01ac5eae416815831ec9911e87bf52e4020be2ec10bfb`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348eefcb70b9d1dbda4c88ba7790edb7ab008799eefe96e3c06e12dbfb8ff41`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 127.0 MB (126972845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f4be64e9e4295aaa8511e4fb3480cd6399d00b1944dc16500543cfc82b38c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bfcc826d9f24aed24a32016ea3851acb2d47ef9c192f4427e9f5ecd0791d8`

```dockerfile
```

-	Layers:
	-	`sha256:2233495a237613e3fa6a9c8bff16dc87259ed4edadcdfbd6c0593ddd070d9c1a`  
		Last Modified: Thu, 27 Jun 2024 18:58:43 GMT  
		Size: 5.0 MB (5031689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5dc4e9cb5a4c309e116bd12ed324d366cb313abc8595bf9703d335a06cdf20`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.0-enterprise`

```console
$ docker pull neo4j@sha256:95a9f6a81621764c306d7db240a74e8db6e506a9d91a6de3ebd26ffb57921de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1885fc3993975f6e5294aa5a8350c6e136ba38fac44df858ee2f05f3cde5bbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4da94ae2dbf9cade7a3c1cab384b387431473be89ab9623a2bff3800711c605`
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
	-	`sha256:7ab61c61aa4493d4aa7bd7ec2af0850b2577ac9564fe54e1a11e90846bed09dd`  
		Last Modified: Tue, 02 Jul 2024 03:04:37 GMT  
		Size: 145.1 MB (145095133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7f380018685529bb822925deb452109e194f536cf769274cd75cc5ca8a396`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552a92cd3328215ba191d535b1b2b7547481ee0b019459b699636dba67bc81d`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847555bf22235039ce550af17d4e9f6f436996fd74d346bc3997763ade32426`  
		Last Modified: Tue, 02 Jul 2024 03:04:41 GMT  
		Size: 412.8 MB (412831201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e385e91a6740b359c2f454dc9f761e0e21f4be93b1b0089a077a4567133888ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e2b64e8ffa73fd8d54ebfa9c2e12aeee984423a67705c670ec810e98cdc0b`

```dockerfile
```

-	Layers:
	-	`sha256:6c15b45ebb7fc4d287a591abc1efc1e847026a798c468605538a427e06654c5a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee800270424fb8ee2e3188e7325590621ce4ad02c0ff9c7069efc07de82a42a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e0c213862d611e4f1d143f9d5591c60cea7f295f18df67715c8e9a64dd078c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e8a856e83bb0885865a55e47f032d8e355317e259c371cedc38700d2e881b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97dce02e215454cb5523c4dea5725359c02c51702f54d3a9e2f26f200c8838`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9bf342ee429c135b9074072ffb2fed5498f888fe4567989ced5b77dd6cdd6`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc613b8fbaccc1c6ab3b2a9deafaa840c8d8ab6ebffc31ff551d0a020bb339c0`  
		Last Modified: Thu, 27 Jun 2024 18:57:20 GMT  
		Size: 412.8 MB (412796340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6782b7f1422c1f7b2175cd58459940bdf5988080b6f17351e29708b5d7a4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc435f5f7b69e2234b02b874310ac58eceb4b5f9e4ccca48e845a4d3d57ada8`

```dockerfile
```

-	Layers:
	-	`sha256:d482a474c9e726206cfeeef0f3223399007687b8e82038f405c216e684dee206`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.2 MB (3188446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0925b8f9d4766ecdc8667be939868da8522dd244409ee41f5e833b325df5a056`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:95a9f6a81621764c306d7db240a74e8db6e506a9d91a6de3ebd26ffb57921de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1885fc3993975f6e5294aa5a8350c6e136ba38fac44df858ee2f05f3cde5bbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4da94ae2dbf9cade7a3c1cab384b387431473be89ab9623a2bff3800711c605`
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
	-	`sha256:7ab61c61aa4493d4aa7bd7ec2af0850b2577ac9564fe54e1a11e90846bed09dd`  
		Last Modified: Tue, 02 Jul 2024 03:04:37 GMT  
		Size: 145.1 MB (145095133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7f380018685529bb822925deb452109e194f536cf769274cd75cc5ca8a396`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552a92cd3328215ba191d535b1b2b7547481ee0b019459b699636dba67bc81d`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847555bf22235039ce550af17d4e9f6f436996fd74d346bc3997763ade32426`  
		Last Modified: Tue, 02 Jul 2024 03:04:41 GMT  
		Size: 412.8 MB (412831201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e385e91a6740b359c2f454dc9f761e0e21f4be93b1b0089a077a4567133888ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e2b64e8ffa73fd8d54ebfa9c2e12aeee984423a67705c670ec810e98cdc0b`

```dockerfile
```

-	Layers:
	-	`sha256:6c15b45ebb7fc4d287a591abc1efc1e847026a798c468605538a427e06654c5a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee800270424fb8ee2e3188e7325590621ce4ad02c0ff9c7069efc07de82a42a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.21.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e0c213862d611e4f1d143f9d5591c60cea7f295f18df67715c8e9a64dd078c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e8a856e83bb0885865a55e47f032d8e355317e259c371cedc38700d2e881b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97dce02e215454cb5523c4dea5725359c02c51702f54d3a9e2f26f200c8838`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9bf342ee429c135b9074072ffb2fed5498f888fe4567989ced5b77dd6cdd6`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc613b8fbaccc1c6ab3b2a9deafaa840c8d8ab6ebffc31ff551d0a020bb339c0`  
		Last Modified: Thu, 27 Jun 2024 18:57:20 GMT  
		Size: 412.8 MB (412796340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6782b7f1422c1f7b2175cd58459940bdf5988080b6f17351e29708b5d7a4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc435f5f7b69e2234b02b874310ac58eceb4b5f9e4ccca48e845a4d3d57ada8`

```dockerfile
```

-	Layers:
	-	`sha256:d482a474c9e726206cfeeef0f3223399007687b8e82038f405c216e684dee206`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.2 MB (3188446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0925b8f9d4766ecdc8667be939868da8522dd244409ee41f5e833b325df5a056`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:91ceeaecdf5eca4c4a3606b64901d34e1f2160f7a485dc13ef0ff61b707177d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.0-enterprise-ubi9` - linux; amd64

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

### `neo4j:5.21.0-enterprise-ubi9` - unknown; unknown

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

### `neo4j:5.21.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a30563b37c9fcf0d1d6532fdf51bf6a2d2520dbf1aa7d19d2482c2d80d0d2e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.2 MB (572157378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e248f014e8cfc5b4b0af4e3e706a4920fac2c19fc1c8574af4a662a7f9e8d7b`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f09bd1a32a488176072aaa6dd0c3f1138ff0def895f0a18b45cfaabd3f608`  
		Last Modified: Thu, 27 Jun 2024 18:59:49 GMT  
		Size: 409.9 MB (409900458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:edff0992fd0ba986870fb3803eb7e500a8805c0167d59816163328f712fbaa63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92792e063117b1cf03353b0f9f6a671685742530f77b219c1303df28811a1fb`

```dockerfile
```

-	Layers:
	-	`sha256:224ab6e15b8556cff8e496c287c1c587b2bbbd6d989a59c1b5a9eb4f4ad86f15`  
		Last Modified: Thu, 27 Jun 2024 18:59:41 GMT  
		Size: 5.3 MB (5253082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8acfd2b76b8d54e617a9aec21cf48da3107ff2d47067fd20995572d5f05729`  
		Last Modified: Thu, 27 Jun 2024 18:59:40 GMT  
		Size: 20.9 KB (20851 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.21.0-ubi9`

```console
$ docker pull neo4j@sha256:e0ccbaa30614886d3e7bee45be3a60a162cb8ca2e518fc8edb9f82d5eff8d25d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.21.0-ubi9` - linux; amd64

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

### `neo4j:5.21.0-ubi9` - unknown; unknown

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

### `neo4j:5.21.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:549108e9f1b3c78b404ab0b0c3591cb60bff978c6f9cf32f5a3bddd6a3925fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289229765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb8ab64aa1c1f2bec01ac5eae416815831ec9911e87bf52e4020be2ec10bfb`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348eefcb70b9d1dbda4c88ba7790edb7ab008799eefe96e3c06e12dbfb8ff41`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 127.0 MB (126972845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.21.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f4be64e9e4295aaa8511e4fb3480cd6399d00b1944dc16500543cfc82b38c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bfcc826d9f24aed24a32016ea3851acb2d47ef9c192f4427e9f5ecd0791d8`

```dockerfile
```

-	Layers:
	-	`sha256:2233495a237613e3fa6a9c8bff16dc87259ed4edadcdfbd6c0593ddd070d9c1a`  
		Last Modified: Thu, 27 Jun 2024 18:58:43 GMT  
		Size: 5.0 MB (5031689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5dc4e9cb5a4c309e116bd12ed324d366cb313abc8595bf9703d335a06cdf20`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:e0ccbaa30614886d3e7bee45be3a60a162cb8ca2e518fc8edb9f82d5eff8d25d
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
$ docker pull neo4j@sha256:549108e9f1b3c78b404ab0b0c3591cb60bff978c6f9cf32f5a3bddd6a3925fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289229765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb8ab64aa1c1f2bec01ac5eae416815831ec9911e87bf52e4020be2ec10bfb`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348eefcb70b9d1dbda4c88ba7790edb7ab008799eefe96e3c06e12dbfb8ff41`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 127.0 MB (126972845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f4be64e9e4295aaa8511e4fb3480cd6399d00b1944dc16500543cfc82b38c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bfcc826d9f24aed24a32016ea3851acb2d47ef9c192f4427e9f5ecd0791d8`

```dockerfile
```

-	Layers:
	-	`sha256:2233495a237613e3fa6a9c8bff16dc87259ed4edadcdfbd6c0593ddd070d9c1a`  
		Last Modified: Thu, 27 Jun 2024 18:58:43 GMT  
		Size: 5.0 MB (5031689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5dc4e9cb5a4c309e116bd12ed324d366cb313abc8595bf9703d335a06cdf20`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:95a9f6a81621764c306d7db240a74e8db6e506a9d91a6de3ebd26ffb57921de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1885fc3993975f6e5294aa5a8350c6e136ba38fac44df858ee2f05f3cde5bbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4da94ae2dbf9cade7a3c1cab384b387431473be89ab9623a2bff3800711c605`
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
	-	`sha256:7ab61c61aa4493d4aa7bd7ec2af0850b2577ac9564fe54e1a11e90846bed09dd`  
		Last Modified: Tue, 02 Jul 2024 03:04:37 GMT  
		Size: 145.1 MB (145095133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7f380018685529bb822925deb452109e194f536cf769274cd75cc5ca8a396`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552a92cd3328215ba191d535b1b2b7547481ee0b019459b699636dba67bc81d`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847555bf22235039ce550af17d4e9f6f436996fd74d346bc3997763ade32426`  
		Last Modified: Tue, 02 Jul 2024 03:04:41 GMT  
		Size: 412.8 MB (412831201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e385e91a6740b359c2f454dc9f761e0e21f4be93b1b0089a077a4567133888ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e2b64e8ffa73fd8d54ebfa9c2e12aeee984423a67705c670ec810e98cdc0b`

```dockerfile
```

-	Layers:
	-	`sha256:6c15b45ebb7fc4d287a591abc1efc1e847026a798c468605538a427e06654c5a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee800270424fb8ee2e3188e7325590621ce4ad02c0ff9c7069efc07de82a42a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e0c213862d611e4f1d143f9d5591c60cea7f295f18df67715c8e9a64dd078c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e8a856e83bb0885865a55e47f032d8e355317e259c371cedc38700d2e881b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97dce02e215454cb5523c4dea5725359c02c51702f54d3a9e2f26f200c8838`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9bf342ee429c135b9074072ffb2fed5498f888fe4567989ced5b77dd6cdd6`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc613b8fbaccc1c6ab3b2a9deafaa840c8d8ab6ebffc31ff551d0a020bb339c0`  
		Last Modified: Thu, 27 Jun 2024 18:57:20 GMT  
		Size: 412.8 MB (412796340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6782b7f1422c1f7b2175cd58459940bdf5988080b6f17351e29708b5d7a4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc435f5f7b69e2234b02b874310ac58eceb4b5f9e4ccca48e845a4d3d57ada8`

```dockerfile
```

-	Layers:
	-	`sha256:d482a474c9e726206cfeeef0f3223399007687b8e82038f405c216e684dee206`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.2 MB (3188446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0925b8f9d4766ecdc8667be939868da8522dd244409ee41f5e833b325df5a056`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:95a9f6a81621764c306d7db240a74e8db6e506a9d91a6de3ebd26ffb57921de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1885fc3993975f6e5294aa5a8350c6e136ba38fac44df858ee2f05f3cde5bbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.4 MB (589362112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4da94ae2dbf9cade7a3c1cab384b387431473be89ab9623a2bff3800711c605`
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
	-	`sha256:7ab61c61aa4493d4aa7bd7ec2af0850b2577ac9564fe54e1a11e90846bed09dd`  
		Last Modified: Tue, 02 Jul 2024 03:04:37 GMT  
		Size: 145.1 MB (145095133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c7f380018685529bb822925deb452109e194f536cf769274cd75cc5ca8a396`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552a92cd3328215ba191d535b1b2b7547481ee0b019459b699636dba67bc81d`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7847555bf22235039ce550af17d4e9f6f436996fd74d346bc3997763ade32426`  
		Last Modified: Tue, 02 Jul 2024 03:04:41 GMT  
		Size: 412.8 MB (412831201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e385e91a6740b359c2f454dc9f761e0e21f4be93b1b0089a077a4567133888ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3209097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852e2b64e8ffa73fd8d54ebfa9c2e12aeee984423a67705c670ec810e98cdc0b`

```dockerfile
```

-	Layers:
	-	`sha256:6c15b45ebb7fc4d287a591abc1efc1e847026a798c468605538a427e06654c5a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 3.2 MB (3188137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee800270424fb8ee2e3188e7325590621ce4ad02c0ff9c7069efc07de82a42a`  
		Last Modified: Tue, 02 Jul 2024 03:04:35 GMT  
		Size: 21.0 KB (20960 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2e0c213862d611e4f1d143f9d5591c60cea7f295f18df67715c8e9a64dd078c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.8 MB (586789635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747e8a856e83bb0885865a55e47f032d8e355317e259c371cedc38700d2e881b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b97dce02e215454cb5523c4dea5725359c02c51702f54d3a9e2f26f200c8838`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.9 KB (3873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b9bf342ee429c135b9074072ffb2fed5498f888fe4567989ced5b77dd6cdd6`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc613b8fbaccc1c6ab3b2a9deafaa840c8d8ab6ebffc31ff551d0a020bb339c0`  
		Last Modified: Thu, 27 Jun 2024 18:57:20 GMT  
		Size: 412.8 MB (412796340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b6782b7f1422c1f7b2175cd58459940bdf5988080b6f17351e29708b5d7a4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc435f5f7b69e2234b02b874310ac58eceb4b5f9e4ccca48e845a4d3d57ada8`

```dockerfile
```

-	Layers:
	-	`sha256:d482a474c9e726206cfeeef0f3223399007687b8e82038f405c216e684dee206`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 3.2 MB (3188446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0925b8f9d4766ecdc8667be939868da8522dd244409ee41f5e833b325df5a056`  
		Last Modified: Thu, 27 Jun 2024 18:57:11 GMT  
		Size: 21.6 KB (21560 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:91ceeaecdf5eca4c4a3606b64901d34e1f2160f7a485dc13ef0ff61b707177d0
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
$ docker pull neo4j@sha256:a30563b37c9fcf0d1d6532fdf51bf6a2d2520dbf1aa7d19d2482c2d80d0d2e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.2 MB (572157378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e248f014e8cfc5b4b0af4e3e706a4920fac2c19fc1c8574af4a662a7f9e8d7b`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8f09bd1a32a488176072aaa6dd0c3f1138ff0def895f0a18b45cfaabd3f608`  
		Last Modified: Thu, 27 Jun 2024 18:59:49 GMT  
		Size: 409.9 MB (409900458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:edff0992fd0ba986870fb3803eb7e500a8805c0167d59816163328f712fbaa63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92792e063117b1cf03353b0f9f6a671685742530f77b219c1303df28811a1fb`

```dockerfile
```

-	Layers:
	-	`sha256:224ab6e15b8556cff8e496c287c1c587b2bbbd6d989a59c1b5a9eb4f4ad86f15`  
		Last Modified: Thu, 27 Jun 2024 18:59:41 GMT  
		Size: 5.3 MB (5253082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8acfd2b76b8d54e617a9aec21cf48da3107ff2d47067fd20995572d5f05729`  
		Last Modified: Thu, 27 Jun 2024 18:59:40 GMT  
		Size: 20.9 KB (20851 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:418c41b829a9efd86bd09017ee9b28ef4e64759c6d688ef26980792aa96d64e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:2ef073774b72aa33b3673f09cd0af5c0854fcdbe7d4b3bd19ec3cd3170be7220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306430532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4000ac205690a4ffb65438deac910ac1ee172b7df1d954268d1dffe65b7df448`
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
	-	`sha256:542dbf574ac3f6e7b25a93b0140987155520512bcff168e003d2efdb4a4afcb8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 145.1 MB (145095107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc5a70b271965ae1d98d138e503d7489e310fd2aa42373a77cece8ef32ff091`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e7fd626e733386cae71ff40e720c61a42338e422a0021cb1b2e85348536e1`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d56cfc0e7d2293f110829fb2e3ed07af48afb39ec8dd072cb40dc4871646e8`  
		Last Modified: Tue, 02 Jul 2024 03:04:14 GMT  
		Size: 129.9 MB (129899646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e940fdd398e1fc4bb63c8b949a410b83d08261bcc99b3ef6ced1c212405bab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631c4f55852bbeef41b04725647e800b82226569eaf94f253f2b52a6b9212cc4`

```dockerfile
```

-	Layers:
	-	`sha256:8776828cae56687fe69be24fea3d57d0a7a8040a0da7964a4328531c2eb43cc4`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 3.0 MB (2967890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95aee782a8f504d8cf15483392e4e6cae5924c3f4b2ebf57d9e90b7553fb986f`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 23.3 KB (23328 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:45ef0824f41a2bab0e196558cd1e7164beea9fbe0df92d615af786a38cb71ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303863095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee200c8e1e14b4820c7f7581fe671e284f29ac9d3ac6d87c49cc5dff1120763`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:06 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 13 Jun 2024 00:40:06 GMT
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec69747e15e5ce852d8bcb00992306d33ddb207e24900a65fdfb623ddd512e21`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 143.9 MB (143892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3850f5fd6366e203f151cb710c3418988466ec7f9b017c10a7045867888f139a`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddc5ce8cbef080759ac3c765ae521faf252b845604fa7e5a3a51570ab227760`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 9.6 KB (9633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1aeea181ee9c08b81c8ade6a2985db100e1836fb04b069713a5816940a1e43`  
		Last Modified: Thu, 27 Jun 2024 18:55:58 GMT  
		Size: 129.9 MB (129869805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:93a8a2d0e5392e4f7d8cb946f26f73bcc957c092d6cce446034c3c2666c5fc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e858c0c551e72940b6e7f679bac9b624e92374330419c5696caa2f35e7d398`

```dockerfile
```

-	Layers:
	-	`sha256:2c83f7504793d2e59e4a6ef33303ac8dbec01f0278bded96378d6f677162ef80`  
		Last Modified: Thu, 27 Jun 2024 18:55:55 GMT  
		Size: 3.0 MB (2968295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09edd92520917eb4cec7bc6a55f9cd219ed82095a4659056a5fec7e227ed1c8`  
		Last Modified: Thu, 27 Jun 2024 18:55:54 GMT  
		Size: 24.0 KB (24026 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:e0ccbaa30614886d3e7bee45be3a60a162cb8ca2e518fc8edb9f82d5eff8d25d
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
$ docker pull neo4j@sha256:549108e9f1b3c78b404ab0b0c3591cb60bff978c6f9cf32f5a3bddd6a3925fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289229765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfb8ab64aa1c1f2bec01ac5eae416815831ec9911e87bf52e4020be2ec10bfb`
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
	-	`sha256:12041dc61838218321383650a1641a04f91cba754a7465ce28de10da7d0af785`  
		Last Modified: Thu, 13 Jun 2024 09:26:57 GMT  
		Size: 37.1 MB (37118393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d77dc2f8c5b7774369e14b1c5b58b124047ade53a30b1ab0cccbdbfdc9c808`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 125.1 MB (125128863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15479eeb359913a3e71bbd26bf9686b28acb4502e4ecd8e09ecfaf2670740c0a`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348eefcb70b9d1dbda4c88ba7790edb7ab008799eefe96e3c06e12dbfb8ff41`  
		Last Modified: Thu, 27 Jun 2024 18:58:45 GMT  
		Size: 127.0 MB (126972845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f4be64e9e4295aaa8511e4fb3480cd6399d00b1944dc16500543cfc82b38c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367bfcc826d9f24aed24a32016ea3851acb2d47ef9c192f4427e9f5ecd0791d8`

```dockerfile
```

-	Layers:
	-	`sha256:2233495a237613e3fa6a9c8bff16dc87259ed4edadcdfbd6c0593ddd070d9c1a`  
		Last Modified: Thu, 27 Jun 2024 18:58:43 GMT  
		Size: 5.0 MB (5031689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5dc4e9cb5a4c309e116bd12ed324d366cb313abc8595bf9703d335a06cdf20`  
		Last Modified: Thu, 27 Jun 2024 18:58:42 GMT  
		Size: 22.1 KB (22077 bytes)  
		MIME: application/vnd.in-toto+json
