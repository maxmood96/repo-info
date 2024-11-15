<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.38`](#neo4j4438)
-	[`neo4j:4.4.38-community`](#neo4j4438-community)
-	[`neo4j:4.4.38-enterprise`](#neo4j4438-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi9`](#neo4j5-community-ubi9)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi9`](#neo4j5-enterprise-ubi9)
-	[`neo4j:5-ubi9`](#neo4j5-ubi9)
-	[`neo4j:5.25`](#neo4j525)
-	[`neo4j:5.25-bullseye`](#neo4j525-bullseye)
-	[`neo4j:5.25-community`](#neo4j525-community)
-	[`neo4j:5.25-community-bullseye`](#neo4j525-community-bullseye)
-	[`neo4j:5.25-community-ubi9`](#neo4j525-community-ubi9)
-	[`neo4j:5.25-enterprise`](#neo4j525-enterprise)
-	[`neo4j:5.25-enterprise-bullseye`](#neo4j525-enterprise-bullseye)
-	[`neo4j:5.25-enterprise-ubi9`](#neo4j525-enterprise-ubi9)
-	[`neo4j:5.25-ubi9`](#neo4j525-ubi9)
-	[`neo4j:5.25.1`](#neo4j5251)
-	[`neo4j:5.25.1-bullseye`](#neo4j5251-bullseye)
-	[`neo4j:5.25.1-community`](#neo4j5251-community)
-	[`neo4j:5.25.1-community-bullseye`](#neo4j5251-community-bullseye)
-	[`neo4j:5.25.1-community-ubi9`](#neo4j5251-community-ubi9)
-	[`neo4j:5.25.1-enterprise`](#neo4j5251-enterprise)
-	[`neo4j:5.25.1-enterprise-bullseye`](#neo4j5251-enterprise-bullseye)
-	[`neo4j:5.25.1-enterprise-ubi9`](#neo4j5251-enterprise-ubi9)
-	[`neo4j:5.25.1-ubi9`](#neo4j5251-ubi9)
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
$ docker pull neo4j@sha256:579780138190b84bef8925cc1fe1a286e69fb08db4f44522f3d35adfdc1d573c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:b5e10be292c531b07aa7d0e9e5d77bfed1403e50830ecd34a93cac9364a865cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306155785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1151f4e610afeedb6e6e6428829d49fe7eda10e4d3c54bafbafa1bf4023183`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f02e37ce0467106de3eb6df803b391166c1e64088bfdb82079a7cf33661a0dd`  
		Last Modified: Tue, 12 Nov 2024 02:40:38 GMT  
		Size: 145.6 MB (145601314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ef7c9bfce379edb6633667d4f39949229a29ee807192c445770975fd5a366c`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc1d5ab2e5114b66be1953f8283d7adc7699bf317ba41fbb981ae6744377909`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37832a575e28ea2aa4d3d487c5a830aa0273e62ab89a3cbf7f35fd9f16357efe`  
		Last Modified: Tue, 12 Nov 2024 02:40:38 GMT  
		Size: 129.1 MB (129089077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:0919bb8b1dd26908d7dc24ca17654bc1a80dc2237cdfd3b61e1cfea75b669bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8150f50cacccc5676976e72f8eecc321341d5d1747415c020056c16b5ec13506`

```dockerfile
```

-	Layers:
	-	`sha256:ae592df74579ddefec25092ccf5259aec1fe430a6aa04f3b6549d37cbf5f890d`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 3.2 MB (3202059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb9fdf5d51661fff00ecfc18570f78061b53acb5eb7a31d0a855ca72f9bd36f`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cafb830704483b4fa32f36a2385b5187d74d1c29ec4eefb2324dcd713596b0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301547438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce66ad4661ca188dcd3dd1f6e6dd69d33bd932f87b5eb425533e59eef5030c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0f23c4561b8cf8ddc692ea95c4ac045ee7e8c46c1e9dd327ec37b999c1f34`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 142.4 MB (142389091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6125113563754f9fdf846610d57203d7be1519010afcf26593b3b22f326474b5`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96557481d80d932182051696a3b42da6ff0a711ea0e15f54265a01281af2e324`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3360d4a5fab98625569f9a682192e4a867c27baac98d28a25c942f6e5e7fc79c`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 129.1 MB (129052891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:7809c8164d1578b01084e75c97cec31f5587cbeac5faa5dc3686b9d7a0ae717c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade919d689db172af673d0f18893ab8a955be7371de10d9c9fdc8560c92c507c`

```dockerfile
```

-	Layers:
	-	`sha256:fd9ab488c559ffce5020cc4fed57abbccf8d73dd7465a3ad7eac5ad7afde1c4b`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 3.2 MB (3202322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f53a353360029d3e75690c2a0cabce90001c7fb665fd8f2039eea651635c3585`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:579780138190b84bef8925cc1fe1a286e69fb08db4f44522f3d35adfdc1d573c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b5e10be292c531b07aa7d0e9e5d77bfed1403e50830ecd34a93cac9364a865cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306155785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1151f4e610afeedb6e6e6428829d49fe7eda10e4d3c54bafbafa1bf4023183`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f02e37ce0467106de3eb6df803b391166c1e64088bfdb82079a7cf33661a0dd`  
		Last Modified: Tue, 12 Nov 2024 02:40:38 GMT  
		Size: 145.6 MB (145601314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ef7c9bfce379edb6633667d4f39949229a29ee807192c445770975fd5a366c`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc1d5ab2e5114b66be1953f8283d7adc7699bf317ba41fbb981ae6744377909`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37832a575e28ea2aa4d3d487c5a830aa0273e62ab89a3cbf7f35fd9f16357efe`  
		Last Modified: Tue, 12 Nov 2024 02:40:38 GMT  
		Size: 129.1 MB (129089077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0919bb8b1dd26908d7dc24ca17654bc1a80dc2237cdfd3b61e1cfea75b669bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8150f50cacccc5676976e72f8eecc321341d5d1747415c020056c16b5ec13506`

```dockerfile
```

-	Layers:
	-	`sha256:ae592df74579ddefec25092ccf5259aec1fe430a6aa04f3b6549d37cbf5f890d`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 3.2 MB (3202059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb9fdf5d51661fff00ecfc18570f78061b53acb5eb7a31d0a855ca72f9bd36f`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cafb830704483b4fa32f36a2385b5187d74d1c29ec4eefb2324dcd713596b0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301547438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce66ad4661ca188dcd3dd1f6e6dd69d33bd932f87b5eb425533e59eef5030c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0f23c4561b8cf8ddc692ea95c4ac045ee7e8c46c1e9dd327ec37b999c1f34`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 142.4 MB (142389091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6125113563754f9fdf846610d57203d7be1519010afcf26593b3b22f326474b5`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96557481d80d932182051696a3b42da6ff0a711ea0e15f54265a01281af2e324`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3360d4a5fab98625569f9a682192e4a867c27baac98d28a25c942f6e5e7fc79c`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 129.1 MB (129052891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:7809c8164d1578b01084e75c97cec31f5587cbeac5faa5dc3686b9d7a0ae717c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade919d689db172af673d0f18893ab8a955be7371de10d9c9fdc8560c92c507c`

```dockerfile
```

-	Layers:
	-	`sha256:fd9ab488c559ffce5020cc4fed57abbccf8d73dd7465a3ad7eac5ad7afde1c4b`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 3.2 MB (3202322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f53a353360029d3e75690c2a0cabce90001c7fb665fd8f2039eea651635c3585`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:2c75038521835daabc7eacc0a0b3dc9ff32eb686aa6d8fa3d099460386097d4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8c93a839f561305d3dd5f0c8ccc3fde28d1b03e2bf76b837d22ad105509d26f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.6 MB (410562197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7245b7301fa9f13c574ff25fbf12ccd09052f47e3255c7d44f5affa1bc7ff73`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ab9fe6a9bd6c76d679070597d7129e68bbc9a3be473b6b07bd68e852026e54f0 NEO4J_TARBALL=neo4j-enterprise-4.4.38-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9285f0f019b0ce821c3ebd41ffb31c7b6b5a87db6a360e1be8911d3587256c82`  
		Last Modified: Tue, 12 Nov 2024 02:16:15 GMT  
		Size: 145.6 MB (145601329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726c835514ac5adda1712d41c097b453a8c50351b729db6da23938444e746514`  
		Last Modified: Tue, 12 Nov 2024 02:16:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca300f413e589da2ebf98b8e44fd514adab1c70a3357059afd2523172431dd71`  
		Last Modified: Tue, 12 Nov 2024 02:16:12 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6725ca378cd18fcb106f636743d0ea1707eaaddcd381bb6c073778572388b`  
		Last Modified: Tue, 12 Nov 2024 02:16:16 GMT  
		Size: 233.5 MB (233495475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b7316dc72f085f1f0ab9ecd08edf79393bd40aa505e2b4f46170a304c41139ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99b494c4439caa9b8dd42aad6265b4d9c081330dac1af4d3e33d080e568da47`

```dockerfile
```

-	Layers:
	-	`sha256:ba8a1168b604c8adc2d8be30bff49df0e8b8914503449a9aed86ab7084097d37`  
		Last Modified: Tue, 12 Nov 2024 02:16:12 GMT  
		Size: 3.4 MB (3352748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3885b122a1272c3b950d89680e763895f658bc21beac7054aab718c703420947`  
		Last Modified: Tue, 12 Nov 2024 02:16:12 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ba18eda767417e59a413f5b9a514360d4441ed2dcbaf1d81bd317c1f117b835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.0 MB (405957334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2b9580d1800378e051f345fda99b56e47747cc99c53c288e4db8d4bd96bbe8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ab9fe6a9bd6c76d679070597d7129e68bbc9a3be473b6b07bd68e852026e54f0 NEO4J_TARBALL=neo4j-enterprise-4.4.38-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0f23c4561b8cf8ddc692ea95c4ac045ee7e8c46c1e9dd327ec37b999c1f34`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 142.4 MB (142389091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3612627c416a6f1d410bad2fd7213d15f84b3341e2767785b0ca9ca915a1c82`  
		Last Modified: Tue, 12 Nov 2024 13:30:34 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06fdfe255625def0a2daae61f948c050bee3bd9bb41377a042d4368ba89db64`  
		Last Modified: Tue, 12 Nov 2024 13:30:34 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e4720fe68a4993a7997141b80d948f2f1da0909a70b336184bdd11788db0a7`  
		Last Modified: Tue, 12 Nov 2024 13:30:40 GMT  
		Size: 233.5 MB (233462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a139a1a0797c44eddb5a34246915f0b0502f5264c55bdbd62d11cacd26dc07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36746f42ef5fa517d2040bf3aef39a62038bbcafda5bc3e253e5fce02614180`

```dockerfile
```

-	Layers:
	-	`sha256:17d5dfe1771979370fe9d107f20ba9b75628aaa2cd200a4c0a426e2baed0b726`  
		Last Modified: Tue, 12 Nov 2024 13:30:34 GMT  
		Size: 3.4 MB (3352987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed162ed77043d80d85c5c1d057cba0e5e9b2d7c3fbe1e4a2465444bbb2f4613`  
		Last Modified: Tue, 12 Nov 2024 13:30:34 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.38`

```console
$ docker pull neo4j@sha256:579780138190b84bef8925cc1fe1a286e69fb08db4f44522f3d35adfdc1d573c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.38` - linux; amd64

```console
$ docker pull neo4j@sha256:b5e10be292c531b07aa7d0e9e5d77bfed1403e50830ecd34a93cac9364a865cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306155785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1151f4e610afeedb6e6e6428829d49fe7eda10e4d3c54bafbafa1bf4023183`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f02e37ce0467106de3eb6df803b391166c1e64088bfdb82079a7cf33661a0dd`  
		Last Modified: Tue, 12 Nov 2024 02:40:38 GMT  
		Size: 145.6 MB (145601314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ef7c9bfce379edb6633667d4f39949229a29ee807192c445770975fd5a366c`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc1d5ab2e5114b66be1953f8283d7adc7699bf317ba41fbb981ae6744377909`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37832a575e28ea2aa4d3d487c5a830aa0273e62ab89a3cbf7f35fd9f16357efe`  
		Last Modified: Tue, 12 Nov 2024 02:40:38 GMT  
		Size: 129.1 MB (129089077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38` - unknown; unknown

```console
$ docker pull neo4j@sha256:0919bb8b1dd26908d7dc24ca17654bc1a80dc2237cdfd3b61e1cfea75b669bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8150f50cacccc5676976e72f8eecc321341d5d1747415c020056c16b5ec13506`

```dockerfile
```

-	Layers:
	-	`sha256:ae592df74579ddefec25092ccf5259aec1fe430a6aa04f3b6549d37cbf5f890d`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 3.2 MB (3202059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb9fdf5d51661fff00ecfc18570f78061b53acb5eb7a31d0a855ca72f9bd36f`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.38` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cafb830704483b4fa32f36a2385b5187d74d1c29ec4eefb2324dcd713596b0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301547438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce66ad4661ca188dcd3dd1f6e6dd69d33bd932f87b5eb425533e59eef5030c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0f23c4561b8cf8ddc692ea95c4ac045ee7e8c46c1e9dd327ec37b999c1f34`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 142.4 MB (142389091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6125113563754f9fdf846610d57203d7be1519010afcf26593b3b22f326474b5`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96557481d80d932182051696a3b42da6ff0a711ea0e15f54265a01281af2e324`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3360d4a5fab98625569f9a682192e4a867c27baac98d28a25c942f6e5e7fc79c`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 129.1 MB (129052891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38` - unknown; unknown

```console
$ docker pull neo4j@sha256:7809c8164d1578b01084e75c97cec31f5587cbeac5faa5dc3686b9d7a0ae717c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade919d689db172af673d0f18893ab8a955be7371de10d9c9fdc8560c92c507c`

```dockerfile
```

-	Layers:
	-	`sha256:fd9ab488c559ffce5020cc4fed57abbccf8d73dd7465a3ad7eac5ad7afde1c4b`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 3.2 MB (3202322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f53a353360029d3e75690c2a0cabce90001c7fb665fd8f2039eea651635c3585`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.38-community`

```console
$ docker pull neo4j@sha256:579780138190b84bef8925cc1fe1a286e69fb08db4f44522f3d35adfdc1d573c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.38-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b5e10be292c531b07aa7d0e9e5d77bfed1403e50830ecd34a93cac9364a865cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306155785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1151f4e610afeedb6e6e6428829d49fe7eda10e4d3c54bafbafa1bf4023183`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f02e37ce0467106de3eb6df803b391166c1e64088bfdb82079a7cf33661a0dd`  
		Last Modified: Tue, 12 Nov 2024 02:40:38 GMT  
		Size: 145.6 MB (145601314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ef7c9bfce379edb6633667d4f39949229a29ee807192c445770975fd5a366c`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc1d5ab2e5114b66be1953f8283d7adc7699bf317ba41fbb981ae6744377909`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37832a575e28ea2aa4d3d487c5a830aa0273e62ab89a3cbf7f35fd9f16357efe`  
		Last Modified: Tue, 12 Nov 2024 02:40:38 GMT  
		Size: 129.1 MB (129089077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0919bb8b1dd26908d7dc24ca17654bc1a80dc2237cdfd3b61e1cfea75b669bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8150f50cacccc5676976e72f8eecc321341d5d1747415c020056c16b5ec13506`

```dockerfile
```

-	Layers:
	-	`sha256:ae592df74579ddefec25092ccf5259aec1fe430a6aa04f3b6549d37cbf5f890d`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 3.2 MB (3202059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb9fdf5d51661fff00ecfc18570f78061b53acb5eb7a31d0a855ca72f9bd36f`  
		Last Modified: Tue, 12 Nov 2024 02:40:36 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.38-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cafb830704483b4fa32f36a2385b5187d74d1c29ec4eefb2324dcd713596b0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301547438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ce66ad4661ca188dcd3dd1f6e6dd69d33bd932f87b5eb425533e59eef5030c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=452bad595302f9c8bf56f311b5076ef21e98e270229403dca90b2d61b2297b33 NEO4J_TARBALL=neo4j-community-4.4.38-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0f23c4561b8cf8ddc692ea95c4ac045ee7e8c46c1e9dd327ec37b999c1f34`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 142.4 MB (142389091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6125113563754f9fdf846610d57203d7be1519010afcf26593b3b22f326474b5`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 3.9 KB (3862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96557481d80d932182051696a3b42da6ff0a711ea0e15f54265a01281af2e324`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3360d4a5fab98625569f9a682192e4a867c27baac98d28a25c942f6e5e7fc79c`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 129.1 MB (129052891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:7809c8164d1578b01084e75c97cec31f5587cbeac5faa5dc3686b9d7a0ae717c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade919d689db172af673d0f18893ab8a955be7371de10d9c9fdc8560c92c507c`

```dockerfile
```

-	Layers:
	-	`sha256:fd9ab488c559ffce5020cc4fed57abbccf8d73dd7465a3ad7eac5ad7afde1c4b`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 3.2 MB (3202322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f53a353360029d3e75690c2a0cabce90001c7fb665fd8f2039eea651635c3585`  
		Last Modified: Tue, 12 Nov 2024 13:27:58 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.38-enterprise`

```console
$ docker pull neo4j@sha256:2c75038521835daabc7eacc0a0b3dc9ff32eb686aa6d8fa3d099460386097d4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.38-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:8c93a839f561305d3dd5f0c8ccc3fde28d1b03e2bf76b837d22ad105509d26f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.6 MB (410562197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7245b7301fa9f13c574ff25fbf12ccd09052f47e3255c7d44f5affa1bc7ff73`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ab9fe6a9bd6c76d679070597d7129e68bbc9a3be473b6b07bd68e852026e54f0 NEO4J_TARBALL=neo4j-enterprise-4.4.38-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9285f0f019b0ce821c3ebd41ffb31c7b6b5a87db6a360e1be8911d3587256c82`  
		Last Modified: Tue, 12 Nov 2024 02:16:15 GMT  
		Size: 145.6 MB (145601329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726c835514ac5adda1712d41c097b453a8c50351b729db6da23938444e746514`  
		Last Modified: Tue, 12 Nov 2024 02:16:12 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca300f413e589da2ebf98b8e44fd514adab1c70a3357059afd2523172431dd71`  
		Last Modified: Tue, 12 Nov 2024 02:16:12 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6725ca378cd18fcb106f636743d0ea1707eaaddcd381bb6c073778572388b`  
		Last Modified: Tue, 12 Nov 2024 02:16:16 GMT  
		Size: 233.5 MB (233495475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b7316dc72f085f1f0ab9ecd08edf79393bd40aa505e2b4f46170a304c41139ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99b494c4439caa9b8dd42aad6265b4d9c081330dac1af4d3e33d080e568da47`

```dockerfile
```

-	Layers:
	-	`sha256:ba8a1168b604c8adc2d8be30bff49df0e8b8914503449a9aed86ab7084097d37`  
		Last Modified: Tue, 12 Nov 2024 02:16:12 GMT  
		Size: 3.4 MB (3352748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3885b122a1272c3b950d89680e763895f658bc21beac7054aab718c703420947`  
		Last Modified: Tue, 12 Nov 2024 02:16:12 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.38-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:4ba18eda767417e59a413f5b9a514360d4441ed2dcbaf1d81bd317c1f117b835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.0 MB (405957334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2b9580d1800378e051f345fda99b56e47747cc99c53c288e4db8d4bd96bbe8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 08 Oct 2024 15:41:49 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["bash"]
# Tue, 08 Oct 2024 15:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Oct 2024 15:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ab9fe6a9bd6c76d679070597d7129e68bbc9a3be473b6b07bd68e852026e54f0 NEO4J_TARBALL=neo4j-enterprise-4.4.38-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 08 Oct 2024 15:41:49 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.38-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 08 Oct 2024 15:41:49 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 15:41:49 GMT
WORKDIR /var/lib/neo4j
# Tue, 08 Oct 2024 15:41:49 GMT
VOLUME [/data /logs]
# Tue, 08 Oct 2024 15:41:49 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 08 Oct 2024 15:41:49 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 08 Oct 2024 15:41:49 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0f23c4561b8cf8ddc692ea95c4ac045ee7e8c46c1e9dd327ec37b999c1f34`  
		Last Modified: Tue, 12 Nov 2024 13:28:02 GMT  
		Size: 142.4 MB (142389091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3612627c416a6f1d410bad2fd7213d15f84b3341e2767785b0ca9ca915a1c82`  
		Last Modified: Tue, 12 Nov 2024 13:30:34 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06fdfe255625def0a2daae61f948c050bee3bd9bb41377a042d4368ba89db64`  
		Last Modified: Tue, 12 Nov 2024 13:30:34 GMT  
		Size: 10.0 KB (9963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e4720fe68a4993a7997141b80d948f2f1da0909a70b336184bdd11788db0a7`  
		Last Modified: Tue, 12 Nov 2024 13:30:40 GMT  
		Size: 233.5 MB (233462782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.38-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a139a1a0797c44eddb5a34246915f0b0502f5264c55bdbd62d11cacd26dc07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36746f42ef5fa517d2040bf3aef39a62038bbcafda5bc3e253e5fce02614180`

```dockerfile
```

-	Layers:
	-	`sha256:17d5dfe1771979370fe9d107f20ba9b75628aaa2cd200a4c0a426e2baed0b726`  
		Last Modified: Tue, 12 Nov 2024 13:30:34 GMT  
		Size: 3.4 MB (3352987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed162ed77043d80d85c5c1d057cba0e5e9b2d7c3fbe1e4a2465444bbb2f4613`  
		Last Modified: Tue, 12 Nov 2024 13:30:34 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:1c6ff1d77341a4dae5d291f77468d8b0a4b01e2dcd49fa3f028d313c4af6192f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0ae83b4f9a2dedcaadfa6844a63612e8f39b1ff62a460409450241f6a214f7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313977097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b053dce1567d461f41b43539e7dae9b035e1a35a52e48ec06381b37653342`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb9f3e565eddc4e6833ebfb7077dbd469a5a4874268cd311fe37f1ee2b75b0`  
		Last Modified: Thu, 14 Nov 2024 21:14:39 GMT  
		Size: 133.9 MB (133850178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f0b6a673e6094870d3fdcd971696e979ba06c4055bb71844990194ee0537f`  
		Last Modified: Thu, 14 Nov 2024 21:14:35 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fb302b729093912e6e27c03014aec2c709c8ed5a9fb6cbac7a1a90ceb153`  
		Last Modified: Thu, 14 Nov 2024 21:14:40 GMT  
		Size: 140.2 MB (140181995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:39c07d43b72067a79d8da50266778002a1a92754f1e18652714aba0af55a6b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91c22e365051a37674d6d2d5a1673bab3668e6394d139aa3e488ec196b37968`

```dockerfile
```

-	Layers:
	-	`sha256:f48868b73c0e3f1f0c76682981e24cd25c400496d4ad71d00da44a47e31d896a`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47af631d4e7bc6cbb58095ac368d0bdfce715ebb0563cb7d4056006d11780111`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3c9470d2ca0b5cdc4aaea86e6f603f5020ffd2689ea1c09e4e8342e0144c7711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312167053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855932b135b8129e38fa94544e1da7b7dd0d6089503454ab6c640f6905821ccb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e1f9bafff5c6a0d382530add91906d92f4e04a2984d0e4eae6bda09fa3f6a`  
		Last Modified: Thu, 14 Nov 2024 22:12:03 GMT  
		Size: 140.2 MB (140181983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f3d5acb84ada99f13323a9aff91bd653c9a2bf26b9effa8964959768771565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c7f48a798c31b5b41a43637af8a544d0ead54b82f4f56acc0191d9ce42d5`

```dockerfile
```

-	Layers:
	-	`sha256:6b1ea43e81e1c8d817e1b311e6ab374f89f6b395959b5fa6b2bf106afd69ac1f`  
		Last Modified: Thu, 14 Nov 2024 22:12:00 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c52a6d585d2378742329a9080fd834eb501cb397e61e36b8d5e967e29b8d5b`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:7fb7633ffd3cd7af4359935f3338544d8d5f1b4aa83547cd22f29cf07de9e4f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:051ff55cc89d4f39244d7c8f6624cdb4f76e2d0bced398024401e9a7ad9de187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608119323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b5bb5e640b26f68c7c532f06f865ddadd03ca5f6ae03e528157930a270d84`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041b88a2fb9c472ecbfc772e45a3b018cd1a7668db24063bbe5f365310f80bd`  
		Last Modified: Tue, 12 Nov 2024 02:17:56 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdca0cd22c0d497293a8ad4f71d0f5700b326380f6b0214d63af64f8cfb8bb`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234f60c6542d45573c83ff2a04ab34b9b37c45445c3722c9bc163f0a548e6765`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ac141efee1dba0d9829a36fb80a5d5d7efe50b428c799a958ebd95663f06f1`  
		Last Modified: Tue, 12 Nov 2024 02:18:02 GMT  
		Size: 432.1 MB (432119108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:076de908a2013cd085e9c013c1b9e08e72eb157a10ffb51bd4604c606a87f1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3bfef88fdb9e387961677c041ca3023bc02898ac6410f622057a815324e42f`

```dockerfile
```

-	Layers:
	-	`sha256:59a1eebef8bd0f84de9373f30583cf8fff216a64c91cef46794b3df91b9741bf`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6b312905e6cdea17718ab5d78524c2288cdf017b00d3e1c97340840c65f53f`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7df0c5180c12b9d661f894efb8b5ee6beae08f4a35421d163752eb1cee68268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605555663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42849c84987e6132b7a3aa62ceda758eabeb6c799e9fb9850f154ea40a75c2fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f4bf514b87eda9f9cd384680952b857c4a970d832d9246cb3a9812a3323f50`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a352f50acc211706037a0fbbe15b26053829c42a5898733c942b029f20b5cc5`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42adddf2329e50d82fe1048f35545a318cc64ca37b29e5afbf0eccfd1e723f7c`  
		Last Modified: Tue, 12 Nov 2024 13:25:38 GMT  
		Size: 432.1 MB (432089166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:9b925d9bfc52ad18b06a1ed3f64c8996fd9948624406cc4cfdec20225f422b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e568224d5c038d92f1e46db372dffc5371966f458c9d0f71cdd766ba4fd7726`

```dockerfile
```

-	Layers:
	-	`sha256:122a15fcb5e810175925212f6e7ae5653294966f4146e39209405c165b0b3a4d`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde38be6ee16eb1296871262883a2a764918865e351840724ce17a62e76a78a0`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:7fb7633ffd3cd7af4359935f3338544d8d5f1b4aa83547cd22f29cf07de9e4f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:051ff55cc89d4f39244d7c8f6624cdb4f76e2d0bced398024401e9a7ad9de187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608119323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b5bb5e640b26f68c7c532f06f865ddadd03ca5f6ae03e528157930a270d84`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041b88a2fb9c472ecbfc772e45a3b018cd1a7668db24063bbe5f365310f80bd`  
		Last Modified: Tue, 12 Nov 2024 02:17:56 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdca0cd22c0d497293a8ad4f71d0f5700b326380f6b0214d63af64f8cfb8bb`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234f60c6542d45573c83ff2a04ab34b9b37c45445c3722c9bc163f0a548e6765`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ac141efee1dba0d9829a36fb80a5d5d7efe50b428c799a958ebd95663f06f1`  
		Last Modified: Tue, 12 Nov 2024 02:18:02 GMT  
		Size: 432.1 MB (432119108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:076de908a2013cd085e9c013c1b9e08e72eb157a10ffb51bd4604c606a87f1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3bfef88fdb9e387961677c041ca3023bc02898ac6410f622057a815324e42f`

```dockerfile
```

-	Layers:
	-	`sha256:59a1eebef8bd0f84de9373f30583cf8fff216a64c91cef46794b3df91b9741bf`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6b312905e6cdea17718ab5d78524c2288cdf017b00d3e1c97340840c65f53f`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7df0c5180c12b9d661f894efb8b5ee6beae08f4a35421d163752eb1cee68268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605555663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42849c84987e6132b7a3aa62ceda758eabeb6c799e9fb9850f154ea40a75c2fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f4bf514b87eda9f9cd384680952b857c4a970d832d9246cb3a9812a3323f50`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a352f50acc211706037a0fbbe15b26053829c42a5898733c942b029f20b5cc5`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42adddf2329e50d82fe1048f35545a318cc64ca37b29e5afbf0eccfd1e723f7c`  
		Last Modified: Tue, 12 Nov 2024 13:25:38 GMT  
		Size: 432.1 MB (432089166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9b925d9bfc52ad18b06a1ed3f64c8996fd9948624406cc4cfdec20225f422b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e568224d5c038d92f1e46db372dffc5371966f458c9d0f71cdd766ba4fd7726`

```dockerfile
```

-	Layers:
	-	`sha256:122a15fcb5e810175925212f6e7ae5653294966f4146e39209405c165b0b3a4d`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde38be6ee16eb1296871262883a2a764918865e351840724ce17a62e76a78a0`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:dbe034b56dea03f408a931a3f593749b0a9e8aefcd8407a9a667f94fe631e30b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:eb7d26f8e5ead80e799605278d16380a991f2bc3dafc9b23404c399ca50ed088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602989331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0146eeb6ab1d07c885d7f5f4d2f8203e9c67b7afda2da8d4ff01d1f7878decb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94888d00a904699c72d1d90a2aeb95340d8b59925baef8fec32e5036fc38e2c8`  
		Last Modified: Thu, 14 Nov 2024 21:15:54 GMT  
		Size: 133.8 MB (133849473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676dc572091818922be830009e8cf242ee6b45b3be100d7652ef200603891d9d`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d164037996f6f75c08b11d20d5a3b85ff117d87324776a537cc816bfb91add3`  
		Last Modified: Thu, 14 Nov 2024 21:15:59 GMT  
		Size: 429.2 MB (429194928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ff4957c27870f6ee18eec3ca66634fc4e23cd99651312378c31044c48da16553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9359eb512cd415988420ba6c2c2d15789edce332abcdaf11192e5a4d1ea2ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:c0318fceace1b81e55d26529026f1138f54ebf8d7a0e5853cdc52f17ba87dc64`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 7.8 MB (7845287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9527916085dd17b7156ec9e5e5ddad2ac0bec80081160653a462a58cbda96f78`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cf8ddd4a4a19363143504a084e334692ae40de92c6ad608976631e9ec088807b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601179946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07e06ed3bd0800eb1b33ac21eb14f7edf99aaffc414f736a44c74eb145a8143`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69476780d661de498dc83d2b1de4f2cc2e0611b28b4e4bf6add1abf522c9a14`  
		Last Modified: Thu, 14 Nov 2024 22:16:15 GMT  
		Size: 429.2 MB (429194876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c70b5c5046371b3124435c2dd865281650a93d1c81778ac62664e7316c469e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7846334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd090a674b8e05a5f334e3a574bf44cda482029f34b01daff75da38d36f5359`

```dockerfile
```

-	Layers:
	-	`sha256:2d05114788494df5ddd53077e3095770c30a10e4c1178ac5249fd72f52ff4923`  
		Last Modified: Thu, 14 Nov 2024 22:16:08 GMT  
		Size: 7.8 MB (7824852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6683551f820d8703a088e0ca7f578205df085bd5959fdd16fc678d2ede2897`  
		Last Modified: Thu, 14 Nov 2024 22:16:07 GMT  
		Size: 21.5 KB (21482 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:1c6ff1d77341a4dae5d291f77468d8b0a4b01e2dcd49fa3f028d313c4af6192f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0ae83b4f9a2dedcaadfa6844a63612e8f39b1ff62a460409450241f6a214f7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313977097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b053dce1567d461f41b43539e7dae9b035e1a35a52e48ec06381b37653342`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb9f3e565eddc4e6833ebfb7077dbd469a5a4874268cd311fe37f1ee2b75b0`  
		Last Modified: Thu, 14 Nov 2024 21:14:39 GMT  
		Size: 133.9 MB (133850178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f0b6a673e6094870d3fdcd971696e979ba06c4055bb71844990194ee0537f`  
		Last Modified: Thu, 14 Nov 2024 21:14:35 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fb302b729093912e6e27c03014aec2c709c8ed5a9fb6cbac7a1a90ceb153`  
		Last Modified: Thu, 14 Nov 2024 21:14:40 GMT  
		Size: 140.2 MB (140181995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:39c07d43b72067a79d8da50266778002a1a92754f1e18652714aba0af55a6b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91c22e365051a37674d6d2d5a1673bab3668e6394d139aa3e488ec196b37968`

```dockerfile
```

-	Layers:
	-	`sha256:f48868b73c0e3f1f0c76682981e24cd25c400496d4ad71d00da44a47e31d896a`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47af631d4e7bc6cbb58095ac368d0bdfce715ebb0563cb7d4056006d11780111`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3c9470d2ca0b5cdc4aaea86e6f603f5020ffd2689ea1c09e4e8342e0144c7711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312167053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855932b135b8129e38fa94544e1da7b7dd0d6089503454ab6c640f6905821ccb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e1f9bafff5c6a0d382530add91906d92f4e04a2984d0e4eae6bda09fa3f6a`  
		Last Modified: Thu, 14 Nov 2024 22:12:03 GMT  
		Size: 140.2 MB (140181983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f3d5acb84ada99f13323a9aff91bd653c9a2bf26b9effa8964959768771565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c7f48a798c31b5b41a43637af8a544d0ead54b82f4f56acc0191d9ce42d5`

```dockerfile
```

-	Layers:
	-	`sha256:6b1ea43e81e1c8d817e1b311e6ab374f89f6b395959b5fa6b2bf106afd69ac1f`  
		Last Modified: Thu, 14 Nov 2024 22:12:00 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c52a6d585d2378742329a9080fd834eb501cb397e61e36b8d5e967e29b8d5b`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-bullseye`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-community`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-community-bullseye`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-community-ubi9`

```console
$ docker pull neo4j@sha256:1c6ff1d77341a4dae5d291f77468d8b0a4b01e2dcd49fa3f028d313c4af6192f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0ae83b4f9a2dedcaadfa6844a63612e8f39b1ff62a460409450241f6a214f7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313977097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b053dce1567d461f41b43539e7dae9b035e1a35a52e48ec06381b37653342`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb9f3e565eddc4e6833ebfb7077dbd469a5a4874268cd311fe37f1ee2b75b0`  
		Last Modified: Thu, 14 Nov 2024 21:14:39 GMT  
		Size: 133.9 MB (133850178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f0b6a673e6094870d3fdcd971696e979ba06c4055bb71844990194ee0537f`  
		Last Modified: Thu, 14 Nov 2024 21:14:35 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fb302b729093912e6e27c03014aec2c709c8ed5a9fb6cbac7a1a90ceb153`  
		Last Modified: Thu, 14 Nov 2024 21:14:40 GMT  
		Size: 140.2 MB (140181995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:39c07d43b72067a79d8da50266778002a1a92754f1e18652714aba0af55a6b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91c22e365051a37674d6d2d5a1673bab3668e6394d139aa3e488ec196b37968`

```dockerfile
```

-	Layers:
	-	`sha256:f48868b73c0e3f1f0c76682981e24cd25c400496d4ad71d00da44a47e31d896a`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47af631d4e7bc6cbb58095ac368d0bdfce715ebb0563cb7d4056006d11780111`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3c9470d2ca0b5cdc4aaea86e6f603f5020ffd2689ea1c09e4e8342e0144c7711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312167053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855932b135b8129e38fa94544e1da7b7dd0d6089503454ab6c640f6905821ccb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e1f9bafff5c6a0d382530add91906d92f4e04a2984d0e4eae6bda09fa3f6a`  
		Last Modified: Thu, 14 Nov 2024 22:12:03 GMT  
		Size: 140.2 MB (140181983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f3d5acb84ada99f13323a9aff91bd653c9a2bf26b9effa8964959768771565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c7f48a798c31b5b41a43637af8a544d0ead54b82f4f56acc0191d9ce42d5`

```dockerfile
```

-	Layers:
	-	`sha256:6b1ea43e81e1c8d817e1b311e6ab374f89f6b395959b5fa6b2bf106afd69ac1f`  
		Last Modified: Thu, 14 Nov 2024 22:12:00 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c52a6d585d2378742329a9080fd834eb501cb397e61e36b8d5e967e29b8d5b`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-enterprise`

```console
$ docker pull neo4j@sha256:7fb7633ffd3cd7af4359935f3338544d8d5f1b4aa83547cd22f29cf07de9e4f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:051ff55cc89d4f39244d7c8f6624cdb4f76e2d0bced398024401e9a7ad9de187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608119323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b5bb5e640b26f68c7c532f06f865ddadd03ca5f6ae03e528157930a270d84`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041b88a2fb9c472ecbfc772e45a3b018cd1a7668db24063bbe5f365310f80bd`  
		Last Modified: Tue, 12 Nov 2024 02:17:56 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdca0cd22c0d497293a8ad4f71d0f5700b326380f6b0214d63af64f8cfb8bb`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234f60c6542d45573c83ff2a04ab34b9b37c45445c3722c9bc163f0a548e6765`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ac141efee1dba0d9829a36fb80a5d5d7efe50b428c799a958ebd95663f06f1`  
		Last Modified: Tue, 12 Nov 2024 02:18:02 GMT  
		Size: 432.1 MB (432119108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:076de908a2013cd085e9c013c1b9e08e72eb157a10ffb51bd4604c606a87f1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3bfef88fdb9e387961677c041ca3023bc02898ac6410f622057a815324e42f`

```dockerfile
```

-	Layers:
	-	`sha256:59a1eebef8bd0f84de9373f30583cf8fff216a64c91cef46794b3df91b9741bf`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6b312905e6cdea17718ab5d78524c2288cdf017b00d3e1c97340840c65f53f`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7df0c5180c12b9d661f894efb8b5ee6beae08f4a35421d163752eb1cee68268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605555663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42849c84987e6132b7a3aa62ceda758eabeb6c799e9fb9850f154ea40a75c2fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f4bf514b87eda9f9cd384680952b857c4a970d832d9246cb3a9812a3323f50`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a352f50acc211706037a0fbbe15b26053829c42a5898733c942b029f20b5cc5`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42adddf2329e50d82fe1048f35545a318cc64ca37b29e5afbf0eccfd1e723f7c`  
		Last Modified: Tue, 12 Nov 2024 13:25:38 GMT  
		Size: 432.1 MB (432089166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:9b925d9bfc52ad18b06a1ed3f64c8996fd9948624406cc4cfdec20225f422b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e568224d5c038d92f1e46db372dffc5371966f458c9d0f71cdd766ba4fd7726`

```dockerfile
```

-	Layers:
	-	`sha256:122a15fcb5e810175925212f6e7ae5653294966f4146e39209405c165b0b3a4d`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde38be6ee16eb1296871262883a2a764918865e351840724ce17a62e76a78a0`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:7fb7633ffd3cd7af4359935f3338544d8d5f1b4aa83547cd22f29cf07de9e4f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:051ff55cc89d4f39244d7c8f6624cdb4f76e2d0bced398024401e9a7ad9de187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608119323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b5bb5e640b26f68c7c532f06f865ddadd03ca5f6ae03e528157930a270d84`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041b88a2fb9c472ecbfc772e45a3b018cd1a7668db24063bbe5f365310f80bd`  
		Last Modified: Tue, 12 Nov 2024 02:17:56 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdca0cd22c0d497293a8ad4f71d0f5700b326380f6b0214d63af64f8cfb8bb`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234f60c6542d45573c83ff2a04ab34b9b37c45445c3722c9bc163f0a548e6765`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ac141efee1dba0d9829a36fb80a5d5d7efe50b428c799a958ebd95663f06f1`  
		Last Modified: Tue, 12 Nov 2024 02:18:02 GMT  
		Size: 432.1 MB (432119108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:076de908a2013cd085e9c013c1b9e08e72eb157a10ffb51bd4604c606a87f1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3bfef88fdb9e387961677c041ca3023bc02898ac6410f622057a815324e42f`

```dockerfile
```

-	Layers:
	-	`sha256:59a1eebef8bd0f84de9373f30583cf8fff216a64c91cef46794b3df91b9741bf`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6b312905e6cdea17718ab5d78524c2288cdf017b00d3e1c97340840c65f53f`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7df0c5180c12b9d661f894efb8b5ee6beae08f4a35421d163752eb1cee68268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605555663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42849c84987e6132b7a3aa62ceda758eabeb6c799e9fb9850f154ea40a75c2fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f4bf514b87eda9f9cd384680952b857c4a970d832d9246cb3a9812a3323f50`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a352f50acc211706037a0fbbe15b26053829c42a5898733c942b029f20b5cc5`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42adddf2329e50d82fe1048f35545a318cc64ca37b29e5afbf0eccfd1e723f7c`  
		Last Modified: Tue, 12 Nov 2024 13:25:38 GMT  
		Size: 432.1 MB (432089166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9b925d9bfc52ad18b06a1ed3f64c8996fd9948624406cc4cfdec20225f422b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e568224d5c038d92f1e46db372dffc5371966f458c9d0f71cdd766ba4fd7726`

```dockerfile
```

-	Layers:
	-	`sha256:122a15fcb5e810175925212f6e7ae5653294966f4146e39209405c165b0b3a4d`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde38be6ee16eb1296871262883a2a764918865e351840724ce17a62e76a78a0`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:dbe034b56dea03f408a931a3f593749b0a9e8aefcd8407a9a667f94fe631e30b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:eb7d26f8e5ead80e799605278d16380a991f2bc3dafc9b23404c399ca50ed088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602989331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0146eeb6ab1d07c885d7f5f4d2f8203e9c67b7afda2da8d4ff01d1f7878decb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94888d00a904699c72d1d90a2aeb95340d8b59925baef8fec32e5036fc38e2c8`  
		Last Modified: Thu, 14 Nov 2024 21:15:54 GMT  
		Size: 133.8 MB (133849473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676dc572091818922be830009e8cf242ee6b45b3be100d7652ef200603891d9d`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d164037996f6f75c08b11d20d5a3b85ff117d87324776a537cc816bfb91add3`  
		Last Modified: Thu, 14 Nov 2024 21:15:59 GMT  
		Size: 429.2 MB (429194928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ff4957c27870f6ee18eec3ca66634fc4e23cd99651312378c31044c48da16553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9359eb512cd415988420ba6c2c2d15789edce332abcdaf11192e5a4d1ea2ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:c0318fceace1b81e55d26529026f1138f54ebf8d7a0e5853cdc52f17ba87dc64`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 7.8 MB (7845287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9527916085dd17b7156ec9e5e5ddad2ac0bec80081160653a462a58cbda96f78`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cf8ddd4a4a19363143504a084e334692ae40de92c6ad608976631e9ec088807b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601179946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07e06ed3bd0800eb1b33ac21eb14f7edf99aaffc414f736a44c74eb145a8143`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69476780d661de498dc83d2b1de4f2cc2e0611b28b4e4bf6add1abf522c9a14`  
		Last Modified: Thu, 14 Nov 2024 22:16:15 GMT  
		Size: 429.2 MB (429194876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c70b5c5046371b3124435c2dd865281650a93d1c81778ac62664e7316c469e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7846334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd090a674b8e05a5f334e3a574bf44cda482029f34b01daff75da38d36f5359`

```dockerfile
```

-	Layers:
	-	`sha256:2d05114788494df5ddd53077e3095770c30a10e4c1178ac5249fd72f52ff4923`  
		Last Modified: Thu, 14 Nov 2024 22:16:08 GMT  
		Size: 7.8 MB (7824852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6683551f820d8703a088e0ca7f578205df085bd5959fdd16fc678d2ede2897`  
		Last Modified: Thu, 14 Nov 2024 22:16:07 GMT  
		Size: 21.5 KB (21482 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-ubi9`

```console
$ docker pull neo4j@sha256:1c6ff1d77341a4dae5d291f77468d8b0a4b01e2dcd49fa3f028d313c4af6192f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0ae83b4f9a2dedcaadfa6844a63612e8f39b1ff62a460409450241f6a214f7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313977097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b053dce1567d461f41b43539e7dae9b035e1a35a52e48ec06381b37653342`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb9f3e565eddc4e6833ebfb7077dbd469a5a4874268cd311fe37f1ee2b75b0`  
		Last Modified: Thu, 14 Nov 2024 21:14:39 GMT  
		Size: 133.9 MB (133850178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f0b6a673e6094870d3fdcd971696e979ba06c4055bb71844990194ee0537f`  
		Last Modified: Thu, 14 Nov 2024 21:14:35 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fb302b729093912e6e27c03014aec2c709c8ed5a9fb6cbac7a1a90ceb153`  
		Last Modified: Thu, 14 Nov 2024 21:14:40 GMT  
		Size: 140.2 MB (140181995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:39c07d43b72067a79d8da50266778002a1a92754f1e18652714aba0af55a6b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91c22e365051a37674d6d2d5a1673bab3668e6394d139aa3e488ec196b37968`

```dockerfile
```

-	Layers:
	-	`sha256:f48868b73c0e3f1f0c76682981e24cd25c400496d4ad71d00da44a47e31d896a`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47af631d4e7bc6cbb58095ac368d0bdfce715ebb0563cb7d4056006d11780111`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3c9470d2ca0b5cdc4aaea86e6f603f5020ffd2689ea1c09e4e8342e0144c7711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312167053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855932b135b8129e38fa94544e1da7b7dd0d6089503454ab6c640f6905821ccb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e1f9bafff5c6a0d382530add91906d92f4e04a2984d0e4eae6bda09fa3f6a`  
		Last Modified: Thu, 14 Nov 2024 22:12:03 GMT  
		Size: 140.2 MB (140181983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f3d5acb84ada99f13323a9aff91bd653c9a2bf26b9effa8964959768771565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c7f48a798c31b5b41a43637af8a544d0ead54b82f4f56acc0191d9ce42d5`

```dockerfile
```

-	Layers:
	-	`sha256:6b1ea43e81e1c8d817e1b311e6ab374f89f6b395959b5fa6b2bf106afd69ac1f`  
		Last Modified: Thu, 14 Nov 2024 22:12:00 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c52a6d585d2378742329a9080fd834eb501cb397e61e36b8d5e967e29b8d5b`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-bullseye`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-community`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-community` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-community-bullseye`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-community-ubi9`

```console
$ docker pull neo4j@sha256:1c6ff1d77341a4dae5d291f77468d8b0a4b01e2dcd49fa3f028d313c4af6192f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0ae83b4f9a2dedcaadfa6844a63612e8f39b1ff62a460409450241f6a214f7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313977097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b053dce1567d461f41b43539e7dae9b035e1a35a52e48ec06381b37653342`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb9f3e565eddc4e6833ebfb7077dbd469a5a4874268cd311fe37f1ee2b75b0`  
		Last Modified: Thu, 14 Nov 2024 21:14:39 GMT  
		Size: 133.9 MB (133850178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f0b6a673e6094870d3fdcd971696e979ba06c4055bb71844990194ee0537f`  
		Last Modified: Thu, 14 Nov 2024 21:14:35 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fb302b729093912e6e27c03014aec2c709c8ed5a9fb6cbac7a1a90ceb153`  
		Last Modified: Thu, 14 Nov 2024 21:14:40 GMT  
		Size: 140.2 MB (140181995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:39c07d43b72067a79d8da50266778002a1a92754f1e18652714aba0af55a6b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91c22e365051a37674d6d2d5a1673bab3668e6394d139aa3e488ec196b37968`

```dockerfile
```

-	Layers:
	-	`sha256:f48868b73c0e3f1f0c76682981e24cd25c400496d4ad71d00da44a47e31d896a`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47af631d4e7bc6cbb58095ac368d0bdfce715ebb0563cb7d4056006d11780111`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3c9470d2ca0b5cdc4aaea86e6f603f5020ffd2689ea1c09e4e8342e0144c7711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312167053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855932b135b8129e38fa94544e1da7b7dd0d6089503454ab6c640f6905821ccb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e1f9bafff5c6a0d382530add91906d92f4e04a2984d0e4eae6bda09fa3f6a`  
		Last Modified: Thu, 14 Nov 2024 22:12:03 GMT  
		Size: 140.2 MB (140181983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f3d5acb84ada99f13323a9aff91bd653c9a2bf26b9effa8964959768771565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c7f48a798c31b5b41a43637af8a544d0ead54b82f4f56acc0191d9ce42d5`

```dockerfile
```

-	Layers:
	-	`sha256:6b1ea43e81e1c8d817e1b311e6ab374f89f6b395959b5fa6b2bf106afd69ac1f`  
		Last Modified: Thu, 14 Nov 2024 22:12:00 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c52a6d585d2378742329a9080fd834eb501cb397e61e36b8d5e967e29b8d5b`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-enterprise`

```console
$ docker pull neo4j@sha256:7fb7633ffd3cd7af4359935f3338544d8d5f1b4aa83547cd22f29cf07de9e4f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:051ff55cc89d4f39244d7c8f6624cdb4f76e2d0bced398024401e9a7ad9de187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608119323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b5bb5e640b26f68c7c532f06f865ddadd03ca5f6ae03e528157930a270d84`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041b88a2fb9c472ecbfc772e45a3b018cd1a7668db24063bbe5f365310f80bd`  
		Last Modified: Tue, 12 Nov 2024 02:17:56 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdca0cd22c0d497293a8ad4f71d0f5700b326380f6b0214d63af64f8cfb8bb`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234f60c6542d45573c83ff2a04ab34b9b37c45445c3722c9bc163f0a548e6765`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ac141efee1dba0d9829a36fb80a5d5d7efe50b428c799a958ebd95663f06f1`  
		Last Modified: Tue, 12 Nov 2024 02:18:02 GMT  
		Size: 432.1 MB (432119108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:076de908a2013cd085e9c013c1b9e08e72eb157a10ffb51bd4604c606a87f1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3bfef88fdb9e387961677c041ca3023bc02898ac6410f622057a815324e42f`

```dockerfile
```

-	Layers:
	-	`sha256:59a1eebef8bd0f84de9373f30583cf8fff216a64c91cef46794b3df91b9741bf`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6b312905e6cdea17718ab5d78524c2288cdf017b00d3e1c97340840c65f53f`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7df0c5180c12b9d661f894efb8b5ee6beae08f4a35421d163752eb1cee68268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605555663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42849c84987e6132b7a3aa62ceda758eabeb6c799e9fb9850f154ea40a75c2fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f4bf514b87eda9f9cd384680952b857c4a970d832d9246cb3a9812a3323f50`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a352f50acc211706037a0fbbe15b26053829c42a5898733c942b029f20b5cc5`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42adddf2329e50d82fe1048f35545a318cc64ca37b29e5afbf0eccfd1e723f7c`  
		Last Modified: Tue, 12 Nov 2024 13:25:38 GMT  
		Size: 432.1 MB (432089166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:9b925d9bfc52ad18b06a1ed3f64c8996fd9948624406cc4cfdec20225f422b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e568224d5c038d92f1e46db372dffc5371966f458c9d0f71cdd766ba4fd7726`

```dockerfile
```

-	Layers:
	-	`sha256:122a15fcb5e810175925212f6e7ae5653294966f4146e39209405c165b0b3a4d`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde38be6ee16eb1296871262883a2a764918865e351840724ce17a62e76a78a0`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:7fb7633ffd3cd7af4359935f3338544d8d5f1b4aa83547cd22f29cf07de9e4f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:051ff55cc89d4f39244d7c8f6624cdb4f76e2d0bced398024401e9a7ad9de187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608119323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b5bb5e640b26f68c7c532f06f865ddadd03ca5f6ae03e528157930a270d84`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041b88a2fb9c472ecbfc772e45a3b018cd1a7668db24063bbe5f365310f80bd`  
		Last Modified: Tue, 12 Nov 2024 02:17:56 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdca0cd22c0d497293a8ad4f71d0f5700b326380f6b0214d63af64f8cfb8bb`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234f60c6542d45573c83ff2a04ab34b9b37c45445c3722c9bc163f0a548e6765`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ac141efee1dba0d9829a36fb80a5d5d7efe50b428c799a958ebd95663f06f1`  
		Last Modified: Tue, 12 Nov 2024 02:18:02 GMT  
		Size: 432.1 MB (432119108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:076de908a2013cd085e9c013c1b9e08e72eb157a10ffb51bd4604c606a87f1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3bfef88fdb9e387961677c041ca3023bc02898ac6410f622057a815324e42f`

```dockerfile
```

-	Layers:
	-	`sha256:59a1eebef8bd0f84de9373f30583cf8fff216a64c91cef46794b3df91b9741bf`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6b312905e6cdea17718ab5d78524c2288cdf017b00d3e1c97340840c65f53f`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7df0c5180c12b9d661f894efb8b5ee6beae08f4a35421d163752eb1cee68268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605555663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42849c84987e6132b7a3aa62ceda758eabeb6c799e9fb9850f154ea40a75c2fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f4bf514b87eda9f9cd384680952b857c4a970d832d9246cb3a9812a3323f50`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a352f50acc211706037a0fbbe15b26053829c42a5898733c942b029f20b5cc5`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42adddf2329e50d82fe1048f35545a318cc64ca37b29e5afbf0eccfd1e723f7c`  
		Last Modified: Tue, 12 Nov 2024 13:25:38 GMT  
		Size: 432.1 MB (432089166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9b925d9bfc52ad18b06a1ed3f64c8996fd9948624406cc4cfdec20225f422b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e568224d5c038d92f1e46db372dffc5371966f458c9d0f71cdd766ba4fd7726`

```dockerfile
```

-	Layers:
	-	`sha256:122a15fcb5e810175925212f6e7ae5653294966f4146e39209405c165b0b3a4d`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde38be6ee16eb1296871262883a2a764918865e351840724ce17a62e76a78a0`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:dbe034b56dea03f408a931a3f593749b0a9e8aefcd8407a9a667f94fe631e30b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:eb7d26f8e5ead80e799605278d16380a991f2bc3dafc9b23404c399ca50ed088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602989331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0146eeb6ab1d07c885d7f5f4d2f8203e9c67b7afda2da8d4ff01d1f7878decb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94888d00a904699c72d1d90a2aeb95340d8b59925baef8fec32e5036fc38e2c8`  
		Last Modified: Thu, 14 Nov 2024 21:15:54 GMT  
		Size: 133.8 MB (133849473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676dc572091818922be830009e8cf242ee6b45b3be100d7652ef200603891d9d`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d164037996f6f75c08b11d20d5a3b85ff117d87324776a537cc816bfb91add3`  
		Last Modified: Thu, 14 Nov 2024 21:15:59 GMT  
		Size: 429.2 MB (429194928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ff4957c27870f6ee18eec3ca66634fc4e23cd99651312378c31044c48da16553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9359eb512cd415988420ba6c2c2d15789edce332abcdaf11192e5a4d1ea2ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:c0318fceace1b81e55d26529026f1138f54ebf8d7a0e5853cdc52f17ba87dc64`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 7.8 MB (7845287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9527916085dd17b7156ec9e5e5ddad2ac0bec80081160653a462a58cbda96f78`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cf8ddd4a4a19363143504a084e334692ae40de92c6ad608976631e9ec088807b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601179946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07e06ed3bd0800eb1b33ac21eb14f7edf99aaffc414f736a44c74eb145a8143`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69476780d661de498dc83d2b1de4f2cc2e0611b28b4e4bf6add1abf522c9a14`  
		Last Modified: Thu, 14 Nov 2024 22:16:15 GMT  
		Size: 429.2 MB (429194876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c70b5c5046371b3124435c2dd865281650a93d1c81778ac62664e7316c469e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7846334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd090a674b8e05a5f334e3a574bf44cda482029f34b01daff75da38d36f5359`

```dockerfile
```

-	Layers:
	-	`sha256:2d05114788494df5ddd53077e3095770c30a10e4c1178ac5249fd72f52ff4923`  
		Last Modified: Thu, 14 Nov 2024 22:16:08 GMT  
		Size: 7.8 MB (7824852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6683551f820d8703a088e0ca7f578205df085bd5959fdd16fc678d2ede2897`  
		Last Modified: Thu, 14 Nov 2024 22:16:07 GMT  
		Size: 21.5 KB (21482 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-ubi9`

```console
$ docker pull neo4j@sha256:1c6ff1d77341a4dae5d291f77468d8b0a4b01e2dcd49fa3f028d313c4af6192f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0ae83b4f9a2dedcaadfa6844a63612e8f39b1ff62a460409450241f6a214f7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313977097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b053dce1567d461f41b43539e7dae9b035e1a35a52e48ec06381b37653342`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb9f3e565eddc4e6833ebfb7077dbd469a5a4874268cd311fe37f1ee2b75b0`  
		Last Modified: Thu, 14 Nov 2024 21:14:39 GMT  
		Size: 133.9 MB (133850178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f0b6a673e6094870d3fdcd971696e979ba06c4055bb71844990194ee0537f`  
		Last Modified: Thu, 14 Nov 2024 21:14:35 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fb302b729093912e6e27c03014aec2c709c8ed5a9fb6cbac7a1a90ceb153`  
		Last Modified: Thu, 14 Nov 2024 21:14:40 GMT  
		Size: 140.2 MB (140181995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:39c07d43b72067a79d8da50266778002a1a92754f1e18652714aba0af55a6b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91c22e365051a37674d6d2d5a1673bab3668e6394d139aa3e488ec196b37968`

```dockerfile
```

-	Layers:
	-	`sha256:f48868b73c0e3f1f0c76682981e24cd25c400496d4ad71d00da44a47e31d896a`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47af631d4e7bc6cbb58095ac368d0bdfce715ebb0563cb7d4056006d11780111`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3c9470d2ca0b5cdc4aaea86e6f603f5020ffd2689ea1c09e4e8342e0144c7711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312167053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855932b135b8129e38fa94544e1da7b7dd0d6089503454ab6c640f6905821ccb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e1f9bafff5c6a0d382530add91906d92f4e04a2984d0e4eae6bda09fa3f6a`  
		Last Modified: Thu, 14 Nov 2024 22:12:03 GMT  
		Size: 140.2 MB (140181983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f3d5acb84ada99f13323a9aff91bd653c9a2bf26b9effa8964959768771565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c7f48a798c31b5b41a43637af8a544d0ead54b82f4f56acc0191d9ce42d5`

```dockerfile
```

-	Layers:
	-	`sha256:6b1ea43e81e1c8d817e1b311e6ab374f89f6b395959b5fa6b2bf106afd69ac1f`  
		Last Modified: Thu, 14 Nov 2024 22:12:00 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c52a6d585d2378742329a9080fd834eb501cb397e61e36b8d5e967e29b8d5b`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:1c6ff1d77341a4dae5d291f77468d8b0a4b01e2dcd49fa3f028d313c4af6192f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0ae83b4f9a2dedcaadfa6844a63612e8f39b1ff62a460409450241f6a214f7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313977097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b053dce1567d461f41b43539e7dae9b035e1a35a52e48ec06381b37653342`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb9f3e565eddc4e6833ebfb7077dbd469a5a4874268cd311fe37f1ee2b75b0`  
		Last Modified: Thu, 14 Nov 2024 21:14:39 GMT  
		Size: 133.9 MB (133850178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f0b6a673e6094870d3fdcd971696e979ba06c4055bb71844990194ee0537f`  
		Last Modified: Thu, 14 Nov 2024 21:14:35 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fb302b729093912e6e27c03014aec2c709c8ed5a9fb6cbac7a1a90ceb153`  
		Last Modified: Thu, 14 Nov 2024 21:14:40 GMT  
		Size: 140.2 MB (140181995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:39c07d43b72067a79d8da50266778002a1a92754f1e18652714aba0af55a6b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91c22e365051a37674d6d2d5a1673bab3668e6394d139aa3e488ec196b37968`

```dockerfile
```

-	Layers:
	-	`sha256:f48868b73c0e3f1f0c76682981e24cd25c400496d4ad71d00da44a47e31d896a`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47af631d4e7bc6cbb58095ac368d0bdfce715ebb0563cb7d4056006d11780111`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3c9470d2ca0b5cdc4aaea86e6f603f5020ffd2689ea1c09e4e8342e0144c7711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312167053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855932b135b8129e38fa94544e1da7b7dd0d6089503454ab6c640f6905821ccb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e1f9bafff5c6a0d382530add91906d92f4e04a2984d0e4eae6bda09fa3f6a`  
		Last Modified: Thu, 14 Nov 2024 22:12:03 GMT  
		Size: 140.2 MB (140181983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f3d5acb84ada99f13323a9aff91bd653c9a2bf26b9effa8964959768771565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c7f48a798c31b5b41a43637af8a544d0ead54b82f4f56acc0191d9ce42d5`

```dockerfile
```

-	Layers:
	-	`sha256:6b1ea43e81e1c8d817e1b311e6ab374f89f6b395959b5fa6b2bf106afd69ac1f`  
		Last Modified: Thu, 14 Nov 2024 22:12:00 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c52a6d585d2378742329a9080fd834eb501cb397e61e36b8d5e967e29b8d5b`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:7fb7633ffd3cd7af4359935f3338544d8d5f1b4aa83547cd22f29cf07de9e4f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:051ff55cc89d4f39244d7c8f6624cdb4f76e2d0bced398024401e9a7ad9de187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608119323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b5bb5e640b26f68c7c532f06f865ddadd03ca5f6ae03e528157930a270d84`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041b88a2fb9c472ecbfc772e45a3b018cd1a7668db24063bbe5f365310f80bd`  
		Last Modified: Tue, 12 Nov 2024 02:17:56 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdca0cd22c0d497293a8ad4f71d0f5700b326380f6b0214d63af64f8cfb8bb`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234f60c6542d45573c83ff2a04ab34b9b37c45445c3722c9bc163f0a548e6765`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ac141efee1dba0d9829a36fb80a5d5d7efe50b428c799a958ebd95663f06f1`  
		Last Modified: Tue, 12 Nov 2024 02:18:02 GMT  
		Size: 432.1 MB (432119108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:076de908a2013cd085e9c013c1b9e08e72eb157a10ffb51bd4604c606a87f1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3bfef88fdb9e387961677c041ca3023bc02898ac6410f622057a815324e42f`

```dockerfile
```

-	Layers:
	-	`sha256:59a1eebef8bd0f84de9373f30583cf8fff216a64c91cef46794b3df91b9741bf`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6b312905e6cdea17718ab5d78524c2288cdf017b00d3e1c97340840c65f53f`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7df0c5180c12b9d661f894efb8b5ee6beae08f4a35421d163752eb1cee68268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605555663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42849c84987e6132b7a3aa62ceda758eabeb6c799e9fb9850f154ea40a75c2fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f4bf514b87eda9f9cd384680952b857c4a970d832d9246cb3a9812a3323f50`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a352f50acc211706037a0fbbe15b26053829c42a5898733c942b029f20b5cc5`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42adddf2329e50d82fe1048f35545a318cc64ca37b29e5afbf0eccfd1e723f7c`  
		Last Modified: Tue, 12 Nov 2024 13:25:38 GMT  
		Size: 432.1 MB (432089166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:9b925d9bfc52ad18b06a1ed3f64c8996fd9948624406cc4cfdec20225f422b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e568224d5c038d92f1e46db372dffc5371966f458c9d0f71cdd766ba4fd7726`

```dockerfile
```

-	Layers:
	-	`sha256:122a15fcb5e810175925212f6e7ae5653294966f4146e39209405c165b0b3a4d`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde38be6ee16eb1296871262883a2a764918865e351840724ce17a62e76a78a0`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:7fb7633ffd3cd7af4359935f3338544d8d5f1b4aa83547cd22f29cf07de9e4f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:051ff55cc89d4f39244d7c8f6624cdb4f76e2d0bced398024401e9a7ad9de187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608119323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125b5bb5e640b26f68c7c532f06f865ddadd03ca5f6ae03e528157930a270d84`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2041b88a2fb9c472ecbfc772e45a3b018cd1a7668db24063bbe5f365310f80bd`  
		Last Modified: Tue, 12 Nov 2024 02:17:56 GMT  
		Size: 144.5 MB (144534759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdca0cd22c0d497293a8ad4f71d0f5700b326380f6b0214d63af64f8cfb8bb`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234f60c6542d45573c83ff2a04ab34b9b37c45445c3722c9bc163f0a548e6765`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ac141efee1dba0d9829a36fb80a5d5d7efe50b428c799a958ebd95663f06f1`  
		Last Modified: Tue, 12 Nov 2024 02:18:02 GMT  
		Size: 432.1 MB (432119108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:076de908a2013cd085e9c013c1b9e08e72eb157a10ffb51bd4604c606a87f1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da3bfef88fdb9e387961677c041ca3023bc02898ac6410f622057a815324e42f`

```dockerfile
```

-	Layers:
	-	`sha256:59a1eebef8bd0f84de9373f30583cf8fff216a64c91cef46794b3df91b9741bf`  
		Last Modified: Tue, 12 Nov 2024 02:17:53 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6b312905e6cdea17718ab5d78524c2288cdf017b00d3e1c97340840c65f53f`  
		Last Modified: Tue, 12 Nov 2024 02:17:52 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:7df0c5180c12b9d661f894efb8b5ee6beae08f4a35421d163752eb1cee68268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605555663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42849c84987e6132b7a3aa62ceda758eabeb6c799e9fb9850f154ea40a75c2fd`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f4bf514b87eda9f9cd384680952b857c4a970d832d9246cb3a9812a3323f50`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a352f50acc211706037a0fbbe15b26053829c42a5898733c942b029f20b5cc5`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42adddf2329e50d82fe1048f35545a318cc64ca37b29e5afbf0eccfd1e723f7c`  
		Last Modified: Tue, 12 Nov 2024 13:25:38 GMT  
		Size: 432.1 MB (432089166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9b925d9bfc52ad18b06a1ed3f64c8996fd9948624406cc4cfdec20225f422b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e568224d5c038d92f1e46db372dffc5371966f458c9d0f71cdd766ba4fd7726`

```dockerfile
```

-	Layers:
	-	`sha256:122a15fcb5e810175925212f6e7ae5653294966f4146e39209405c165b0b3a4d`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde38be6ee16eb1296871262883a2a764918865e351840724ce17a62e76a78a0`  
		Last Modified: Tue, 12 Nov 2024 13:25:28 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:dbe034b56dea03f408a931a3f593749b0a9e8aefcd8407a9a667f94fe631e30b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:eb7d26f8e5ead80e799605278d16380a991f2bc3dafc9b23404c399ca50ed088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602989331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0146eeb6ab1d07c885d7f5f4d2f8203e9c67b7afda2da8d4ff01d1f7878decb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94888d00a904699c72d1d90a2aeb95340d8b59925baef8fec32e5036fc38e2c8`  
		Last Modified: Thu, 14 Nov 2024 21:15:54 GMT  
		Size: 133.8 MB (133849473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676dc572091818922be830009e8cf242ee6b45b3be100d7652ef200603891d9d`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d164037996f6f75c08b11d20d5a3b85ff117d87324776a537cc816bfb91add3`  
		Last Modified: Thu, 14 Nov 2024 21:15:59 GMT  
		Size: 429.2 MB (429194928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ff4957c27870f6ee18eec3ca66634fc4e23cd99651312378c31044c48da16553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9359eb512cd415988420ba6c2c2d15789edce332abcdaf11192e5a4d1ea2ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:c0318fceace1b81e55d26529026f1138f54ebf8d7a0e5853cdc52f17ba87dc64`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 7.8 MB (7845287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9527916085dd17b7156ec9e5e5ddad2ac0bec80081160653a462a58cbda96f78`  
		Last Modified: Thu, 14 Nov 2024 21:15:52 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:cf8ddd4a4a19363143504a084e334692ae40de92c6ad608976631e9ec088807b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601179946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07e06ed3bd0800eb1b33ac21eb14f7edf99aaffc414f736a44c74eb145a8143`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=34691d29bb1add0ca4e189eb5cc16da057ede9934f599f3ebd628c3f548759e3 NEO4J_TARBALL=neo4j-enterprise-5.25.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69476780d661de498dc83d2b1de4f2cc2e0611b28b4e4bf6add1abf522c9a14`  
		Last Modified: Thu, 14 Nov 2024 22:16:15 GMT  
		Size: 429.2 MB (429194876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:c70b5c5046371b3124435c2dd865281650a93d1c81778ac62664e7316c469e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7846334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd090a674b8e05a5f334e3a574bf44cda482029f34b01daff75da38d36f5359`

```dockerfile
```

-	Layers:
	-	`sha256:2d05114788494df5ddd53077e3095770c30a10e4c1178ac5249fd72f52ff4923`  
		Last Modified: Thu, 14 Nov 2024 22:16:08 GMT  
		Size: 7.8 MB (7824852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e6683551f820d8703a088e0ca7f578205df085bd5959fdd16fc678d2ede2897`  
		Last Modified: Thu, 14 Nov 2024 22:16:07 GMT  
		Size: 21.5 KB (21482 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:2858b77dc78727aa8e0356ca03b7081582095dd2230d1fcfd13c3553048b350a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:1827d0915d05e0c47d19f4706f850afdcaa02ce7c9d46da9d5e71939a9462d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319111015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ce681f60e20bf2902952828883ada8376c12126eafc9ceffcbd05061bc5a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfb93aa49b4ca4b4cfc2702992795cada6f72d13c5b5f983104b24da5ccbb64`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 144.5 MB (144534782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02527cdce608d4247f2b4118ae67dfc84006aa79617d5af4d9af3262ae313e8`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f70db6b372df6e05256fb0c42114ba459b709b77731ffbde90942f256115211`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af48ff0aaf891a792b16df9ede46009c4d7ef904993fd242af727b6429f06e2`  
		Last Modified: Tue, 12 Nov 2024 02:16:35 GMT  
		Size: 143.1 MB (143110775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:8209538f566ac7d365e9ea0407e07e6868abadba0e1fc95decd9c273db206388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418f9b026c9eb16ad648767fe2ed281fbb472e2e3139538acd088bffa8da6b14`

```dockerfile
```

-	Layers:
	-	`sha256:ed178cfcc05b69201330e3983871839c340285daaf6f9e20b9beb375f797410c`  
		Last Modified: Tue, 12 Nov 2024 02:16:32 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b8840702b0ba669137892b9b0aa756a9c1416d71a9bca2028de6220beabd58`  
		Last Modified: Tue, 12 Nov 2024 02:16:31 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:810a2c942c0cee7d0dc3c204fe68f2e7c9bada63aad1c84bf67e32f222227299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2430ce4731a7e5946ccb4580cf0a85f91eef0ffcb7dfbe1be1143b81714a900f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 30 Oct 2024 15:39:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6526161e37718eb3c317bb21e8cb53e4226e4514310e95e0acafe07e94e442f2`  
		Last Modified: Tue, 12 Nov 2024 13:21:11 GMT  
		Size: 143.4 MB (143360973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eb9ec213af138bfb9b39cf73864117057fb6bdcb5d289be1b1dac735d1fb25`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9140b544340c7fe3e2f42ac6e7c1a13b3630f20d1690536f8ce5b852bc0f8ff9`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4360957302c371ad24398ee81d1a4e8410b9edc286230f60a162461a54cc1a7d`  
		Last Modified: Tue, 12 Nov 2024 13:21:12 GMT  
		Size: 143.1 MB (143080266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:c9a2ed68e94e8cd40b5052122b93b560a741be006940af93e4067e5d2687789f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56715678d6aba3dd8bce2645ef7c0ab0c1f375bd2674481936a0ddc23130fa0a`

```dockerfile
```

-	Layers:
	-	`sha256:f404035e3502bd9c60b885f804380d590c3786a95c0a182a8c0cbf82745e08c4`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34cfca4f7fe68b91375adb208d8965deb6c7b61721c3ece8c9545beb04506538`  
		Last Modified: Tue, 12 Nov 2024 13:21:08 GMT  
		Size: 24.0 KB (24039 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:1c6ff1d77341a4dae5d291f77468d8b0a4b01e2dcd49fa3f028d313c4af6192f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0ae83b4f9a2dedcaadfa6844a63612e8f39b1ff62a460409450241f6a214f7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313977097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b053dce1567d461f41b43539e7dae9b035e1a35a52e48ec06381b37653342`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:45c667d4bed394050d06fa644ce9574d9fe75c2ed92a12e23fb5b733428b21f6 in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:20:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:d2e5d6c907c71aea278da1e0e3424927afce03a253cba174efe5392fcba72b55`  
		Last Modified: Wed, 13 Nov 2024 18:56:52 GMT  
		Size: 39.9 MB (39871319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b6ec0388eddfe9b76df03c99092e0ca82d8a980895ea6ec4f7d925e674d7c5`  
		Last Modified: Wed, 13 Nov 2024 18:56:51 GMT  
		Size: 63.6 KB (63553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bb9f3e565eddc4e6833ebfb7077dbd469a5a4874268cd311fe37f1ee2b75b0`  
		Last Modified: Thu, 14 Nov 2024 21:14:39 GMT  
		Size: 133.9 MB (133850178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233f0b6a673e6094870d3fdcd971696e979ba06c4055bb71844990194ee0537f`  
		Last Modified: Thu, 14 Nov 2024 21:14:35 GMT  
		Size: 10.0 KB (10020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc3fb302b729093912e6e27c03014aec2c709c8ed5a9fb6cbac7a1a90ceb153`  
		Last Modified: Thu, 14 Nov 2024 21:14:40 GMT  
		Size: 140.2 MB (140181995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:39c07d43b72067a79d8da50266778002a1a92754f1e18652714aba0af55a6b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91c22e365051a37674d6d2d5a1673bab3668e6394d139aa3e488ec196b37968`

```dockerfile
```

-	Layers:
	-	`sha256:f48868b73c0e3f1f0c76682981e24cd25c400496d4ad71d00da44a47e31d896a`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47af631d4e7bc6cbb58095ac368d0bdfce715ebb0563cb7d4056006d11780111`  
		Last Modified: Thu, 14 Nov 2024 21:14:36 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3c9470d2ca0b5cdc4aaea86e6f603f5020ffd2689ea1c09e4e8342e0144c7711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312167053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855932b135b8129e38fa94544e1da7b7dd0d6089503454ab6c640f6905821ccb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL url="https://www.redhat.com"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 30 Oct 2024 15:39:25 GMT
ENV container oci
# Wed, 30 Oct 2024 15:39:25 GMT
COPY dir:e27ddab6b88291890d801136d36e16fa6ad2af7f2a7e00f455a75bd89d96622f in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-13T17:24:29" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="8389cd46e6826a07db9fbf425dd110900e32c6f9" "build-date"="2024-11-13T17:16:40Z" "release"="1731518200"
# Wed, 30 Oct 2024 15:39:25 GMT
RUN /bin/sh
# Wed, 30 Oct 2024 15:39:25 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV NEO4J_SHA256=7dae6bfca596e0c3fbcf12ad8897e95277601047d1253b44c6a513983ede6859 NEO4J_TARBALL=neo4j-community-5.25.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Wed, 30 Oct 2024 15:39:25 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
# Wed, 30 Oct 2024 15:39:25 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.25.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Wed, 30 Oct 2024 15:39:25 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Oct 2024 15:39:25 GMT
WORKDIR /var/lib/neo4j
# Wed, 30 Oct 2024 15:39:25 GMT
VOLUME [/data /logs]
# Wed, 30 Oct 2024 15:39:25 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 30 Oct 2024 15:39:25 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:636ce8d23eab8a4456a354f6ee07a387ed3d02c854cfe9deacc58ab7259339bf`  
		Last Modified: Wed, 13 Nov 2024 19:37:14 GMT  
		Size: 38.1 MB (38073783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce756de279cd0aa23acc884e1d32ccff7fef4582b5922432ba03c8fe651a180b`  
		Last Modified: Wed, 13 Nov 2024 19:37:13 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800c74bd8490261aed4586a8606c80584d9c07e901bdee8a76d46a1eb0f2bfd`  
		Last Modified: Thu, 14 Nov 2024 22:12:02 GMT  
		Size: 133.8 MB (133837625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0136ec65b9b6bffcdb44ac806013bcdaf380819c89bef2d2eec6c8f2af8395`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335e1f9bafff5c6a0d382530add91906d92f4e04a2984d0e4eae6bda09fa3f6a`  
		Last Modified: Thu, 14 Nov 2024 22:12:03 GMT  
		Size: 140.2 MB (140181983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f3d5acb84ada99f13323a9aff91bd653c9a2bf26b9effa8964959768771565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560c7f48a798c31b5b41a43637af8a544d0ead54b82f4f56acc0191d9ce42d5`

```dockerfile
```

-	Layers:
	-	`sha256:6b1ea43e81e1c8d817e1b311e6ab374f89f6b395959b5fa6b2bf106afd69ac1f`  
		Last Modified: Thu, 14 Nov 2024 22:12:00 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c52a6d585d2378742329a9080fd834eb501cb397e61e36b8d5e967e29b8d5b`  
		Last Modified: Thu, 14 Nov 2024 22:11:59 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json
