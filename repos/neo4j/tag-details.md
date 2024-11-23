<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.39`](#neo4j4439)
-	[`neo4j:4.4.39-community`](#neo4j4439-community)
-	[`neo4j:4.4.39-enterprise`](#neo4j4439-enterprise)
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
$ docker pull neo4j@sha256:ba940670fd65b79e94923a5a6b8a642c7165b88d7746d272d3527c221422e427
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:00f3bfa93b1c8b74436508ba9c308bf32bd88fec56112def158c1115e84445e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306155852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64ab8bb6a78bdd39c2d33227d5e66349acad073d862872f5bc0d5fcab23ae78`
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
	-	`sha256:5d10abbb4489bd29b1d05df0973d5033c4770b808331c0f692293345cf9fc0b0`  
		Last Modified: Sat, 16 Nov 2024 03:51:26 GMT  
		Size: 145.6 MB (145601404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254efdd988aa57ea1a2fd57947ebaf281a6cc2f17fd573306f0971cb4f86254`  
		Last Modified: Sat, 16 Nov 2024 03:51:24 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6b23f2c9e8b680b5e6dbfec1fcc240aa7bd1db7019c2eab78a902124ad923e`  
		Last Modified: Sat, 16 Nov 2024 03:51:24 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e84719564db91c85eed514d0670e002ae7c5d597c747a295e97db6e2a3d9e3`  
		Last Modified: Sat, 16 Nov 2024 03:51:25 GMT  
		Size: 129.1 MB (129089053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:102400600996bfe08afaa8ee75545ba544f12a3db868104bb780254aa89ef515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75af8ae34dff6c6d032ded3e2ea7219d9bf18b3221cec93a15d32913d442b7b`

```dockerfile
```

-	Layers:
	-	`sha256:c180d882f94ad80d5d93080a28199911f4f34ce5b802d42af84614657f9b1026`  
		Last Modified: Sat, 16 Nov 2024 03:51:24 GMT  
		Size: 3.2 MB (3202059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07a31c95e82baa5ef30f200c19ef888995c7764ed2f04ff46b3b44b093ac389`  
		Last Modified: Sat, 16 Nov 2024 03:51:24 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee9e38f32aa67c7fbcf7655ed98bda9601dc4fc6aa875b771e7f7dd3283ddd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301547458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f7d962f31869b352a6fe2ed1f4b368a174f42c10c582bea6bb63480b351124`
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
	-	`sha256:2e006532f22d92e9d5637b1cc7ac1a8afef6c6963132343754ef28d006467ca3`  
		Last Modified: Sat, 16 Nov 2024 04:39:49 GMT  
		Size: 142.4 MB (142389148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ed05a5ef7b403fba6ddf846b953f4e72f589d8e54a4fd7de9a65bb149e578b`  
		Last Modified: Sat, 16 Nov 2024 04:39:45 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d6b8ce9916363dc613a4121f97069ab995ca2a60a9670109742de3ab3627ab`  
		Last Modified: Sat, 16 Nov 2024 04:39:45 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9702a148bf6c91f7d2ba563c42dbb66c7ffd4cdbf46ab27375eda8a99fe1ccdc`  
		Last Modified: Sat, 16 Nov 2024 04:39:49 GMT  
		Size: 129.1 MB (129052846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:d7fe3ff4356c1b5cebeab84fea0e4e2e5d3971874c21c35a028118e85b5175de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0f8120f99526993183ea67a2176832c456e5b8b9fc04744abe25c11bc178dd`

```dockerfile
```

-	Layers:
	-	`sha256:c870dbfb88e02f77a69bc036e7904d05af78b9bff56889896c5e0b70df0cbdd8`  
		Last Modified: Sat, 16 Nov 2024 04:39:46 GMT  
		Size: 3.2 MB (3202322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b00eeaddec5896d529f81e45470b4ee39d86bbd83491dec4e12accb73b83d645`  
		Last Modified: Sat, 16 Nov 2024 04:39:45 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:ba940670fd65b79e94923a5a6b8a642c7165b88d7746d272d3527c221422e427
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:00f3bfa93b1c8b74436508ba9c308bf32bd88fec56112def158c1115e84445e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306155852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64ab8bb6a78bdd39c2d33227d5e66349acad073d862872f5bc0d5fcab23ae78`
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
	-	`sha256:5d10abbb4489bd29b1d05df0973d5033c4770b808331c0f692293345cf9fc0b0`  
		Last Modified: Sat, 16 Nov 2024 03:51:26 GMT  
		Size: 145.6 MB (145601404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2254efdd988aa57ea1a2fd57947ebaf281a6cc2f17fd573306f0971cb4f86254`  
		Last Modified: Sat, 16 Nov 2024 03:51:24 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6b23f2c9e8b680b5e6dbfec1fcc240aa7bd1db7019c2eab78a902124ad923e`  
		Last Modified: Sat, 16 Nov 2024 03:51:24 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e84719564db91c85eed514d0670e002ae7c5d597c747a295e97db6e2a3d9e3`  
		Last Modified: Sat, 16 Nov 2024 03:51:25 GMT  
		Size: 129.1 MB (129089053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:102400600996bfe08afaa8ee75545ba544f12a3db868104bb780254aa89ef515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75af8ae34dff6c6d032ded3e2ea7219d9bf18b3221cec93a15d32913d442b7b`

```dockerfile
```

-	Layers:
	-	`sha256:c180d882f94ad80d5d93080a28199911f4f34ce5b802d42af84614657f9b1026`  
		Last Modified: Sat, 16 Nov 2024 03:51:24 GMT  
		Size: 3.2 MB (3202059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e07a31c95e82baa5ef30f200c19ef888995c7764ed2f04ff46b3b44b093ac389`  
		Last Modified: Sat, 16 Nov 2024 03:51:24 GMT  
		Size: 20.0 KB (19957 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:ee9e38f32aa67c7fbcf7655ed98bda9601dc4fc6aa875b771e7f7dd3283ddd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301547458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f7d962f31869b352a6fe2ed1f4b368a174f42c10c582bea6bb63480b351124`
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
	-	`sha256:2e006532f22d92e9d5637b1cc7ac1a8afef6c6963132343754ef28d006467ca3`  
		Last Modified: Sat, 16 Nov 2024 04:39:49 GMT  
		Size: 142.4 MB (142389148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ed05a5ef7b403fba6ddf846b953f4e72f589d8e54a4fd7de9a65bb149e578b`  
		Last Modified: Sat, 16 Nov 2024 04:39:45 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d6b8ce9916363dc613a4121f97069ab995ca2a60a9670109742de3ab3627ab`  
		Last Modified: Sat, 16 Nov 2024 04:39:45 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9702a148bf6c91f7d2ba563c42dbb66c7ffd4cdbf46ab27375eda8a99fe1ccdc`  
		Last Modified: Sat, 16 Nov 2024 04:39:49 GMT  
		Size: 129.1 MB (129052846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d7fe3ff4356c1b5cebeab84fea0e4e2e5d3971874c21c35a028118e85b5175de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0f8120f99526993183ea67a2176832c456e5b8b9fc04744abe25c11bc178dd`

```dockerfile
```

-	Layers:
	-	`sha256:c870dbfb88e02f77a69bc036e7904d05af78b9bff56889896c5e0b70df0cbdd8`  
		Last Modified: Sat, 16 Nov 2024 04:39:46 GMT  
		Size: 3.2 MB (3202322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b00eeaddec5896d529f81e45470b4ee39d86bbd83491dec4e12accb73b83d645`  
		Last Modified: Sat, 16 Nov 2024 04:39:45 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:ba74ccdd888690081f1df448b9384d1ec40276b62fbae21dda8f267dc83fd118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:780245440e70d39b3de41808d91af0e8d94cfbe8d4904bd86aac96b3dacc411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.6 MB (410562178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e623075ddaa6eadcc95b0f7532def4d19ab10e591839b92c3a7065e44a0adf5e`
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
	-	`sha256:26b956fda217dbebe98bd096ee2cbe68eb968bcc57a0c2757b83efd9a3d7dfec`  
		Last Modified: Sat, 16 Nov 2024 04:51:45 GMT  
		Size: 145.6 MB (145601404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8132e12c0ad9cb0a935338d752ae1b204688cc1eeae5f327052696a0543dd196`  
		Last Modified: Sat, 16 Nov 2024 04:51:41 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906d05ca54846099deb75f7ef6f861b6f93d2f5dfadeb48519e1b139af4df48`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03ad8fbb60ae1652a52f38c2fc5ce44d03c42dcdbd409ce15051588b4b7c590`  
		Last Modified: Sat, 16 Nov 2024 04:51:49 GMT  
		Size: 233.5 MB (233495384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:408df8153017b1d3265a2ab75c7544a190adc9e4a6c2bb69f276baec3e761e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481481328216c210a8dc55ec2eb7c1381f2dc19bf5c45c4ec22a1366ee14087c`

```dockerfile
```

-	Layers:
	-	`sha256:37e5516355762c82d2b0b84565f9dbd64daeb55b81783f0c4c26280578c51c25`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.4 MB (3352748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baaa5c8f051e850b951faa0243baa45b9cb8ac1faf9340f84d7cb61adde2b607`  
		Last Modified: Sat, 16 Nov 2024 04:51:41 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:59aa522694ea42f90dc618cfdef80e4dad453d18987db6edffd48f52e2ce9957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.0 MB (405957358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b793c16b9b43f146732e62aaf7a953d5964197adc32f46c00b31012bc7e3e96c`
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
	-	`sha256:2e006532f22d92e9d5637b1cc7ac1a8afef6c6963132343754ef28d006467ca3`  
		Last Modified: Sat, 16 Nov 2024 04:39:49 GMT  
		Size: 142.4 MB (142389148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba3f4e12587974e3ea41d2b0263d3d13267fed978db9f4a304a4c34fea9c878`  
		Last Modified: Sat, 16 Nov 2024 04:42:15 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e824f002501a24ac34ce0beb83dd2ad257806871d53c0f236dfa9343e5cc87`  
		Last Modified: Sat, 16 Nov 2024 04:42:15 GMT  
		Size: 10.0 KB (9955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8280f836acdb6078a600e56c9370498fd3c1ae39895de61244d5a4457c4f2a1f`  
		Last Modified: Sat, 16 Nov 2024 04:42:20 GMT  
		Size: 233.5 MB (233462758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b4974f4dd0361f34a4d6b473f75760b3ccccdfec70712d34c54bc4c916059681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3372496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daeb339d6de3f54a078f9f9442274334b1ac8899090dac95f625ab4b78c3f47`

```dockerfile
```

-	Layers:
	-	`sha256:672ebe026976f5887231f69e5ba5fe5800d2d013fd67a5ae469735a989068e18`  
		Last Modified: Sat, 16 Nov 2024 04:42:16 GMT  
		Size: 3.4 MB (3352987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0313d3b511cd56dabce5870b4a40cebd0bdcfb5cfff7134853513d4dd0b762f`  
		Last Modified: Sat, 16 Nov 2024 04:42:15 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.39`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:4.4.39-community`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:4.4.39-enterprise`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:a139fcc8ee957cdf3186df77043bc97119dfa5bf0494d77fb91cab80612a7a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:41326e7635a2035a32f34285aae76a6e636cb982b8eb98557730f83188443afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313979634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2078d8e4f8ef123bb38a61258f7b5f015698c83217720c1885f5eb5076193`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d699ed19a7026bed8284e493e29672744eca2f26b5248dc1f209f26fd4b4e720`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 133.8 MB (133849264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0545597a6926348a3861fe4cebc1e5780454b640008aa6a37a56b7c133fd4`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2dc0545f98cb9e7ae40064e8245960ab37356d65e6b4e867e47f81b9f40a3a`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 140.2 MB (140181976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f350af5c1f6e522d3e266a704808496f6ef304e2f79506ba231f211a6732be04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd44ddf4be03a7e01f08e986e1395ac8d3811f87103a3214c76d77c9a18b07fd`

```dockerfile
```

-	Layers:
	-	`sha256:07068aba371864da822b89dbebba307519efd071797d7dc00e185a7df5bd83c3`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329a77b5a6a6b8d5c79710aabe6032712bd60124fa3b80246f62c1637e7fba24`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 22.5 KB (22546 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9eb57a6a15b5ea6cb79e1b602c05ac8f233b11d94b087fe2e58be28199501ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52c24e501b46cf8aa6f3f298a6148344f9cadc754635eaa9c961d0aa47ce17`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0baeef380d77fbef249485e41e036948fc46a16d1464c2a56469d4b115c44`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 140.2 MB (140182027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:23d5318cd77b4696006651f18d2e052319ed676ca8c1e176e2ae5d2d5bde4347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637b08ebfd76de82609504fe00226018254ea3956b62a99294099c41377f90f`

```dockerfile
```

-	Layers:
	-	`sha256:f022d71c37a0903b948c6df78781707920eca464cbc0688083a44ea78dfdf284`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f83c569248fc613179fdb4b014c51a840f5ed08b7709c13c5bc90c740230331`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:6dab977d6cd6db4509dc379a227aa89cc0bbd93256d4cafbfb08cc43d5341e9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5b27268a3ff3295d3ead4c84eba8023d5eb29dc2981f0fea62db8e3ca9aea718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608121269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917edbc58a0d8126cd3fcfa66d84b43a6bcf12967d795291a67d5a6d93a4c233`
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
	-	`sha256:2e1a37447ddb0fdbdcaf9e583d14f96efc209fd3e964041998ef0f8443a55edf`  
		Last Modified: Sat, 16 Nov 2024 04:53:09 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7686ec4f5ba0e9697bd592326ea50d7a955b424ca0e697aa7f941f03c33dfb`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08c95a8b2fc276d3677ae5c817e606eb373b82b28be6fa62a904e8a8fb714d`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d50af54b276030bb4e8a8f74b1eba5ecba3b03c914f3a4d4b71d855334757d0`  
		Last Modified: Sat, 16 Nov 2024 04:53:12 GMT  
		Size: 432.1 MB (432119089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2fe3dd728c22ef80d4e6c1ede09c4e394eb375b65a54db6dfd8adeb798b1ac57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c67473f3c1848b1d86097593b5491a51c721d92122e40fddb66099ac4c0b96a`

```dockerfile
```

-	Layers:
	-	`sha256:4e9fda4a6f6cef1d5bbe90abdd6d7ac5baa743758f590dd768e9a376bb0b5b8e`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd8b93e4d9dcfdf009aceb88928aab4b1d5d2ba01a6749e9287ad1925d4cc72`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e55df648c2510c05b32e7421166be2a6b9f786ceb239419e8a421a9fe212c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605556095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ee29ac1fc0b94318e12e9e7a4d2fce5848339dae92fbd0659bb8bfad4133`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcaebee5a6a52dc8e7bd800d7d9927c19604e85c43dc3b60c8aaf9b5b823f6`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35c68471bc924b8ef806d0c9f01331f7f7677c46650b6dfa7d6c23c7d70bb62`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897dc78dfe0cd203f3c122ca3369c5723a18a8fccfe4087091a30459a94dc9c`  
		Last Modified: Sat, 16 Nov 2024 04:37:35 GMT  
		Size: 432.1 MB (432089569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab8b8847d096d63380d9d1428011278dea087edb347e467d1689f2e2406a4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0079edc9cb04d1f1c116433bbcdf22bf4d6718b580c0106f018f9ea6960724c4`

```dockerfile
```

-	Layers:
	-	`sha256:e0c1a0dc39455b0e801e995eee407611f5c8a9c1d5832f02d73401d051223e71`  
		Last Modified: Sat, 16 Nov 2024 04:37:23 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aebd3f28437d8b4264c3adf90ef3cc42d92402b575da43c3368b9a3fcc0878`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:6dab977d6cd6db4509dc379a227aa89cc0bbd93256d4cafbfb08cc43d5341e9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5b27268a3ff3295d3ead4c84eba8023d5eb29dc2981f0fea62db8e3ca9aea718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608121269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917edbc58a0d8126cd3fcfa66d84b43a6bcf12967d795291a67d5a6d93a4c233`
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
	-	`sha256:2e1a37447ddb0fdbdcaf9e583d14f96efc209fd3e964041998ef0f8443a55edf`  
		Last Modified: Sat, 16 Nov 2024 04:53:09 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7686ec4f5ba0e9697bd592326ea50d7a955b424ca0e697aa7f941f03c33dfb`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08c95a8b2fc276d3677ae5c817e606eb373b82b28be6fa62a904e8a8fb714d`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d50af54b276030bb4e8a8f74b1eba5ecba3b03c914f3a4d4b71d855334757d0`  
		Last Modified: Sat, 16 Nov 2024 04:53:12 GMT  
		Size: 432.1 MB (432119089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2fe3dd728c22ef80d4e6c1ede09c4e394eb375b65a54db6dfd8adeb798b1ac57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c67473f3c1848b1d86097593b5491a51c721d92122e40fddb66099ac4c0b96a`

```dockerfile
```

-	Layers:
	-	`sha256:4e9fda4a6f6cef1d5bbe90abdd6d7ac5baa743758f590dd768e9a376bb0b5b8e`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd8b93e4d9dcfdf009aceb88928aab4b1d5d2ba01a6749e9287ad1925d4cc72`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e55df648c2510c05b32e7421166be2a6b9f786ceb239419e8a421a9fe212c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605556095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ee29ac1fc0b94318e12e9e7a4d2fce5848339dae92fbd0659bb8bfad4133`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcaebee5a6a52dc8e7bd800d7d9927c19604e85c43dc3b60c8aaf9b5b823f6`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35c68471bc924b8ef806d0c9f01331f7f7677c46650b6dfa7d6c23c7d70bb62`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897dc78dfe0cd203f3c122ca3369c5723a18a8fccfe4087091a30459a94dc9c`  
		Last Modified: Sat, 16 Nov 2024 04:37:35 GMT  
		Size: 432.1 MB (432089569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab8b8847d096d63380d9d1428011278dea087edb347e467d1689f2e2406a4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0079edc9cb04d1f1c116433bbcdf22bf4d6718b580c0106f018f9ea6960724c4`

```dockerfile
```

-	Layers:
	-	`sha256:e0c1a0dc39455b0e801e995eee407611f5c8a9c1d5832f02d73401d051223e71`  
		Last Modified: Sat, 16 Nov 2024 04:37:23 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aebd3f28437d8b4264c3adf90ef3cc42d92402b575da43c3368b9a3fcc0878`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:8937a8a5059935eca9ba6075631174d00b110df58b877aee7865a247bc486c0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1f61f9a4c8374389288cd2cc5753fec284a3d71080648dcc7c657dfbf8d31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602992361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65f1f2310b1f9cb0310843343fade6acdef09234f36d4d6c1703921cd5ffc0f`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7cda7184de2dad5787aa22199072aa2ce5f3806a7393d91ee6819c6a2e72f`  
		Last Modified: Sat, 16 Nov 2024 02:12:53 GMT  
		Size: 133.8 MB (133849116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6c5b72b6452a0bdf04a0ac3995b02c08d9cba4e98ea10d2d96e1ae46b5c8e`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186fd32f31064cd20cfe94fd992bc97636bbfcff0d38aec5f20b3ddf2e7455c7`  
		Last Modified: Sat, 16 Nov 2024 02:12:57 GMT  
		Size: 429.2 MB (429194852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8248223725b6bdacd1c74e03983ca72b4ed8d2a5fe8c00fe9da2e75d6c2be7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3595cec09e93914c7f923aa756a235bd7bedfacbaf9f2e2281eae3e7cb3b72b4`

```dockerfile
```

-	Layers:
	-	`sha256:1603dfef5b32c1f3ff7e7d27f8df6398b9228c763b094010dd5b95d563e8b8c7`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 7.8 MB (7845287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0fc3d860033b379ff26a7bcb1047adc80b24707c58a5fd0b596d584d3ff9d0`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6e344a04225b9065cbb797a0b3d6e1083077c80de13d8b285b1cf96012f1a1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601154760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9858ac8e905ff7328c263884ffbf9d5bb979abcb8693688ea0fe157285374334`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76dd95a74c1cdb225698384ce1587b03f3a5f6f7275ded7db6a54fbacd9e00e`  
		Last Modified: Sat, 16 Nov 2024 02:48:12 GMT  
		Size: 429.2 MB (429194940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a1eb5f018a3eec4f4b812465511ff5d3feb8264785e6269f2d5cbd2d9ffc8523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7846334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff749f721c0048b393b0874e02e842cb965452a634261478d32d53ebb63f6ae`

```dockerfile
```

-	Layers:
	-	`sha256:6d198f202ed445d6babffd9d10ea2882e8d4b2653d34e8aecae755a63d9f0f8e`  
		Last Modified: Sat, 16 Nov 2024 02:48:05 GMT  
		Size: 7.8 MB (7824852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0ea6e302611c76ec6b665e1370d6fc44119489ff28c0f8dbf33574c8edde53`  
		Last Modified: Sat, 16 Nov 2024 02:48:04 GMT  
		Size: 21.5 KB (21482 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:a139fcc8ee957cdf3186df77043bc97119dfa5bf0494d77fb91cab80612a7a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:41326e7635a2035a32f34285aae76a6e636cb982b8eb98557730f83188443afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313979634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2078d8e4f8ef123bb38a61258f7b5f015698c83217720c1885f5eb5076193`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d699ed19a7026bed8284e493e29672744eca2f26b5248dc1f209f26fd4b4e720`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 133.8 MB (133849264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0545597a6926348a3861fe4cebc1e5780454b640008aa6a37a56b7c133fd4`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2dc0545f98cb9e7ae40064e8245960ab37356d65e6b4e867e47f81b9f40a3a`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 140.2 MB (140181976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f350af5c1f6e522d3e266a704808496f6ef304e2f79506ba231f211a6732be04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd44ddf4be03a7e01f08e986e1395ac8d3811f87103a3214c76d77c9a18b07fd`

```dockerfile
```

-	Layers:
	-	`sha256:07068aba371864da822b89dbebba307519efd071797d7dc00e185a7df5bd83c3`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329a77b5a6a6b8d5c79710aabe6032712bd60124fa3b80246f62c1637e7fba24`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 22.5 KB (22546 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9eb57a6a15b5ea6cb79e1b602c05ac8f233b11d94b087fe2e58be28199501ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52c24e501b46cf8aa6f3f298a6148344f9cadc754635eaa9c961d0aa47ce17`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0baeef380d77fbef249485e41e036948fc46a16d1464c2a56469d4b115c44`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 140.2 MB (140182027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:23d5318cd77b4696006651f18d2e052319ed676ca8c1e176e2ae5d2d5bde4347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637b08ebfd76de82609504fe00226018254ea3956b62a99294099c41377f90f`

```dockerfile
```

-	Layers:
	-	`sha256:f022d71c37a0903b948c6df78781707920eca464cbc0688083a44ea78dfdf284`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f83c569248fc613179fdb4b014c51a840f5ed08b7709c13c5bc90c740230331`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-bullseye`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-community`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-community` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-community-bullseye`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-community-ubi9`

```console
$ docker pull neo4j@sha256:a139fcc8ee957cdf3186df77043bc97119dfa5bf0494d77fb91cab80612a7a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:41326e7635a2035a32f34285aae76a6e636cb982b8eb98557730f83188443afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313979634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2078d8e4f8ef123bb38a61258f7b5f015698c83217720c1885f5eb5076193`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d699ed19a7026bed8284e493e29672744eca2f26b5248dc1f209f26fd4b4e720`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 133.8 MB (133849264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0545597a6926348a3861fe4cebc1e5780454b640008aa6a37a56b7c133fd4`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2dc0545f98cb9e7ae40064e8245960ab37356d65e6b4e867e47f81b9f40a3a`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 140.2 MB (140181976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f350af5c1f6e522d3e266a704808496f6ef304e2f79506ba231f211a6732be04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd44ddf4be03a7e01f08e986e1395ac8d3811f87103a3214c76d77c9a18b07fd`

```dockerfile
```

-	Layers:
	-	`sha256:07068aba371864da822b89dbebba307519efd071797d7dc00e185a7df5bd83c3`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329a77b5a6a6b8d5c79710aabe6032712bd60124fa3b80246f62c1637e7fba24`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 22.5 KB (22546 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9eb57a6a15b5ea6cb79e1b602c05ac8f233b11d94b087fe2e58be28199501ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52c24e501b46cf8aa6f3f298a6148344f9cadc754635eaa9c961d0aa47ce17`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0baeef380d77fbef249485e41e036948fc46a16d1464c2a56469d4b115c44`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 140.2 MB (140182027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:23d5318cd77b4696006651f18d2e052319ed676ca8c1e176e2ae5d2d5bde4347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637b08ebfd76de82609504fe00226018254ea3956b62a99294099c41377f90f`

```dockerfile
```

-	Layers:
	-	`sha256:f022d71c37a0903b948c6df78781707920eca464cbc0688083a44ea78dfdf284`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f83c569248fc613179fdb4b014c51a840f5ed08b7709c13c5bc90c740230331`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-enterprise`

```console
$ docker pull neo4j@sha256:6dab977d6cd6db4509dc379a227aa89cc0bbd93256d4cafbfb08cc43d5341e9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5b27268a3ff3295d3ead4c84eba8023d5eb29dc2981f0fea62db8e3ca9aea718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608121269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917edbc58a0d8126cd3fcfa66d84b43a6bcf12967d795291a67d5a6d93a4c233`
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
	-	`sha256:2e1a37447ddb0fdbdcaf9e583d14f96efc209fd3e964041998ef0f8443a55edf`  
		Last Modified: Sat, 16 Nov 2024 04:53:09 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7686ec4f5ba0e9697bd592326ea50d7a955b424ca0e697aa7f941f03c33dfb`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08c95a8b2fc276d3677ae5c817e606eb373b82b28be6fa62a904e8a8fb714d`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d50af54b276030bb4e8a8f74b1eba5ecba3b03c914f3a4d4b71d855334757d0`  
		Last Modified: Sat, 16 Nov 2024 04:53:12 GMT  
		Size: 432.1 MB (432119089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2fe3dd728c22ef80d4e6c1ede09c4e394eb375b65a54db6dfd8adeb798b1ac57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c67473f3c1848b1d86097593b5491a51c721d92122e40fddb66099ac4c0b96a`

```dockerfile
```

-	Layers:
	-	`sha256:4e9fda4a6f6cef1d5bbe90abdd6d7ac5baa743758f590dd768e9a376bb0b5b8e`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd8b93e4d9dcfdf009aceb88928aab4b1d5d2ba01a6749e9287ad1925d4cc72`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e55df648c2510c05b32e7421166be2a6b9f786ceb239419e8a421a9fe212c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605556095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ee29ac1fc0b94318e12e9e7a4d2fce5848339dae92fbd0659bb8bfad4133`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcaebee5a6a52dc8e7bd800d7d9927c19604e85c43dc3b60c8aaf9b5b823f6`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35c68471bc924b8ef806d0c9f01331f7f7677c46650b6dfa7d6c23c7d70bb62`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897dc78dfe0cd203f3c122ca3369c5723a18a8fccfe4087091a30459a94dc9c`  
		Last Modified: Sat, 16 Nov 2024 04:37:35 GMT  
		Size: 432.1 MB (432089569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab8b8847d096d63380d9d1428011278dea087edb347e467d1689f2e2406a4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0079edc9cb04d1f1c116433bbcdf22bf4d6718b580c0106f018f9ea6960724c4`

```dockerfile
```

-	Layers:
	-	`sha256:e0c1a0dc39455b0e801e995eee407611f5c8a9c1d5832f02d73401d051223e71`  
		Last Modified: Sat, 16 Nov 2024 04:37:23 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aebd3f28437d8b4264c3adf90ef3cc42d92402b575da43c3368b9a3fcc0878`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:6dab977d6cd6db4509dc379a227aa89cc0bbd93256d4cafbfb08cc43d5341e9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5b27268a3ff3295d3ead4c84eba8023d5eb29dc2981f0fea62db8e3ca9aea718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608121269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917edbc58a0d8126cd3fcfa66d84b43a6bcf12967d795291a67d5a6d93a4c233`
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
	-	`sha256:2e1a37447ddb0fdbdcaf9e583d14f96efc209fd3e964041998ef0f8443a55edf`  
		Last Modified: Sat, 16 Nov 2024 04:53:09 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7686ec4f5ba0e9697bd592326ea50d7a955b424ca0e697aa7f941f03c33dfb`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08c95a8b2fc276d3677ae5c817e606eb373b82b28be6fa62a904e8a8fb714d`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d50af54b276030bb4e8a8f74b1eba5ecba3b03c914f3a4d4b71d855334757d0`  
		Last Modified: Sat, 16 Nov 2024 04:53:12 GMT  
		Size: 432.1 MB (432119089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2fe3dd728c22ef80d4e6c1ede09c4e394eb375b65a54db6dfd8adeb798b1ac57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c67473f3c1848b1d86097593b5491a51c721d92122e40fddb66099ac4c0b96a`

```dockerfile
```

-	Layers:
	-	`sha256:4e9fda4a6f6cef1d5bbe90abdd6d7ac5baa743758f590dd768e9a376bb0b5b8e`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd8b93e4d9dcfdf009aceb88928aab4b1d5d2ba01a6749e9287ad1925d4cc72`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e55df648c2510c05b32e7421166be2a6b9f786ceb239419e8a421a9fe212c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605556095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ee29ac1fc0b94318e12e9e7a4d2fce5848339dae92fbd0659bb8bfad4133`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcaebee5a6a52dc8e7bd800d7d9927c19604e85c43dc3b60c8aaf9b5b823f6`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35c68471bc924b8ef806d0c9f01331f7f7677c46650b6dfa7d6c23c7d70bb62`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897dc78dfe0cd203f3c122ca3369c5723a18a8fccfe4087091a30459a94dc9c`  
		Last Modified: Sat, 16 Nov 2024 04:37:35 GMT  
		Size: 432.1 MB (432089569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab8b8847d096d63380d9d1428011278dea087edb347e467d1689f2e2406a4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0079edc9cb04d1f1c116433bbcdf22bf4d6718b580c0106f018f9ea6960724c4`

```dockerfile
```

-	Layers:
	-	`sha256:e0c1a0dc39455b0e801e995eee407611f5c8a9c1d5832f02d73401d051223e71`  
		Last Modified: Sat, 16 Nov 2024 04:37:23 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aebd3f28437d8b4264c3adf90ef3cc42d92402b575da43c3368b9a3fcc0878`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:8937a8a5059935eca9ba6075631174d00b110df58b877aee7865a247bc486c0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1f61f9a4c8374389288cd2cc5753fec284a3d71080648dcc7c657dfbf8d31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602992361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65f1f2310b1f9cb0310843343fade6acdef09234f36d4d6c1703921cd5ffc0f`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7cda7184de2dad5787aa22199072aa2ce5f3806a7393d91ee6819c6a2e72f`  
		Last Modified: Sat, 16 Nov 2024 02:12:53 GMT  
		Size: 133.8 MB (133849116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6c5b72b6452a0bdf04a0ac3995b02c08d9cba4e98ea10d2d96e1ae46b5c8e`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186fd32f31064cd20cfe94fd992bc97636bbfcff0d38aec5f20b3ddf2e7455c7`  
		Last Modified: Sat, 16 Nov 2024 02:12:57 GMT  
		Size: 429.2 MB (429194852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8248223725b6bdacd1c74e03983ca72b4ed8d2a5fe8c00fe9da2e75d6c2be7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3595cec09e93914c7f923aa756a235bd7bedfacbaf9f2e2281eae3e7cb3b72b4`

```dockerfile
```

-	Layers:
	-	`sha256:1603dfef5b32c1f3ff7e7d27f8df6398b9228c763b094010dd5b95d563e8b8c7`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 7.8 MB (7845287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0fc3d860033b379ff26a7bcb1047adc80b24707c58a5fd0b596d584d3ff9d0`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6e344a04225b9065cbb797a0b3d6e1083077c80de13d8b285b1cf96012f1a1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601154760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9858ac8e905ff7328c263884ffbf9d5bb979abcb8693688ea0fe157285374334`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76dd95a74c1cdb225698384ce1587b03f3a5f6f7275ded7db6a54fbacd9e00e`  
		Last Modified: Sat, 16 Nov 2024 02:48:12 GMT  
		Size: 429.2 MB (429194940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a1eb5f018a3eec4f4b812465511ff5d3feb8264785e6269f2d5cbd2d9ffc8523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7846334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff749f721c0048b393b0874e02e842cb965452a634261478d32d53ebb63f6ae`

```dockerfile
```

-	Layers:
	-	`sha256:6d198f202ed445d6babffd9d10ea2882e8d4b2653d34e8aecae755a63d9f0f8e`  
		Last Modified: Sat, 16 Nov 2024 02:48:05 GMT  
		Size: 7.8 MB (7824852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0ea6e302611c76ec6b665e1370d6fc44119489ff28c0f8dbf33574c8edde53`  
		Last Modified: Sat, 16 Nov 2024 02:48:04 GMT  
		Size: 21.5 KB (21482 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25-ubi9`

```console
$ docker pull neo4j@sha256:a139fcc8ee957cdf3186df77043bc97119dfa5bf0494d77fb91cab80612a7a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:41326e7635a2035a32f34285aae76a6e636cb982b8eb98557730f83188443afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313979634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2078d8e4f8ef123bb38a61258f7b5f015698c83217720c1885f5eb5076193`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d699ed19a7026bed8284e493e29672744eca2f26b5248dc1f209f26fd4b4e720`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 133.8 MB (133849264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0545597a6926348a3861fe4cebc1e5780454b640008aa6a37a56b7c133fd4`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2dc0545f98cb9e7ae40064e8245960ab37356d65e6b4e867e47f81b9f40a3a`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 140.2 MB (140181976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f350af5c1f6e522d3e266a704808496f6ef304e2f79506ba231f211a6732be04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd44ddf4be03a7e01f08e986e1395ac8d3811f87103a3214c76d77c9a18b07fd`

```dockerfile
```

-	Layers:
	-	`sha256:07068aba371864da822b89dbebba307519efd071797d7dc00e185a7df5bd83c3`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329a77b5a6a6b8d5c79710aabe6032712bd60124fa3b80246f62c1637e7fba24`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 22.5 KB (22546 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9eb57a6a15b5ea6cb79e1b602c05ac8f233b11d94b087fe2e58be28199501ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52c24e501b46cf8aa6f3f298a6148344f9cadc754635eaa9c961d0aa47ce17`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0baeef380d77fbef249485e41e036948fc46a16d1464c2a56469d4b115c44`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 140.2 MB (140182027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:23d5318cd77b4696006651f18d2e052319ed676ca8c1e176e2ae5d2d5bde4347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637b08ebfd76de82609504fe00226018254ea3956b62a99294099c41377f90f`

```dockerfile
```

-	Layers:
	-	`sha256:f022d71c37a0903b948c6df78781707920eca464cbc0688083a44ea78dfdf284`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f83c569248fc613179fdb4b014c51a840f5ed08b7709c13c5bc90c740230331`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-bullseye`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-community`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-community` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-community-bullseye`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-community-ubi9`

```console
$ docker pull neo4j@sha256:a139fcc8ee957cdf3186df77043bc97119dfa5bf0494d77fb91cab80612a7a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:41326e7635a2035a32f34285aae76a6e636cb982b8eb98557730f83188443afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313979634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2078d8e4f8ef123bb38a61258f7b5f015698c83217720c1885f5eb5076193`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d699ed19a7026bed8284e493e29672744eca2f26b5248dc1f209f26fd4b4e720`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 133.8 MB (133849264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0545597a6926348a3861fe4cebc1e5780454b640008aa6a37a56b7c133fd4`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2dc0545f98cb9e7ae40064e8245960ab37356d65e6b4e867e47f81b9f40a3a`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 140.2 MB (140181976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f350af5c1f6e522d3e266a704808496f6ef304e2f79506ba231f211a6732be04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd44ddf4be03a7e01f08e986e1395ac8d3811f87103a3214c76d77c9a18b07fd`

```dockerfile
```

-	Layers:
	-	`sha256:07068aba371864da822b89dbebba307519efd071797d7dc00e185a7df5bd83c3`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329a77b5a6a6b8d5c79710aabe6032712bd60124fa3b80246f62c1637e7fba24`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 22.5 KB (22546 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9eb57a6a15b5ea6cb79e1b602c05ac8f233b11d94b087fe2e58be28199501ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52c24e501b46cf8aa6f3f298a6148344f9cadc754635eaa9c961d0aa47ce17`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0baeef380d77fbef249485e41e036948fc46a16d1464c2a56469d4b115c44`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 140.2 MB (140182027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:23d5318cd77b4696006651f18d2e052319ed676ca8c1e176e2ae5d2d5bde4347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637b08ebfd76de82609504fe00226018254ea3956b62a99294099c41377f90f`

```dockerfile
```

-	Layers:
	-	`sha256:f022d71c37a0903b948c6df78781707920eca464cbc0688083a44ea78dfdf284`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f83c569248fc613179fdb4b014c51a840f5ed08b7709c13c5bc90c740230331`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-enterprise`

```console
$ docker pull neo4j@sha256:6dab977d6cd6db4509dc379a227aa89cc0bbd93256d4cafbfb08cc43d5341e9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5b27268a3ff3295d3ead4c84eba8023d5eb29dc2981f0fea62db8e3ca9aea718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608121269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917edbc58a0d8126cd3fcfa66d84b43a6bcf12967d795291a67d5a6d93a4c233`
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
	-	`sha256:2e1a37447ddb0fdbdcaf9e583d14f96efc209fd3e964041998ef0f8443a55edf`  
		Last Modified: Sat, 16 Nov 2024 04:53:09 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7686ec4f5ba0e9697bd592326ea50d7a955b424ca0e697aa7f941f03c33dfb`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08c95a8b2fc276d3677ae5c817e606eb373b82b28be6fa62a904e8a8fb714d`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d50af54b276030bb4e8a8f74b1eba5ecba3b03c914f3a4d4b71d855334757d0`  
		Last Modified: Sat, 16 Nov 2024 04:53:12 GMT  
		Size: 432.1 MB (432119089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2fe3dd728c22ef80d4e6c1ede09c4e394eb375b65a54db6dfd8adeb798b1ac57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c67473f3c1848b1d86097593b5491a51c721d92122e40fddb66099ac4c0b96a`

```dockerfile
```

-	Layers:
	-	`sha256:4e9fda4a6f6cef1d5bbe90abdd6d7ac5baa743758f590dd768e9a376bb0b5b8e`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd8b93e4d9dcfdf009aceb88928aab4b1d5d2ba01a6749e9287ad1925d4cc72`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e55df648c2510c05b32e7421166be2a6b9f786ceb239419e8a421a9fe212c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605556095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ee29ac1fc0b94318e12e9e7a4d2fce5848339dae92fbd0659bb8bfad4133`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcaebee5a6a52dc8e7bd800d7d9927c19604e85c43dc3b60c8aaf9b5b823f6`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35c68471bc924b8ef806d0c9f01331f7f7677c46650b6dfa7d6c23c7d70bb62`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897dc78dfe0cd203f3c122ca3369c5723a18a8fccfe4087091a30459a94dc9c`  
		Last Modified: Sat, 16 Nov 2024 04:37:35 GMT  
		Size: 432.1 MB (432089569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab8b8847d096d63380d9d1428011278dea087edb347e467d1689f2e2406a4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0079edc9cb04d1f1c116433bbcdf22bf4d6718b580c0106f018f9ea6960724c4`

```dockerfile
```

-	Layers:
	-	`sha256:e0c1a0dc39455b0e801e995eee407611f5c8a9c1d5832f02d73401d051223e71`  
		Last Modified: Sat, 16 Nov 2024 04:37:23 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aebd3f28437d8b4264c3adf90ef3cc42d92402b575da43c3368b9a3fcc0878`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:6dab977d6cd6db4509dc379a227aa89cc0bbd93256d4cafbfb08cc43d5341e9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5b27268a3ff3295d3ead4c84eba8023d5eb29dc2981f0fea62db8e3ca9aea718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608121269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917edbc58a0d8126cd3fcfa66d84b43a6bcf12967d795291a67d5a6d93a4c233`
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
	-	`sha256:2e1a37447ddb0fdbdcaf9e583d14f96efc209fd3e964041998ef0f8443a55edf`  
		Last Modified: Sat, 16 Nov 2024 04:53:09 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7686ec4f5ba0e9697bd592326ea50d7a955b424ca0e697aa7f941f03c33dfb`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08c95a8b2fc276d3677ae5c817e606eb373b82b28be6fa62a904e8a8fb714d`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d50af54b276030bb4e8a8f74b1eba5ecba3b03c914f3a4d4b71d855334757d0`  
		Last Modified: Sat, 16 Nov 2024 04:53:12 GMT  
		Size: 432.1 MB (432119089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2fe3dd728c22ef80d4e6c1ede09c4e394eb375b65a54db6dfd8adeb798b1ac57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c67473f3c1848b1d86097593b5491a51c721d92122e40fddb66099ac4c0b96a`

```dockerfile
```

-	Layers:
	-	`sha256:4e9fda4a6f6cef1d5bbe90abdd6d7ac5baa743758f590dd768e9a376bb0b5b8e`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd8b93e4d9dcfdf009aceb88928aab4b1d5d2ba01a6749e9287ad1925d4cc72`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e55df648c2510c05b32e7421166be2a6b9f786ceb239419e8a421a9fe212c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605556095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ee29ac1fc0b94318e12e9e7a4d2fce5848339dae92fbd0659bb8bfad4133`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcaebee5a6a52dc8e7bd800d7d9927c19604e85c43dc3b60c8aaf9b5b823f6`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35c68471bc924b8ef806d0c9f01331f7f7677c46650b6dfa7d6c23c7d70bb62`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897dc78dfe0cd203f3c122ca3369c5723a18a8fccfe4087091a30459a94dc9c`  
		Last Modified: Sat, 16 Nov 2024 04:37:35 GMT  
		Size: 432.1 MB (432089569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab8b8847d096d63380d9d1428011278dea087edb347e467d1689f2e2406a4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0079edc9cb04d1f1c116433bbcdf22bf4d6718b580c0106f018f9ea6960724c4`

```dockerfile
```

-	Layers:
	-	`sha256:e0c1a0dc39455b0e801e995eee407611f5c8a9c1d5832f02d73401d051223e71`  
		Last Modified: Sat, 16 Nov 2024 04:37:23 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aebd3f28437d8b4264c3adf90ef3cc42d92402b575da43c3368b9a3fcc0878`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:8937a8a5059935eca9ba6075631174d00b110df58b877aee7865a247bc486c0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1f61f9a4c8374389288cd2cc5753fec284a3d71080648dcc7c657dfbf8d31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602992361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65f1f2310b1f9cb0310843343fade6acdef09234f36d4d6c1703921cd5ffc0f`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7cda7184de2dad5787aa22199072aa2ce5f3806a7393d91ee6819c6a2e72f`  
		Last Modified: Sat, 16 Nov 2024 02:12:53 GMT  
		Size: 133.8 MB (133849116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6c5b72b6452a0bdf04a0ac3995b02c08d9cba4e98ea10d2d96e1ae46b5c8e`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186fd32f31064cd20cfe94fd992bc97636bbfcff0d38aec5f20b3ddf2e7455c7`  
		Last Modified: Sat, 16 Nov 2024 02:12:57 GMT  
		Size: 429.2 MB (429194852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8248223725b6bdacd1c74e03983ca72b4ed8d2a5fe8c00fe9da2e75d6c2be7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3595cec09e93914c7f923aa756a235bd7bedfacbaf9f2e2281eae3e7cb3b72b4`

```dockerfile
```

-	Layers:
	-	`sha256:1603dfef5b32c1f3ff7e7d27f8df6398b9228c763b094010dd5b95d563e8b8c7`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 7.8 MB (7845287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0fc3d860033b379ff26a7bcb1047adc80b24707c58a5fd0b596d584d3ff9d0`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6e344a04225b9065cbb797a0b3d6e1083077c80de13d8b285b1cf96012f1a1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601154760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9858ac8e905ff7328c263884ffbf9d5bb979abcb8693688ea0fe157285374334`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76dd95a74c1cdb225698384ce1587b03f3a5f6f7275ded7db6a54fbacd9e00e`  
		Last Modified: Sat, 16 Nov 2024 02:48:12 GMT  
		Size: 429.2 MB (429194940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a1eb5f018a3eec4f4b812465511ff5d3feb8264785e6269f2d5cbd2d9ffc8523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7846334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff749f721c0048b393b0874e02e842cb965452a634261478d32d53ebb63f6ae`

```dockerfile
```

-	Layers:
	-	`sha256:6d198f202ed445d6babffd9d10ea2882e8d4b2653d34e8aecae755a63d9f0f8e`  
		Last Modified: Sat, 16 Nov 2024 02:48:05 GMT  
		Size: 7.8 MB (7824852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0ea6e302611c76ec6b665e1370d6fc44119489ff28c0f8dbf33574c8edde53`  
		Last Modified: Sat, 16 Nov 2024 02:48:04 GMT  
		Size: 21.5 KB (21482 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.25.1-ubi9`

```console
$ docker pull neo4j@sha256:a139fcc8ee957cdf3186df77043bc97119dfa5bf0494d77fb91cab80612a7a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.25.1-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:41326e7635a2035a32f34285aae76a6e636cb982b8eb98557730f83188443afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313979634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2078d8e4f8ef123bb38a61258f7b5f015698c83217720c1885f5eb5076193`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d699ed19a7026bed8284e493e29672744eca2f26b5248dc1f209f26fd4b4e720`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 133.8 MB (133849264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0545597a6926348a3861fe4cebc1e5780454b640008aa6a37a56b7c133fd4`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2dc0545f98cb9e7ae40064e8245960ab37356d65e6b4e867e47f81b9f40a3a`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 140.2 MB (140181976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f350af5c1f6e522d3e266a704808496f6ef304e2f79506ba231f211a6732be04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd44ddf4be03a7e01f08e986e1395ac8d3811f87103a3214c76d77c9a18b07fd`

```dockerfile
```

-	Layers:
	-	`sha256:07068aba371864da822b89dbebba307519efd071797d7dc00e185a7df5bd83c3`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329a77b5a6a6b8d5c79710aabe6032712bd60124fa3b80246f62c1637e7fba24`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 22.5 KB (22546 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.25.1-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9eb57a6a15b5ea6cb79e1b602c05ac8f233b11d94b087fe2e58be28199501ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52c24e501b46cf8aa6f3f298a6148344f9cadc754635eaa9c961d0aa47ce17`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0baeef380d77fbef249485e41e036948fc46a16d1464c2a56469d4b115c44`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 140.2 MB (140182027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.25.1-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:23d5318cd77b4696006651f18d2e052319ed676ca8c1e176e2ae5d2d5bde4347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637b08ebfd76de82609504fe00226018254ea3956b62a99294099c41377f90f`

```dockerfile
```

-	Layers:
	-	`sha256:f022d71c37a0903b948c6df78781707920eca464cbc0688083a44ea78dfdf284`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f83c569248fc613179fdb4b014c51a840f5ed08b7709c13c5bc90c740230331`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:a139fcc8ee957cdf3186df77043bc97119dfa5bf0494d77fb91cab80612a7a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:41326e7635a2035a32f34285aae76a6e636cb982b8eb98557730f83188443afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313979634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2078d8e4f8ef123bb38a61258f7b5f015698c83217720c1885f5eb5076193`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d699ed19a7026bed8284e493e29672744eca2f26b5248dc1f209f26fd4b4e720`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 133.8 MB (133849264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0545597a6926348a3861fe4cebc1e5780454b640008aa6a37a56b7c133fd4`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2dc0545f98cb9e7ae40064e8245960ab37356d65e6b4e867e47f81b9f40a3a`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 140.2 MB (140181976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f350af5c1f6e522d3e266a704808496f6ef304e2f79506ba231f211a6732be04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd44ddf4be03a7e01f08e986e1395ac8d3811f87103a3214c76d77c9a18b07fd`

```dockerfile
```

-	Layers:
	-	`sha256:07068aba371864da822b89dbebba307519efd071797d7dc00e185a7df5bd83c3`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329a77b5a6a6b8d5c79710aabe6032712bd60124fa3b80246f62c1637e7fba24`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 22.5 KB (22546 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9eb57a6a15b5ea6cb79e1b602c05ac8f233b11d94b087fe2e58be28199501ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52c24e501b46cf8aa6f3f298a6148344f9cadc754635eaa9c961d0aa47ce17`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0baeef380d77fbef249485e41e036948fc46a16d1464c2a56469d4b115c44`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 140.2 MB (140182027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:23d5318cd77b4696006651f18d2e052319ed676ca8c1e176e2ae5d2d5bde4347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637b08ebfd76de82609504fe00226018254ea3956b62a99294099c41377f90f`

```dockerfile
```

-	Layers:
	-	`sha256:f022d71c37a0903b948c6df78781707920eca464cbc0688083a44ea78dfdf284`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f83c569248fc613179fdb4b014c51a840f5ed08b7709c13c5bc90c740230331`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:6dab977d6cd6db4509dc379a227aa89cc0bbd93256d4cafbfb08cc43d5341e9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:5b27268a3ff3295d3ead4c84eba8023d5eb29dc2981f0fea62db8e3ca9aea718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608121269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917edbc58a0d8126cd3fcfa66d84b43a6bcf12967d795291a67d5a6d93a4c233`
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
	-	`sha256:2e1a37447ddb0fdbdcaf9e583d14f96efc209fd3e964041998ef0f8443a55edf`  
		Last Modified: Sat, 16 Nov 2024 04:53:09 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7686ec4f5ba0e9697bd592326ea50d7a955b424ca0e697aa7f941f03c33dfb`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08c95a8b2fc276d3677ae5c817e606eb373b82b28be6fa62a904e8a8fb714d`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d50af54b276030bb4e8a8f74b1eba5ecba3b03c914f3a4d4b71d855334757d0`  
		Last Modified: Sat, 16 Nov 2024 04:53:12 GMT  
		Size: 432.1 MB (432119089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2fe3dd728c22ef80d4e6c1ede09c4e394eb375b65a54db6dfd8adeb798b1ac57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c67473f3c1848b1d86097593b5491a51c721d92122e40fddb66099ac4c0b96a`

```dockerfile
```

-	Layers:
	-	`sha256:4e9fda4a6f6cef1d5bbe90abdd6d7ac5baa743758f590dd768e9a376bb0b5b8e`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd8b93e4d9dcfdf009aceb88928aab4b1d5d2ba01a6749e9287ad1925d4cc72`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e55df648c2510c05b32e7421166be2a6b9f786ceb239419e8a421a9fe212c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605556095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ee29ac1fc0b94318e12e9e7a4d2fce5848339dae92fbd0659bb8bfad4133`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcaebee5a6a52dc8e7bd800d7d9927c19604e85c43dc3b60c8aaf9b5b823f6`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35c68471bc924b8ef806d0c9f01331f7f7677c46650b6dfa7d6c23c7d70bb62`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897dc78dfe0cd203f3c122ca3369c5723a18a8fccfe4087091a30459a94dc9c`  
		Last Modified: Sat, 16 Nov 2024 04:37:35 GMT  
		Size: 432.1 MB (432089569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab8b8847d096d63380d9d1428011278dea087edb347e467d1689f2e2406a4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0079edc9cb04d1f1c116433bbcdf22bf4d6718b580c0106f018f9ea6960724c4`

```dockerfile
```

-	Layers:
	-	`sha256:e0c1a0dc39455b0e801e995eee407611f5c8a9c1d5832f02d73401d051223e71`  
		Last Modified: Sat, 16 Nov 2024 04:37:23 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aebd3f28437d8b4264c3adf90ef3cc42d92402b575da43c3368b9a3fcc0878`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:6dab977d6cd6db4509dc379a227aa89cc0bbd93256d4cafbfb08cc43d5341e9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:5b27268a3ff3295d3ead4c84eba8023d5eb29dc2981f0fea62db8e3ca9aea718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.1 MB (608121269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917edbc58a0d8126cd3fcfa66d84b43a6bcf12967d795291a67d5a6d93a4c233`
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
	-	`sha256:2e1a37447ddb0fdbdcaf9e583d14f96efc209fd3e964041998ef0f8443a55edf`  
		Last Modified: Sat, 16 Nov 2024 04:53:09 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7686ec4f5ba0e9697bd592326ea50d7a955b424ca0e697aa7f941f03c33dfb`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c08c95a8b2fc276d3677ae5c817e606eb373b82b28be6fa62a904e8a8fb714d`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d50af54b276030bb4e8a8f74b1eba5ecba3b03c914f3a4d4b71d855334757d0`  
		Last Modified: Sat, 16 Nov 2024 04:53:12 GMT  
		Size: 432.1 MB (432119089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2fe3dd728c22ef80d4e6c1ede09c4e394eb375b65a54db6dfd8adeb798b1ac57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c67473f3c1848b1d86097593b5491a51c721d92122e40fddb66099ac4c0b96a`

```dockerfile
```

-	Layers:
	-	`sha256:4e9fda4a6f6cef1d5bbe90abdd6d7ac5baa743758f590dd768e9a376bb0b5b8e`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 3.6 MB (3561844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd8b93e4d9dcfdf009aceb88928aab4b1d5d2ba01a6749e9287ad1925d4cc72`  
		Last Modified: Sat, 16 Nov 2024 04:53:07 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1e55df648c2510c05b32e7421166be2a6b9f786ceb239419e8a421a9fe212c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.6 MB (605556095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f995ee29ac1fc0b94318e12e9e7a4d2fce5848339dae92fbd0659bb8bfad4133`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcaebee5a6a52dc8e7bd800d7d9927c19604e85c43dc3b60c8aaf9b5b823f6`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 3.9 KB (3879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35c68471bc924b8ef806d0c9f01331f7f7677c46650b6dfa7d6c23c7d70bb62`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897dc78dfe0cd203f3c122ca3369c5723a18a8fccfe4087091a30459a94dc9c`  
		Last Modified: Sat, 16 Nov 2024 04:37:35 GMT  
		Size: 432.1 MB (432089569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:ab8b8847d096d63380d9d1428011278dea087edb347e467d1689f2e2406a4130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0079edc9cb04d1f1c116433bbcdf22bf4d6718b580c0106f018f9ea6960724c4`

```dockerfile
```

-	Layers:
	-	`sha256:e0c1a0dc39455b0e801e995eee407611f5c8a9c1d5832f02d73401d051223e71`  
		Last Modified: Sat, 16 Nov 2024 04:37:23 GMT  
		Size: 3.6 MB (3561536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53aebd3f28437d8b4264c3adf90ef3cc42d92402b575da43c3368b9a3fcc0878`  
		Last Modified: Sat, 16 Nov 2024 04:37:22 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:8937a8a5059935eca9ba6075631174d00b110df58b877aee7865a247bc486c0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1f61f9a4c8374389288cd2cc5753fec284a3d71080648dcc7c657dfbf8d31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.0 MB (602992361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65f1f2310b1f9cb0310843343fade6acdef09234f36d4d6c1703921cd5ffc0f`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7cda7184de2dad5787aa22199072aa2ce5f3806a7393d91ee6819c6a2e72f`  
		Last Modified: Sat, 16 Nov 2024 02:12:53 GMT  
		Size: 133.8 MB (133849116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6c5b72b6452a0bdf04a0ac3995b02c08d9cba4e98ea10d2d96e1ae46b5c8e`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186fd32f31064cd20cfe94fd992bc97636bbfcff0d38aec5f20b3ddf2e7455c7`  
		Last Modified: Sat, 16 Nov 2024 02:12:57 GMT  
		Size: 429.2 MB (429194852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8248223725b6bdacd1c74e03983ca72b4ed8d2a5fe8c00fe9da2e75d6c2be7fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3595cec09e93914c7f923aa756a235bd7bedfacbaf9f2e2281eae3e7cb3b72b4`

```dockerfile
```

-	Layers:
	-	`sha256:1603dfef5b32c1f3ff7e7d27f8df6398b9228c763b094010dd5b95d563e8b8c7`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 7.8 MB (7845287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0fc3d860033b379ff26a7bcb1047adc80b24707c58a5fd0b596d584d3ff9d0`  
		Last Modified: Sat, 16 Nov 2024 02:12:52 GMT  
		Size: 21.4 KB (21369 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6e344a04225b9065cbb797a0b3d6e1083077c80de13d8b285b1cf96012f1a1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 MB (601154760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9858ac8e905ff7328c263884ffbf9d5bb979abcb8693688ea0fe157285374334`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76dd95a74c1cdb225698384ce1587b03f3a5f6f7275ded7db6a54fbacd9e00e`  
		Last Modified: Sat, 16 Nov 2024 02:48:12 GMT  
		Size: 429.2 MB (429194940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a1eb5f018a3eec4f4b812465511ff5d3feb8264785e6269f2d5cbd2d9ffc8523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7846334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff749f721c0048b393b0874e02e842cb965452a634261478d32d53ebb63f6ae`

```dockerfile
```

-	Layers:
	-	`sha256:6d198f202ed445d6babffd9d10ea2882e8d4b2653d34e8aecae755a63d9f0f8e`  
		Last Modified: Sat, 16 Nov 2024 02:48:05 GMT  
		Size: 7.8 MB (7824852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0ea6e302611c76ec6b665e1370d6fc44119489ff28c0f8dbf33574c8edde53`  
		Last Modified: Sat, 16 Nov 2024 02:48:04 GMT  
		Size: 21.5 KB (21482 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:499dfad4f2c49748943e6be36d7421a331943e54d1e74ba2649a4d6c929cdccb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:20304018969a57c422a91bdf98bda3970bce9984a930e486a9fc04b75bb99a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319112855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324591ef442691117d2d97df2e49b8fa07b5938cc228530d3ec99acfb0aa2bf8`
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
	-	`sha256:8f333c5af1809ded841c08a0321b71ed6b5292a589baa48af9fd3ee2d8291565`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 144.5 MB (144536720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232e86997e5e7c13a0cb47c5a5cb0bf4f095c697bae3ed721692885dcc6aab3b`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa66b4573de17d9a4a5431135436e53d188cf4ab37c39253d6706e0866b1a6`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7c435d9ee9775b5785c238daca03ace667a7c932e9a4d2927e7c883bc11d`  
		Last Modified: Sat, 16 Nov 2024 04:51:44 GMT  
		Size: 143.1 MB (143110677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:9a94a1751dee39f153fedcb5496830cea25e35ffb649864f259aa82990f880ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6404fe14639fb376536fb204e6585d09346323d0afb4ba833cfac4f0606c3c10`

```dockerfile
```

-	Layers:
	-	`sha256:a8d5940849d28d197878a77a4504f4db487e2066b383905c8ccf0d24fe73fc90`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 3.2 MB (3240546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa53cd663f0853a576c498ec974e2b730d475074b185af1156df1bbc33971414`  
		Last Modified: Sat, 16 Nov 2024 04:51:42 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c372b2ed25330af61b2cd315cfdcdde43f083b7bcd2d4fb1442c35187c3870cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316546732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaed992472b341e3b07c71da5f1a19817069ac7db6b33754a348fddbeb156a5`
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
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241721ee2b92afa899603e40bbf36026a64d672f522d70b386758fd406d01c0f`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb0f9178ba15bbca50e9a1e12bad99a6ae74d48e8906bd8e2005755dd3b2b5e`  
		Last Modified: Sat, 16 Nov 2024 04:33:08 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bed02c7bcf1ee2c0fe649d0c09508058fae014105c59ed123ef8cdb7280653d`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.1 MB (143080218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:bedb7372c6550b47b4047573a156569f2719cfbe2e970ce296a47b34a923c3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3264376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ade4ef21bd8488582ed2ba3e044f6d94d0fcaef8a33ca73af7bb5c8226a81`

```dockerfile
```

-	Layers:
	-	`sha256:1b460290dac0ef8b15c44248f690bcd7417d2fe6c8461d6542ef49a8f11d04d3`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 3.2 MB (3240334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aafcd74ef1c990664c2e928492524511c2cb94b327549b8781537959507af4e`  
		Last Modified: Sat, 16 Nov 2024 04:33:09 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:a139fcc8ee957cdf3186df77043bc97119dfa5bf0494d77fb91cab80612a7a9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:41326e7635a2035a32f34285aae76a6e636cb982b8eb98557730f83188443afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (313979634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f2078d8e4f8ef123bb38a61258f7b5f015698c83217720c1885f5eb5076193`
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
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d699ed19a7026bed8284e493e29672744eca2f26b5248dc1f209f26fd4b4e720`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 133.8 MB (133849264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0545597a6926348a3861fe4cebc1e5780454b640008aa6a37a56b7c133fd4`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2dc0545f98cb9e7ae40064e8245960ab37356d65e6b4e867e47f81b9f40a3a`  
		Last Modified: Sat, 16 Nov 2024 02:11:47 GMT  
		Size: 140.2 MB (140181976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:f350af5c1f6e522d3e266a704808496f6ef304e2f79506ba231f211a6732be04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7545341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd44ddf4be03a7e01f08e986e1395ac8d3811f87103a3214c76d77c9a18b07fd`

```dockerfile
```

-	Layers:
	-	`sha256:07068aba371864da822b89dbebba307519efd071797d7dc00e185a7df5bd83c3`  
		Last Modified: Sat, 16 Nov 2024 02:11:45 GMT  
		Size: 7.5 MB (7522795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329a77b5a6a6b8d5c79710aabe6032712bd60124fa3b80246f62c1637e7fba24`  
		Last Modified: Sat, 16 Nov 2024 02:11:44 GMT  
		Size: 22.5 KB (22546 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9eb57a6a15b5ea6cb79e1b602c05ac8f233b11d94b087fe2e58be28199501ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312141847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f52c24e501b46cf8aa6f3f298a6148344f9cadc754635eaa9c961d0aa47ce17`
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
COPY dir:7fe66f5f8373d1d6b22336da5ccea9872ce92f8e71c6661e555027e35af9fc8d in / 
# Wed, 30 Oct 2024 15:39:25 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 30 Oct 2024 15:39:25 GMT
CMD ["/bin/bash"]
# Wed, 30 Oct 2024 15:39:25 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Wed, 30 Oct 2024 15:39:25 GMT
LABEL "build-date"="2024-11-14T14:10:44" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
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
	-	`sha256:06efaada693c8039399aa295b10cf1156c7c64eb4814487ce00c94f0f3312913`  
		Last Modified: Thu, 14 Nov 2024 22:57:54 GMT  
		Size: 38.0 MB (38048586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61b2e9481ca4da337dc5e273b5e6c1e9a053035fb040222bf843ef269dc0699`  
		Last Modified: Thu, 14 Nov 2024 22:57:48 GMT  
		Size: 63.6 KB (63602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e76690689eaa8435b1c15cd6d6d9ae4ae66c91ab047385c41cc2997e3711c`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 133.8 MB (133837576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510bc11605b75d02754862e9eed408819c9dfdca07e28df24946524f23542a88`  
		Last Modified: Sat, 16 Nov 2024 02:44:06 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd0baeef380d77fbef249485e41e036948fc46a16d1464c2a56469d4b115c44`  
		Last Modified: Sat, 16 Nov 2024 02:44:11 GMT  
		Size: 140.2 MB (140182027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:23d5318cd77b4696006651f18d2e052319ed676ca8c1e176e2ae5d2d5bde4347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d637b08ebfd76de82609504fe00226018254ea3956b62a99294099c41377f90f`

```dockerfile
```

-	Layers:
	-	`sha256:f022d71c37a0903b948c6df78781707920eca464cbc0688083a44ea78dfdf284`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 7.5 MB (7502408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f83c569248fc613179fdb4b014c51a840f5ed08b7709c13c5bc90c740230331`  
		Last Modified: Sat, 16 Nov 2024 02:44:07 GMT  
		Size: 22.7 KB (22708 bytes)  
		MIME: application/vnd.in-toto+json
