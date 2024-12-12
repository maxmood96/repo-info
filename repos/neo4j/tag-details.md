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
-	[`neo4j:5.26`](#neo4j526)
-	[`neo4j:5.26-bullseye`](#neo4j526-bullseye)
-	[`neo4j:5.26-community`](#neo4j526-community)
-	[`neo4j:5.26-community-bullseye`](#neo4j526-community-bullseye)
-	[`neo4j:5.26-community-ubi9`](#neo4j526-community-ubi9)
-	[`neo4j:5.26-enterprise`](#neo4j526-enterprise)
-	[`neo4j:5.26-enterprise-bullseye`](#neo4j526-enterprise-bullseye)
-	[`neo4j:5.26-enterprise-ubi9`](#neo4j526-enterprise-ubi9)
-	[`neo4j:5.26-ubi9`](#neo4j526-ubi9)
-	[`neo4j:5.26.0`](#neo4j5260)
-	[`neo4j:5.26.0-bullseye`](#neo4j5260-bullseye)
-	[`neo4j:5.26.0-community`](#neo4j5260-community)
-	[`neo4j:5.26.0-community-bullseye`](#neo4j5260-community-bullseye)
-	[`neo4j:5.26.0-community-ubi9`](#neo4j5260-community-ubi9)
-	[`neo4j:5.26.0-enterprise`](#neo4j5260-enterprise)
-	[`neo4j:5.26.0-enterprise-bullseye`](#neo4j5260-enterprise-bullseye)
-	[`neo4j:5.26.0-enterprise-ubi9`](#neo4j5260-enterprise-ubi9)
-	[`neo4j:5.26.0-ubi9`](#neo4j5260-ubi9)
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
$ docker pull neo4j@sha256:a646bfed7ad1c6d2dcd8026d407473834f849b62da829b61e626a388bfdcc840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:a00d4c310fda3dbb130bd1dabe9d0afba2154c466005f17a223a5509e65f9f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305100509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6205ba8801801f2d337d1d633962e8412c4e035f6327b8dec758943a39a52e6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0ed842590ef87186c2fa6843c0233756b1a25b631eb5d740bddf85896fbcce04 NEO4J_TARBALL=neo4j-community-4.4.39-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522cdc3b7b691c6fce64d54f4f6a91d7f90544400a02ce25ae100e50c6f0ca28`  
		Last Modified: Tue, 03 Dec 2024 03:25:37 GMT  
		Size: 145.6 MB (145601457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c885dbae8fd19d00239ba8c79aab627dee54283b393933eea064f69cc89b0fd1`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409cc90b263f3f4045961498fe8484531b536946954ef0bd5800d535d10b1375`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 10.0 KB (9987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2cd0020471319c7045cc2916ae55602c22eb3fbc16bcc11cb99f92680c3265`  
		Last Modified: Tue, 03 Dec 2024 03:25:37 GMT  
		Size: 129.2 MB (129232556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:b0e0bf07da593dc89d7c0703533a1ff01215d87d36aa523c9ed13fd065a94c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3220140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e270c406e74bd1611186f133d5e18b8dd39433a6251d6a8188d1645c4f0c0db`

```dockerfile
```

-	Layers:
	-	`sha256:5ccddce5e1530673c9a6dec3be0088aab88534f9caff8ac3e128f1de855f91f0`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 3.2 MB (3200184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f886c12fdf7eadc9c1ba1678b0e6d9393d453ad513b30ba597056c1f68f088`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5eeaa11e1aa881ce1177904b043712de497515e032d77d4c167b01cb1e7c705b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300346623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747bcb46ef9a70a3d23416e4c79285b9655ea869ad7af557a3d667eb961c32d4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0ed842590ef87186c2fa6843c0233756b1a25b631eb5d740bddf85896fbcce04 NEO4J_TARBALL=neo4j-community-4.4.39-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5dff04b2bf13f7daa9b187569e3dac438596fb37c4f93fe7d65747f4fe8d7b`  
		Last Modified: Tue, 03 Dec 2024 14:04:51 GMT  
		Size: 142.4 MB (142389020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afddef27eca95f626d1ee7bdec235fec37a676b7cf6fd8b0ee711add1b464c7c`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261dfe618e6434ff87dc085a789d0bfd2fdd236d0f9173e59424cb16309f23dc`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b265d1704678ccd48e3b09cd3dcfbaf6332c44dc8e6a59becd20100ccb11d`  
		Last Modified: Tue, 03 Dec 2024 14:04:52 GMT  
		Size: 129.2 MB (129198794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:536570858fd79700f7f6c2fe4d1b7c9af0adafc6791709ded48bd4a034f8b7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3220548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920defb81834493e445a8c3afb24f0444e92bf8e132dbac8c9862fdff553636b`

```dockerfile
```

-	Layers:
	-	`sha256:aa9ce0dd3b208a33d7cf9522dca92ca116fc59cc9a7d2815ea1815a2fc296bf8`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 3.2 MB (3200447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594c11ca7bc0996b1c2f548790b620e737cf860aeb094359c0b7349c7c5b3774`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 20.1 KB (20101 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:a646bfed7ad1c6d2dcd8026d407473834f849b62da829b61e626a388bfdcc840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a00d4c310fda3dbb130bd1dabe9d0afba2154c466005f17a223a5509e65f9f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305100509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6205ba8801801f2d337d1d633962e8412c4e035f6327b8dec758943a39a52e6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0ed842590ef87186c2fa6843c0233756b1a25b631eb5d740bddf85896fbcce04 NEO4J_TARBALL=neo4j-community-4.4.39-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522cdc3b7b691c6fce64d54f4f6a91d7f90544400a02ce25ae100e50c6f0ca28`  
		Last Modified: Tue, 03 Dec 2024 03:25:37 GMT  
		Size: 145.6 MB (145601457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c885dbae8fd19d00239ba8c79aab627dee54283b393933eea064f69cc89b0fd1`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409cc90b263f3f4045961498fe8484531b536946954ef0bd5800d535d10b1375`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 10.0 KB (9987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2cd0020471319c7045cc2916ae55602c22eb3fbc16bcc11cb99f92680c3265`  
		Last Modified: Tue, 03 Dec 2024 03:25:37 GMT  
		Size: 129.2 MB (129232556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b0e0bf07da593dc89d7c0703533a1ff01215d87d36aa523c9ed13fd065a94c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3220140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e270c406e74bd1611186f133d5e18b8dd39433a6251d6a8188d1645c4f0c0db`

```dockerfile
```

-	Layers:
	-	`sha256:5ccddce5e1530673c9a6dec3be0088aab88534f9caff8ac3e128f1de855f91f0`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 3.2 MB (3200184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f886c12fdf7eadc9c1ba1678b0e6d9393d453ad513b30ba597056c1f68f088`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5eeaa11e1aa881ce1177904b043712de497515e032d77d4c167b01cb1e7c705b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300346623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747bcb46ef9a70a3d23416e4c79285b9655ea869ad7af557a3d667eb961c32d4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0ed842590ef87186c2fa6843c0233756b1a25b631eb5d740bddf85896fbcce04 NEO4J_TARBALL=neo4j-community-4.4.39-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5dff04b2bf13f7daa9b187569e3dac438596fb37c4f93fe7d65747f4fe8d7b`  
		Last Modified: Tue, 03 Dec 2024 14:04:51 GMT  
		Size: 142.4 MB (142389020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afddef27eca95f626d1ee7bdec235fec37a676b7cf6fd8b0ee711add1b464c7c`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261dfe618e6434ff87dc085a789d0bfd2fdd236d0f9173e59424cb16309f23dc`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b265d1704678ccd48e3b09cd3dcfbaf6332c44dc8e6a59becd20100ccb11d`  
		Last Modified: Tue, 03 Dec 2024 14:04:52 GMT  
		Size: 129.2 MB (129198794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:536570858fd79700f7f6c2fe4d1b7c9af0adafc6791709ded48bd4a034f8b7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3220548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920defb81834493e445a8c3afb24f0444e92bf8e132dbac8c9862fdff553636b`

```dockerfile
```

-	Layers:
	-	`sha256:aa9ce0dd3b208a33d7cf9522dca92ca116fc59cc9a7d2815ea1815a2fc296bf8`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 3.2 MB (3200447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594c11ca7bc0996b1c2f548790b620e737cf860aeb094359c0b7349c7c5b3774`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 20.1 KB (20101 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:a161b88a2b184c99ada158cbe8855445af3d353344f1c4b53e186fdee03aba60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ba1428fee503ff1e9bf19cb30058a97785695030c59d088d102c26f9aedd06bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.8 MB (409832468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ec500f7e987cdb804cb0ea0b065a88bf416cb5e0c301a0cdd52d161d6b9ffe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9f1e68c0dbea7ec6fbf1baa4a32510588d675f4692d4ae9d0a7e8d820cd9b308 NEO4J_TARBALL=neo4j-enterprise-4.4.39-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0503670579e43950881346fbbf9391d490262def6b985426e02e8996af7941e4`  
		Last Modified: Tue, 03 Dec 2024 03:25:51 GMT  
		Size: 145.6 MB (145601451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d3d88084864472e0a664af1bc5c367337919ba10ce49a307d24e4548de0bb8`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ed4ac710ca84242e376f4bfccaab03a29f5665d3a1218e0c98ca47f1ed3991`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 10.0 KB (9986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193734ef44ba5f18d1587fe2605128ca7aee5f0931be51fc23c9c1bef1ea3b5d`  
		Last Modified: Tue, 03 Dec 2024 03:25:51 GMT  
		Size: 234.0 MB (233964516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ad06888177b24063ae05dafc9247e689863fb1613426e8aada61266f866b6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3370261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069e29b9361100ecc014f74495732eec1be29f27d6445485c421a575cd748e6d`

```dockerfile
```

-	Layers:
	-	`sha256:42f511faa169283b64de7c07fcc439b29e94cfbd35c55447ff823f7b1ec1b401`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 3.4 MB (3350873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3417d69e7767d6f699cfad5d57a5c7bd9737cc3b8160c1c304be687424f1a458`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2ad752308c7e9895717c09a8edf153ec401e1630784d738b1273272451b04a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.1 MB (405077358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213ee1b558e4d747c55bf918c983c1aecd50d9abb790ce16c74e39309d230a9a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9f1e68c0dbea7ec6fbf1baa4a32510588d675f4692d4ae9d0a7e8d820cd9b308 NEO4J_TARBALL=neo4j-enterprise-4.4.39-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5dff04b2bf13f7daa9b187569e3dac438596fb37c4f93fe7d65747f4fe8d7b`  
		Last Modified: Tue, 03 Dec 2024 14:04:51 GMT  
		Size: 142.4 MB (142389020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c29744969a62a1da70f2683850426fde5a9f8ec5029055ad8e18e9e81767b9`  
		Last Modified: Tue, 03 Dec 2024 14:07:20 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af77ebefa4c5f79e14374f482e2984052eaf86f5a74a696b3004b806022e2ed5`  
		Last Modified: Tue, 03 Dec 2024 14:07:20 GMT  
		Size: 10.0 KB (9982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d87f5c65ba3d706a30e29adb3adad0a074ff00950d0e0dae9f67c0d6e970c`  
		Last Modified: Tue, 03 Dec 2024 14:07:25 GMT  
		Size: 233.9 MB (233929534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:761fa27d9c6d5290e49c150dbc9734206e41d9b995c72b2c6660c996cf8b4d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3370620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4210fb378ddadeeee693cce451d259caa966b50c3d40dc10da641ec0b5defb`

```dockerfile
```

-	Layers:
	-	`sha256:3144f71130270b2efaf6dd96ac1f2f38c7c7db03932b429d1c27ee96291e4fd9`  
		Last Modified: Tue, 03 Dec 2024 14:07:20 GMT  
		Size: 3.4 MB (3351112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3514c0cb5d115d9c65d36c6de119466e0babf9ff3db7f039bd479e8e7408b725`  
		Last Modified: Tue, 03 Dec 2024 14:07:20 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.39`

```console
$ docker pull neo4j@sha256:a646bfed7ad1c6d2dcd8026d407473834f849b62da829b61e626a388bfdcc840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.39` - linux; amd64

```console
$ docker pull neo4j@sha256:a00d4c310fda3dbb130bd1dabe9d0afba2154c466005f17a223a5509e65f9f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305100509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6205ba8801801f2d337d1d633962e8412c4e035f6327b8dec758943a39a52e6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0ed842590ef87186c2fa6843c0233756b1a25b631eb5d740bddf85896fbcce04 NEO4J_TARBALL=neo4j-community-4.4.39-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522cdc3b7b691c6fce64d54f4f6a91d7f90544400a02ce25ae100e50c6f0ca28`  
		Last Modified: Tue, 03 Dec 2024 03:25:37 GMT  
		Size: 145.6 MB (145601457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c885dbae8fd19d00239ba8c79aab627dee54283b393933eea064f69cc89b0fd1`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409cc90b263f3f4045961498fe8484531b536946954ef0bd5800d535d10b1375`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 10.0 KB (9987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2cd0020471319c7045cc2916ae55602c22eb3fbc16bcc11cb99f92680c3265`  
		Last Modified: Tue, 03 Dec 2024 03:25:37 GMT  
		Size: 129.2 MB (129232556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.39` - unknown; unknown

```console
$ docker pull neo4j@sha256:b0e0bf07da593dc89d7c0703533a1ff01215d87d36aa523c9ed13fd065a94c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3220140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e270c406e74bd1611186f133d5e18b8dd39433a6251d6a8188d1645c4f0c0db`

```dockerfile
```

-	Layers:
	-	`sha256:5ccddce5e1530673c9a6dec3be0088aab88534f9caff8ac3e128f1de855f91f0`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 3.2 MB (3200184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f886c12fdf7eadc9c1ba1678b0e6d9393d453ad513b30ba597056c1f68f088`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.39` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5eeaa11e1aa881ce1177904b043712de497515e032d77d4c167b01cb1e7c705b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300346623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747bcb46ef9a70a3d23416e4c79285b9655ea869ad7af557a3d667eb961c32d4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0ed842590ef87186c2fa6843c0233756b1a25b631eb5d740bddf85896fbcce04 NEO4J_TARBALL=neo4j-community-4.4.39-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5dff04b2bf13f7daa9b187569e3dac438596fb37c4f93fe7d65747f4fe8d7b`  
		Last Modified: Tue, 03 Dec 2024 14:04:51 GMT  
		Size: 142.4 MB (142389020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afddef27eca95f626d1ee7bdec235fec37a676b7cf6fd8b0ee711add1b464c7c`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261dfe618e6434ff87dc085a789d0bfd2fdd236d0f9173e59424cb16309f23dc`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b265d1704678ccd48e3b09cd3dcfbaf6332c44dc8e6a59becd20100ccb11d`  
		Last Modified: Tue, 03 Dec 2024 14:04:52 GMT  
		Size: 129.2 MB (129198794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.39` - unknown; unknown

```console
$ docker pull neo4j@sha256:536570858fd79700f7f6c2fe4d1b7c9af0adafc6791709ded48bd4a034f8b7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3220548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920defb81834493e445a8c3afb24f0444e92bf8e132dbac8c9862fdff553636b`

```dockerfile
```

-	Layers:
	-	`sha256:aa9ce0dd3b208a33d7cf9522dca92ca116fc59cc9a7d2815ea1815a2fc296bf8`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 3.2 MB (3200447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594c11ca7bc0996b1c2f548790b620e737cf860aeb094359c0b7349c7c5b3774`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 20.1 KB (20101 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.39-community`

```console
$ docker pull neo4j@sha256:a646bfed7ad1c6d2dcd8026d407473834f849b62da829b61e626a388bfdcc840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.39-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a00d4c310fda3dbb130bd1dabe9d0afba2154c466005f17a223a5509e65f9f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.1 MB (305100509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6205ba8801801f2d337d1d633962e8412c4e035f6327b8dec758943a39a52e6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0ed842590ef87186c2fa6843c0233756b1a25b631eb5d740bddf85896fbcce04 NEO4J_TARBALL=neo4j-community-4.4.39-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522cdc3b7b691c6fce64d54f4f6a91d7f90544400a02ce25ae100e50c6f0ca28`  
		Last Modified: Tue, 03 Dec 2024 03:25:37 GMT  
		Size: 145.6 MB (145601457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c885dbae8fd19d00239ba8c79aab627dee54283b393933eea064f69cc89b0fd1`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409cc90b263f3f4045961498fe8484531b536946954ef0bd5800d535d10b1375`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 10.0 KB (9987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2cd0020471319c7045cc2916ae55602c22eb3fbc16bcc11cb99f92680c3265`  
		Last Modified: Tue, 03 Dec 2024 03:25:37 GMT  
		Size: 129.2 MB (129232556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.39-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b0e0bf07da593dc89d7c0703533a1ff01215d87d36aa523c9ed13fd065a94c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3220140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e270c406e74bd1611186f133d5e18b8dd39433a6251d6a8188d1645c4f0c0db`

```dockerfile
```

-	Layers:
	-	`sha256:5ccddce5e1530673c9a6dec3be0088aab88534f9caff8ac3e128f1de855f91f0`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 3.2 MB (3200184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f886c12fdf7eadc9c1ba1678b0e6d9393d453ad513b30ba597056c1f68f088`  
		Last Modified: Tue, 03 Dec 2024 03:25:35 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.39-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5eeaa11e1aa881ce1177904b043712de497515e032d77d4c167b01cb1e7c705b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300346623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747bcb46ef9a70a3d23416e4c79285b9655ea869ad7af557a3d667eb961c32d4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=0ed842590ef87186c2fa6843c0233756b1a25b631eb5d740bddf85896fbcce04 NEO4J_TARBALL=neo4j-community-4.4.39-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5dff04b2bf13f7daa9b187569e3dac438596fb37c4f93fe7d65747f4fe8d7b`  
		Last Modified: Tue, 03 Dec 2024 14:04:51 GMT  
		Size: 142.4 MB (142389020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afddef27eca95f626d1ee7bdec235fec37a676b7cf6fd8b0ee711add1b464c7c`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261dfe618e6434ff87dc085a789d0bfd2fdd236d0f9173e59424cb16309f23dc`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b265d1704678ccd48e3b09cd3dcfbaf6332c44dc8e6a59becd20100ccb11d`  
		Last Modified: Tue, 03 Dec 2024 14:04:52 GMT  
		Size: 129.2 MB (129198794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.39-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:536570858fd79700f7f6c2fe4d1b7c9af0adafc6791709ded48bd4a034f8b7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3220548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920defb81834493e445a8c3afb24f0444e92bf8e132dbac8c9862fdff553636b`

```dockerfile
```

-	Layers:
	-	`sha256:aa9ce0dd3b208a33d7cf9522dca92ca116fc59cc9a7d2815ea1815a2fc296bf8`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 3.2 MB (3200447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594c11ca7bc0996b1c2f548790b620e737cf860aeb094359c0b7349c7c5b3774`  
		Last Modified: Tue, 03 Dec 2024 14:04:48 GMT  
		Size: 20.1 KB (20101 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.39-enterprise`

```console
$ docker pull neo4j@sha256:a161b88a2b184c99ada158cbe8855445af3d353344f1c4b53e186fdee03aba60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.39-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ba1428fee503ff1e9bf19cb30058a97785695030c59d088d102c26f9aedd06bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.8 MB (409832468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ec500f7e987cdb804cb0ea0b065a88bf416cb5e0c301a0cdd52d161d6b9ffe`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9f1e68c0dbea7ec6fbf1baa4a32510588d675f4692d4ae9d0a7e8d820cd9b308 NEO4J_TARBALL=neo4j-enterprise-4.4.39-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0503670579e43950881346fbbf9391d490262def6b985426e02e8996af7941e4`  
		Last Modified: Tue, 03 Dec 2024 03:25:51 GMT  
		Size: 145.6 MB (145601451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d3d88084864472e0a664af1bc5c367337919ba10ce49a307d24e4548de0bb8`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ed4ac710ca84242e376f4bfccaab03a29f5665d3a1218e0c98ca47f1ed3991`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 10.0 KB (9986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193734ef44ba5f18d1587fe2605128ca7aee5f0931be51fc23c9c1bef1ea3b5d`  
		Last Modified: Tue, 03 Dec 2024 03:25:51 GMT  
		Size: 234.0 MB (233964516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.39-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ad06888177b24063ae05dafc9247e689863fb1613426e8aada61266f866b6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3370261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069e29b9361100ecc014f74495732eec1be29f27d6445485c421a575cd748e6d`

```dockerfile
```

-	Layers:
	-	`sha256:42f511faa169283b64de7c07fcc439b29e94cfbd35c55447ff823f7b1ec1b401`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 3.4 MB (3350873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3417d69e7767d6f699cfad5d57a5c7bd9737cc3b8160c1c304be687424f1a458`  
		Last Modified: Tue, 03 Dec 2024 03:25:48 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.39-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2ad752308c7e9895717c09a8edf153ec401e1630784d738b1273272451b04a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.1 MB (405077358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213ee1b558e4d747c55bf918c983c1aecd50d9abb790ce16c74e39309d230a9a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 22 Nov 2024 10:48:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Fri, 22 Nov 2024 10:48:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 22 Nov 2024 10:48:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9f1e68c0dbea7ec6fbf1baa4a32510588d675f4692d4ae9d0a7e8d820cd9b308 NEO4J_TARBALL=neo4j-enterprise-4.4.39-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Fri, 22 Nov 2024 10:48:03 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.39-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 22 Nov 2024 10:48:03 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2024 10:48:03 GMT
WORKDIR /var/lib/neo4j
# Fri, 22 Nov 2024 10:48:03 GMT
VOLUME [/data /logs]
# Fri, 22 Nov 2024 10:48:03 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 22 Nov 2024 10:48:03 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 10:48:03 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5dff04b2bf13f7daa9b187569e3dac438596fb37c4f93fe7d65747f4fe8d7b`  
		Last Modified: Tue, 03 Dec 2024 14:04:51 GMT  
		Size: 142.4 MB (142389020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c29744969a62a1da70f2683850426fde5a9f8ec5029055ad8e18e9e81767b9`  
		Last Modified: Tue, 03 Dec 2024 14:07:20 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af77ebefa4c5f79e14374f482e2984052eaf86f5a74a696b3004b806022e2ed5`  
		Last Modified: Tue, 03 Dec 2024 14:07:20 GMT  
		Size: 10.0 KB (9982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d87f5c65ba3d706a30e29adb3adad0a074ff00950d0e0dae9f67c0d6e970c`  
		Last Modified: Tue, 03 Dec 2024 14:07:25 GMT  
		Size: 233.9 MB (233929534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.39-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:761fa27d9c6d5290e49c150dbc9734206e41d9b995c72b2c6660c996cf8b4d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3370620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4210fb378ddadeeee693cce451d259caa966b50c3d40dc10da641ec0b5defb`

```dockerfile
```

-	Layers:
	-	`sha256:3144f71130270b2efaf6dd96ac1f2f38c7c7db03932b429d1c27ee96291e4fd9`  
		Last Modified: Tue, 03 Dec 2024 14:07:20 GMT  
		Size: 3.4 MB (3351112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3514c0cb5d115d9c65d36c6de119466e0babf9ff3db7f039bd479e8e7408b725`  
		Last Modified: Tue, 03 Dec 2024 14:07:20 GMT  
		Size: 19.5 KB (19508 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:8ca1b48108451dc79dc78280471143e98e4f42761bf0352c4d40ecacddd971f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3a07d4c3514a3a140209179bbc989ae6dcfe2221926e81c6b0278fcc69ec11bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332261595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c61a88c53b2d3ccad523075dd77353a4ec3cbffb564ee108d22309ed6e7878`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb449271df182b23f612d36d13b2e3fbeb7c8b1b801a03c4836b8879acd3c2d`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 133.9 MB (133857635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4271fb21b47adc8526a5203c5a0ac7cfa91a8482d7ecd0019f00460de4f6a`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d08690d60e34b502dd155f05d369a0b7e05f59e570cfe7340653f84b5cd2ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 159.0 MB (158974600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5b7cea601a7170bc77285f257cbb01968e70faf65984d8b914c4ef0da18bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6420457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df82eb069e58c33116ff7dd217664c7df6d7fe96a27d4219a3bddb47954c82`

```dockerfile
```

-	Layers:
	-	`sha256:c5dbe9e0cd47923c10317270d46d877e20c83c036267038f63379a751c56e736`  
		Last Modified: Wed, 11 Dec 2024 20:30:21 GMT  
		Size: 6.4 MB (6398690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857345cd65c672d5a9f26c7182964ed1b8ad7101683a9bce8bd5ea22237f08ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:41b127d076695b95d714b8d7e9a1c12bac2ea34eb4f7919be5cf643cd90fe849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330473904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b0209c870dd34862be29fdb99607414d532f07a600e3ecd9306d537deff00a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec867fd87e18f223055f7512b18b0403db034a194bc9eaf4e9fe8dcb6398010`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 159.0 MB (158974628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e93c85ec2fd0ac6c21f5cb6658ceca7f3c3b7156d6ca2c0bcdbd31e1f2fedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac93d9ae9358b1959a3a49541df90a2f94f3dea762cf6a2533203e6da32aa480`

```dockerfile
```

-	Layers:
	-	`sha256:1fd3c7e653a94849d95f1d07a42e4b60bf1dba88b7a7718ba1e4e1578e7e84c3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 6.4 MB (6378303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d3591854f94c9463c485dab703af1b00d944ee9e86d246a1304499197be158`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:cc0383c2422befc8f18436e4d0ac10ccb1ec8dfaa1059274e4b1c8ef68a88f6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1a344bec7aa22801f8161da45e9315cbd0ee675bf609a0c2bcd818a16884c1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624452280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd37cb1e2f9ee6b72c807625151e3df1cb69ffca720b1765bf37ecaa8b2669`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7883af60572206c2c155ee75ad9f7cbbdabb1bf196d91d8c9cf5fd5e433b0d8`  
		Last Modified: Mon, 09 Dec 2024 19:31:42 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072cd16f67817e8bb1fe9b546bb6203d98bcc057ec858a31dc1a7186aa5eadd6`  
		Last Modified: Mon, 09 Dec 2024 19:31:46 GMT  
		Size: 449.6 MB (449649015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4d3109bfd5bf5c2ecd5ed1986162d5e07708e674e166a1e9b512288cd0b8658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9687a9804b3faaa31901ca5a6dffb282b33c9ccb810d8d1f5a257f930e63238`

```dockerfile
```

-	Layers:
	-	`sha256:6d86386f6a77721f37a1fdbe3095922982a5432bb50c68c1cf008396d17b62c6`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 3.6 MB (3551481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950fe4bcedc78eb5f67fb4c0b87ef9c1018819ab9b740e4e7789fd69896ff0ef`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9a9e36ad05c7acc4f53c377b7af0c3e5fd2292406304b2ca780dd6613f3a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621734165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9306b866e1458428b58ca461cad204812e23659a768aa100e3f06a6fdc203d44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e66b4604c710e62a04b89e80fb806ac571b28e00c8337016b9b3870852110`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58037f66f958514fd05b12544c5c499cdecff55b3f2ed3dbca9b6b6032247f3`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7097958692f8fbd70eb15887b22d3dfb26b7d54c8b4c7bfb36ea4e4fb49b045`  
		Last Modified: Tue, 10 Dec 2024 01:20:40 GMT  
		Size: 449.6 MB (449614350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b729c49bee0ba5de19eb0cf8d34cc0151c8de41effb0fd089911585d0a0efc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda59757c40e04ee6d376740096190ff94b64fd2efa6b0702f402b59a3bbe0ad`

```dockerfile
```

-	Layers:
	-	`sha256:36090a5a4c81d065885cb3b7dd3108cc3dcd1bf90af68e9e2bdf75eac80cf38b`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.6 MB (3551173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554db7c08a0e27d6cae88b0214e8b54b679a151ee920c15c7cc551bba9dbe8db`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:cc0383c2422befc8f18436e4d0ac10ccb1ec8dfaa1059274e4b1c8ef68a88f6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1a344bec7aa22801f8161da45e9315cbd0ee675bf609a0c2bcd818a16884c1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624452280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd37cb1e2f9ee6b72c807625151e3df1cb69ffca720b1765bf37ecaa8b2669`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7883af60572206c2c155ee75ad9f7cbbdabb1bf196d91d8c9cf5fd5e433b0d8`  
		Last Modified: Mon, 09 Dec 2024 19:31:42 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072cd16f67817e8bb1fe9b546bb6203d98bcc057ec858a31dc1a7186aa5eadd6`  
		Last Modified: Mon, 09 Dec 2024 19:31:46 GMT  
		Size: 449.6 MB (449649015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4d3109bfd5bf5c2ecd5ed1986162d5e07708e674e166a1e9b512288cd0b8658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9687a9804b3faaa31901ca5a6dffb282b33c9ccb810d8d1f5a257f930e63238`

```dockerfile
```

-	Layers:
	-	`sha256:6d86386f6a77721f37a1fdbe3095922982a5432bb50c68c1cf008396d17b62c6`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 3.6 MB (3551481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950fe4bcedc78eb5f67fb4c0b87ef9c1018819ab9b740e4e7789fd69896ff0ef`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9a9e36ad05c7acc4f53c377b7af0c3e5fd2292406304b2ca780dd6613f3a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621734165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9306b866e1458428b58ca461cad204812e23659a768aa100e3f06a6fdc203d44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e66b4604c710e62a04b89e80fb806ac571b28e00c8337016b9b3870852110`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58037f66f958514fd05b12544c5c499cdecff55b3f2ed3dbca9b6b6032247f3`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7097958692f8fbd70eb15887b22d3dfb26b7d54c8b4c7bfb36ea4e4fb49b045`  
		Last Modified: Tue, 10 Dec 2024 01:20:40 GMT  
		Size: 449.6 MB (449614350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b729c49bee0ba5de19eb0cf8d34cc0151c8de41effb0fd089911585d0a0efc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda59757c40e04ee6d376740096190ff94b64fd2efa6b0702f402b59a3bbe0ad`

```dockerfile
```

-	Layers:
	-	`sha256:36090a5a4c81d065885cb3b7dd3108cc3dcd1bf90af68e9e2bdf75eac80cf38b`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.6 MB (3551173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554db7c08a0e27d6cae88b0214e8b54b679a151ee920c15c7cc551bba9dbe8db`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:3c5fd2df54d8963f534234798ffeb1aba32efb451e49857f32aff43049d1c397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ea5cfcf54fd2687dbcbd7c0d8b80e7d2c7c12455d0a11dc59115025cae75adf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (620008790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c665da7365d4d53b4c876bda24890d305a7435552a9a8d23d3bb4b20e46d4af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc6524ff49eab59fdce5378d4e8dd567adbe0fbef3cf2ea61cc645f2766466a`  
		Last Modified: Wed, 11 Dec 2024 20:30:37 GMT  
		Size: 133.9 MB (133859633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7565601d292d8e9a14f6b5efe3b771cdbd9043129838158de80eb482051d7a`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88ffcb43fa11e336a37abfa4aa70fce56a279843deb4141a3ab82d42e875bac`  
		Last Modified: Wed, 11 Dec 2024 20:30:42 GMT  
		Size: 446.7 MB (446719796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:aab5f73a2efb5b56430ca015f2cda43f62f52528ee9ec342b391d56b484ee1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027039802db0b73abdf28b8819b0a5db0b40d1b436a3c5a7585854f76a03380c`

```dockerfile
```

-	Layers:
	-	`sha256:b9903fecd8bbac4e56beb432601f0786b2faf9eba461cf34bf4f90642a279235`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 6.7 MB (6711329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80362427837bd120a6f4e803d44ca5ba1331f4c0e5260c692cb699febf5bc156`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 20.6 KB (20588 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0082eef4d95f0ce597227e2e19fdbbf01d2dc21adbcb58701837caadc6c8c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.2 MB (618219110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d88e2b4e12af2d3cc2f6301d04b390ebc5a171674f6b826c34e73dcfeebb599`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e3709cf841bc19ef451c077eafcac2a0d807b9aaff5f0c93e1c588e92b4e66`  
		Last Modified: Wed, 11 Dec 2024 20:51:01 GMT  
		Size: 446.7 MB (446719834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17082a1854941eb3148276237e9ab494263ab1a37e5d7386e7f6fbe052ff75ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6711595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe04d39a37f9c52a4d1956cc73bd4531156724bd66d699e9fefb9dc4844061e`

```dockerfile
```

-	Layers:
	-	`sha256:c1b2002ab188c60f328786069d783605ed0f7435250b720b4f661ce812332ecd`  
		Last Modified: Wed, 11 Dec 2024 20:50:52 GMT  
		Size: 6.7 MB (6690894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53facf7f437fd7125aaed6899ff4dc092806bbfde05b9450749ecd797aa87baa`  
		Last Modified: Wed, 11 Dec 2024 20:50:51 GMT  
		Size: 20.7 KB (20701 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:8ca1b48108451dc79dc78280471143e98e4f42761bf0352c4d40ecacddd971f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3a07d4c3514a3a140209179bbc989ae6dcfe2221926e81c6b0278fcc69ec11bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332261595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c61a88c53b2d3ccad523075dd77353a4ec3cbffb564ee108d22309ed6e7878`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb449271df182b23f612d36d13b2e3fbeb7c8b1b801a03c4836b8879acd3c2d`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 133.9 MB (133857635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4271fb21b47adc8526a5203c5a0ac7cfa91a8482d7ecd0019f00460de4f6a`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d08690d60e34b502dd155f05d369a0b7e05f59e570cfe7340653f84b5cd2ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 159.0 MB (158974600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5b7cea601a7170bc77285f257cbb01968e70faf65984d8b914c4ef0da18bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6420457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df82eb069e58c33116ff7dd217664c7df6d7fe96a27d4219a3bddb47954c82`

```dockerfile
```

-	Layers:
	-	`sha256:c5dbe9e0cd47923c10317270d46d877e20c83c036267038f63379a751c56e736`  
		Last Modified: Wed, 11 Dec 2024 20:30:21 GMT  
		Size: 6.4 MB (6398690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857345cd65c672d5a9f26c7182964ed1b8ad7101683a9bce8bd5ea22237f08ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:41b127d076695b95d714b8d7e9a1c12bac2ea34eb4f7919be5cf643cd90fe849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330473904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b0209c870dd34862be29fdb99607414d532f07a600e3ecd9306d537deff00a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec867fd87e18f223055f7512b18b0403db034a194bc9eaf4e9fe8dcb6398010`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 159.0 MB (158974628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e93c85ec2fd0ac6c21f5cb6658ceca7f3c3b7156d6ca2c0bcdbd31e1f2fedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac93d9ae9358b1959a3a49541df90a2f94f3dea762cf6a2533203e6da32aa480`

```dockerfile
```

-	Layers:
	-	`sha256:1fd3c7e653a94849d95f1d07a42e4b60bf1dba88b7a7718ba1e4e1578e7e84c3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 6.4 MB (6378303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d3591854f94c9463c485dab703af1b00d944ee9e86d246a1304499197be158`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-bullseye`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-community`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-community` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-community-bullseye`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-community-ubi9`

```console
$ docker pull neo4j@sha256:8ca1b48108451dc79dc78280471143e98e4f42761bf0352c4d40ecacddd971f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3a07d4c3514a3a140209179bbc989ae6dcfe2221926e81c6b0278fcc69ec11bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332261595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c61a88c53b2d3ccad523075dd77353a4ec3cbffb564ee108d22309ed6e7878`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb449271df182b23f612d36d13b2e3fbeb7c8b1b801a03c4836b8879acd3c2d`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 133.9 MB (133857635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4271fb21b47adc8526a5203c5a0ac7cfa91a8482d7ecd0019f00460de4f6a`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d08690d60e34b502dd155f05d369a0b7e05f59e570cfe7340653f84b5cd2ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 159.0 MB (158974600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5b7cea601a7170bc77285f257cbb01968e70faf65984d8b914c4ef0da18bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6420457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df82eb069e58c33116ff7dd217664c7df6d7fe96a27d4219a3bddb47954c82`

```dockerfile
```

-	Layers:
	-	`sha256:c5dbe9e0cd47923c10317270d46d877e20c83c036267038f63379a751c56e736`  
		Last Modified: Wed, 11 Dec 2024 20:30:21 GMT  
		Size: 6.4 MB (6398690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857345cd65c672d5a9f26c7182964ed1b8ad7101683a9bce8bd5ea22237f08ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:41b127d076695b95d714b8d7e9a1c12bac2ea34eb4f7919be5cf643cd90fe849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330473904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b0209c870dd34862be29fdb99607414d532f07a600e3ecd9306d537deff00a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec867fd87e18f223055f7512b18b0403db034a194bc9eaf4e9fe8dcb6398010`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 159.0 MB (158974628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e93c85ec2fd0ac6c21f5cb6658ceca7f3c3b7156d6ca2c0bcdbd31e1f2fedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac93d9ae9358b1959a3a49541df90a2f94f3dea762cf6a2533203e6da32aa480`

```dockerfile
```

-	Layers:
	-	`sha256:1fd3c7e653a94849d95f1d07a42e4b60bf1dba88b7a7718ba1e4e1578e7e84c3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 6.4 MB (6378303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d3591854f94c9463c485dab703af1b00d944ee9e86d246a1304499197be158`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-enterprise`

```console
$ docker pull neo4j@sha256:cc0383c2422befc8f18436e4d0ac10ccb1ec8dfaa1059274e4b1c8ef68a88f6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1a344bec7aa22801f8161da45e9315cbd0ee675bf609a0c2bcd818a16884c1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624452280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd37cb1e2f9ee6b72c807625151e3df1cb69ffca720b1765bf37ecaa8b2669`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7883af60572206c2c155ee75ad9f7cbbdabb1bf196d91d8c9cf5fd5e433b0d8`  
		Last Modified: Mon, 09 Dec 2024 19:31:42 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072cd16f67817e8bb1fe9b546bb6203d98bcc057ec858a31dc1a7186aa5eadd6`  
		Last Modified: Mon, 09 Dec 2024 19:31:46 GMT  
		Size: 449.6 MB (449649015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4d3109bfd5bf5c2ecd5ed1986162d5e07708e674e166a1e9b512288cd0b8658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9687a9804b3faaa31901ca5a6dffb282b33c9ccb810d8d1f5a257f930e63238`

```dockerfile
```

-	Layers:
	-	`sha256:6d86386f6a77721f37a1fdbe3095922982a5432bb50c68c1cf008396d17b62c6`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 3.6 MB (3551481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950fe4bcedc78eb5f67fb4c0b87ef9c1018819ab9b740e4e7789fd69896ff0ef`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9a9e36ad05c7acc4f53c377b7af0c3e5fd2292406304b2ca780dd6613f3a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621734165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9306b866e1458428b58ca461cad204812e23659a768aa100e3f06a6fdc203d44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e66b4604c710e62a04b89e80fb806ac571b28e00c8337016b9b3870852110`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58037f66f958514fd05b12544c5c499cdecff55b3f2ed3dbca9b6b6032247f3`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7097958692f8fbd70eb15887b22d3dfb26b7d54c8b4c7bfb36ea4e4fb49b045`  
		Last Modified: Tue, 10 Dec 2024 01:20:40 GMT  
		Size: 449.6 MB (449614350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b729c49bee0ba5de19eb0cf8d34cc0151c8de41effb0fd089911585d0a0efc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda59757c40e04ee6d376740096190ff94b64fd2efa6b0702f402b59a3bbe0ad`

```dockerfile
```

-	Layers:
	-	`sha256:36090a5a4c81d065885cb3b7dd3108cc3dcd1bf90af68e9e2bdf75eac80cf38b`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.6 MB (3551173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554db7c08a0e27d6cae88b0214e8b54b679a151ee920c15c7cc551bba9dbe8db`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:cc0383c2422befc8f18436e4d0ac10ccb1ec8dfaa1059274e4b1c8ef68a88f6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1a344bec7aa22801f8161da45e9315cbd0ee675bf609a0c2bcd818a16884c1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624452280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd37cb1e2f9ee6b72c807625151e3df1cb69ffca720b1765bf37ecaa8b2669`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7883af60572206c2c155ee75ad9f7cbbdabb1bf196d91d8c9cf5fd5e433b0d8`  
		Last Modified: Mon, 09 Dec 2024 19:31:42 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072cd16f67817e8bb1fe9b546bb6203d98bcc057ec858a31dc1a7186aa5eadd6`  
		Last Modified: Mon, 09 Dec 2024 19:31:46 GMT  
		Size: 449.6 MB (449649015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4d3109bfd5bf5c2ecd5ed1986162d5e07708e674e166a1e9b512288cd0b8658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9687a9804b3faaa31901ca5a6dffb282b33c9ccb810d8d1f5a257f930e63238`

```dockerfile
```

-	Layers:
	-	`sha256:6d86386f6a77721f37a1fdbe3095922982a5432bb50c68c1cf008396d17b62c6`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 3.6 MB (3551481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950fe4bcedc78eb5f67fb4c0b87ef9c1018819ab9b740e4e7789fd69896ff0ef`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9a9e36ad05c7acc4f53c377b7af0c3e5fd2292406304b2ca780dd6613f3a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621734165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9306b866e1458428b58ca461cad204812e23659a768aa100e3f06a6fdc203d44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e66b4604c710e62a04b89e80fb806ac571b28e00c8337016b9b3870852110`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58037f66f958514fd05b12544c5c499cdecff55b3f2ed3dbca9b6b6032247f3`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7097958692f8fbd70eb15887b22d3dfb26b7d54c8b4c7bfb36ea4e4fb49b045`  
		Last Modified: Tue, 10 Dec 2024 01:20:40 GMT  
		Size: 449.6 MB (449614350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b729c49bee0ba5de19eb0cf8d34cc0151c8de41effb0fd089911585d0a0efc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda59757c40e04ee6d376740096190ff94b64fd2efa6b0702f402b59a3bbe0ad`

```dockerfile
```

-	Layers:
	-	`sha256:36090a5a4c81d065885cb3b7dd3108cc3dcd1bf90af68e9e2bdf75eac80cf38b`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.6 MB (3551173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554db7c08a0e27d6cae88b0214e8b54b679a151ee920c15c7cc551bba9dbe8db`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:3c5fd2df54d8963f534234798ffeb1aba32efb451e49857f32aff43049d1c397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ea5cfcf54fd2687dbcbd7c0d8b80e7d2c7c12455d0a11dc59115025cae75adf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (620008790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c665da7365d4d53b4c876bda24890d305a7435552a9a8d23d3bb4b20e46d4af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc6524ff49eab59fdce5378d4e8dd567adbe0fbef3cf2ea61cc645f2766466a`  
		Last Modified: Wed, 11 Dec 2024 20:30:37 GMT  
		Size: 133.9 MB (133859633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7565601d292d8e9a14f6b5efe3b771cdbd9043129838158de80eb482051d7a`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88ffcb43fa11e336a37abfa4aa70fce56a279843deb4141a3ab82d42e875bac`  
		Last Modified: Wed, 11 Dec 2024 20:30:42 GMT  
		Size: 446.7 MB (446719796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:aab5f73a2efb5b56430ca015f2cda43f62f52528ee9ec342b391d56b484ee1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027039802db0b73abdf28b8819b0a5db0b40d1b436a3c5a7585854f76a03380c`

```dockerfile
```

-	Layers:
	-	`sha256:b9903fecd8bbac4e56beb432601f0786b2faf9eba461cf34bf4f90642a279235`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 6.7 MB (6711329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80362427837bd120a6f4e803d44ca5ba1331f4c0e5260c692cb699febf5bc156`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 20.6 KB (20588 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0082eef4d95f0ce597227e2e19fdbbf01d2dc21adbcb58701837caadc6c8c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.2 MB (618219110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d88e2b4e12af2d3cc2f6301d04b390ebc5a171674f6b826c34e73dcfeebb599`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e3709cf841bc19ef451c077eafcac2a0d807b9aaff5f0c93e1c588e92b4e66`  
		Last Modified: Wed, 11 Dec 2024 20:51:01 GMT  
		Size: 446.7 MB (446719834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17082a1854941eb3148276237e9ab494263ab1a37e5d7386e7f6fbe052ff75ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6711595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe04d39a37f9c52a4d1956cc73bd4531156724bd66d699e9fefb9dc4844061e`

```dockerfile
```

-	Layers:
	-	`sha256:c1b2002ab188c60f328786069d783605ed0f7435250b720b4f661ce812332ecd`  
		Last Modified: Wed, 11 Dec 2024 20:50:52 GMT  
		Size: 6.7 MB (6690894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53facf7f437fd7125aaed6899ff4dc092806bbfde05b9450749ecd797aa87baa`  
		Last Modified: Wed, 11 Dec 2024 20:50:51 GMT  
		Size: 20.7 KB (20701 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-ubi9`

```console
$ docker pull neo4j@sha256:8ca1b48108451dc79dc78280471143e98e4f42761bf0352c4d40ecacddd971f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3a07d4c3514a3a140209179bbc989ae6dcfe2221926e81c6b0278fcc69ec11bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332261595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c61a88c53b2d3ccad523075dd77353a4ec3cbffb564ee108d22309ed6e7878`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb449271df182b23f612d36d13b2e3fbeb7c8b1b801a03c4836b8879acd3c2d`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 133.9 MB (133857635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4271fb21b47adc8526a5203c5a0ac7cfa91a8482d7ecd0019f00460de4f6a`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d08690d60e34b502dd155f05d369a0b7e05f59e570cfe7340653f84b5cd2ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 159.0 MB (158974600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5b7cea601a7170bc77285f257cbb01968e70faf65984d8b914c4ef0da18bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6420457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df82eb069e58c33116ff7dd217664c7df6d7fe96a27d4219a3bddb47954c82`

```dockerfile
```

-	Layers:
	-	`sha256:c5dbe9e0cd47923c10317270d46d877e20c83c036267038f63379a751c56e736`  
		Last Modified: Wed, 11 Dec 2024 20:30:21 GMT  
		Size: 6.4 MB (6398690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857345cd65c672d5a9f26c7182964ed1b8ad7101683a9bce8bd5ea22237f08ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:41b127d076695b95d714b8d7e9a1c12bac2ea34eb4f7919be5cf643cd90fe849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330473904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b0209c870dd34862be29fdb99607414d532f07a600e3ecd9306d537deff00a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec867fd87e18f223055f7512b18b0403db034a194bc9eaf4e9fe8dcb6398010`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 159.0 MB (158974628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e93c85ec2fd0ac6c21f5cb6658ceca7f3c3b7156d6ca2c0bcdbd31e1f2fedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac93d9ae9358b1959a3a49541df90a2f94f3dea762cf6a2533203e6da32aa480`

```dockerfile
```

-	Layers:
	-	`sha256:1fd3c7e653a94849d95f1d07a42e4b60bf1dba88b7a7718ba1e4e1578e7e84c3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 6.4 MB (6378303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d3591854f94c9463c485dab703af1b00d944ee9e86d246a1304499197be158`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-bullseye`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-community`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-community-bullseye`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-community-ubi9`

```console
$ docker pull neo4j@sha256:8ca1b48108451dc79dc78280471143e98e4f42761bf0352c4d40ecacddd971f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3a07d4c3514a3a140209179bbc989ae6dcfe2221926e81c6b0278fcc69ec11bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332261595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c61a88c53b2d3ccad523075dd77353a4ec3cbffb564ee108d22309ed6e7878`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb449271df182b23f612d36d13b2e3fbeb7c8b1b801a03c4836b8879acd3c2d`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 133.9 MB (133857635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4271fb21b47adc8526a5203c5a0ac7cfa91a8482d7ecd0019f00460de4f6a`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d08690d60e34b502dd155f05d369a0b7e05f59e570cfe7340653f84b5cd2ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 159.0 MB (158974600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5b7cea601a7170bc77285f257cbb01968e70faf65984d8b914c4ef0da18bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6420457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df82eb069e58c33116ff7dd217664c7df6d7fe96a27d4219a3bddb47954c82`

```dockerfile
```

-	Layers:
	-	`sha256:c5dbe9e0cd47923c10317270d46d877e20c83c036267038f63379a751c56e736`  
		Last Modified: Wed, 11 Dec 2024 20:30:21 GMT  
		Size: 6.4 MB (6398690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857345cd65c672d5a9f26c7182964ed1b8ad7101683a9bce8bd5ea22237f08ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:41b127d076695b95d714b8d7e9a1c12bac2ea34eb4f7919be5cf643cd90fe849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330473904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b0209c870dd34862be29fdb99607414d532f07a600e3ecd9306d537deff00a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec867fd87e18f223055f7512b18b0403db034a194bc9eaf4e9fe8dcb6398010`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 159.0 MB (158974628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e93c85ec2fd0ac6c21f5cb6658ceca7f3c3b7156d6ca2c0bcdbd31e1f2fedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac93d9ae9358b1959a3a49541df90a2f94f3dea762cf6a2533203e6da32aa480`

```dockerfile
```

-	Layers:
	-	`sha256:1fd3c7e653a94849d95f1d07a42e4b60bf1dba88b7a7718ba1e4e1578e7e84c3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 6.4 MB (6378303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d3591854f94c9463c485dab703af1b00d944ee9e86d246a1304499197be158`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-enterprise`

```console
$ docker pull neo4j@sha256:cc0383c2422befc8f18436e4d0ac10ccb1ec8dfaa1059274e4b1c8ef68a88f6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1a344bec7aa22801f8161da45e9315cbd0ee675bf609a0c2bcd818a16884c1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624452280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd37cb1e2f9ee6b72c807625151e3df1cb69ffca720b1765bf37ecaa8b2669`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7883af60572206c2c155ee75ad9f7cbbdabb1bf196d91d8c9cf5fd5e433b0d8`  
		Last Modified: Mon, 09 Dec 2024 19:31:42 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072cd16f67817e8bb1fe9b546bb6203d98bcc057ec858a31dc1a7186aa5eadd6`  
		Last Modified: Mon, 09 Dec 2024 19:31:46 GMT  
		Size: 449.6 MB (449649015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4d3109bfd5bf5c2ecd5ed1986162d5e07708e674e166a1e9b512288cd0b8658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9687a9804b3faaa31901ca5a6dffb282b33c9ccb810d8d1f5a257f930e63238`

```dockerfile
```

-	Layers:
	-	`sha256:6d86386f6a77721f37a1fdbe3095922982a5432bb50c68c1cf008396d17b62c6`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 3.6 MB (3551481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950fe4bcedc78eb5f67fb4c0b87ef9c1018819ab9b740e4e7789fd69896ff0ef`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9a9e36ad05c7acc4f53c377b7af0c3e5fd2292406304b2ca780dd6613f3a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621734165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9306b866e1458428b58ca461cad204812e23659a768aa100e3f06a6fdc203d44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e66b4604c710e62a04b89e80fb806ac571b28e00c8337016b9b3870852110`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58037f66f958514fd05b12544c5c499cdecff55b3f2ed3dbca9b6b6032247f3`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7097958692f8fbd70eb15887b22d3dfb26b7d54c8b4c7bfb36ea4e4fb49b045`  
		Last Modified: Tue, 10 Dec 2024 01:20:40 GMT  
		Size: 449.6 MB (449614350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b729c49bee0ba5de19eb0cf8d34cc0151c8de41effb0fd089911585d0a0efc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda59757c40e04ee6d376740096190ff94b64fd2efa6b0702f402b59a3bbe0ad`

```dockerfile
```

-	Layers:
	-	`sha256:36090a5a4c81d065885cb3b7dd3108cc3dcd1bf90af68e9e2bdf75eac80cf38b`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.6 MB (3551173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554db7c08a0e27d6cae88b0214e8b54b679a151ee920c15c7cc551bba9dbe8db`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:cc0383c2422befc8f18436e4d0ac10ccb1ec8dfaa1059274e4b1c8ef68a88f6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1a344bec7aa22801f8161da45e9315cbd0ee675bf609a0c2bcd818a16884c1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624452280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd37cb1e2f9ee6b72c807625151e3df1cb69ffca720b1765bf37ecaa8b2669`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7883af60572206c2c155ee75ad9f7cbbdabb1bf196d91d8c9cf5fd5e433b0d8`  
		Last Modified: Mon, 09 Dec 2024 19:31:42 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072cd16f67817e8bb1fe9b546bb6203d98bcc057ec858a31dc1a7186aa5eadd6`  
		Last Modified: Mon, 09 Dec 2024 19:31:46 GMT  
		Size: 449.6 MB (449649015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4d3109bfd5bf5c2ecd5ed1986162d5e07708e674e166a1e9b512288cd0b8658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9687a9804b3faaa31901ca5a6dffb282b33c9ccb810d8d1f5a257f930e63238`

```dockerfile
```

-	Layers:
	-	`sha256:6d86386f6a77721f37a1fdbe3095922982a5432bb50c68c1cf008396d17b62c6`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 3.6 MB (3551481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950fe4bcedc78eb5f67fb4c0b87ef9c1018819ab9b740e4e7789fd69896ff0ef`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9a9e36ad05c7acc4f53c377b7af0c3e5fd2292406304b2ca780dd6613f3a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621734165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9306b866e1458428b58ca461cad204812e23659a768aa100e3f06a6fdc203d44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e66b4604c710e62a04b89e80fb806ac571b28e00c8337016b9b3870852110`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58037f66f958514fd05b12544c5c499cdecff55b3f2ed3dbca9b6b6032247f3`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7097958692f8fbd70eb15887b22d3dfb26b7d54c8b4c7bfb36ea4e4fb49b045`  
		Last Modified: Tue, 10 Dec 2024 01:20:40 GMT  
		Size: 449.6 MB (449614350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b729c49bee0ba5de19eb0cf8d34cc0151c8de41effb0fd089911585d0a0efc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda59757c40e04ee6d376740096190ff94b64fd2efa6b0702f402b59a3bbe0ad`

```dockerfile
```

-	Layers:
	-	`sha256:36090a5a4c81d065885cb3b7dd3108cc3dcd1bf90af68e9e2bdf75eac80cf38b`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.6 MB (3551173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554db7c08a0e27d6cae88b0214e8b54b679a151ee920c15c7cc551bba9dbe8db`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:3c5fd2df54d8963f534234798ffeb1aba32efb451e49857f32aff43049d1c397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ea5cfcf54fd2687dbcbd7c0d8b80e7d2c7c12455d0a11dc59115025cae75adf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (620008790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c665da7365d4d53b4c876bda24890d305a7435552a9a8d23d3bb4b20e46d4af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc6524ff49eab59fdce5378d4e8dd567adbe0fbef3cf2ea61cc645f2766466a`  
		Last Modified: Wed, 11 Dec 2024 20:30:37 GMT  
		Size: 133.9 MB (133859633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7565601d292d8e9a14f6b5efe3b771cdbd9043129838158de80eb482051d7a`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88ffcb43fa11e336a37abfa4aa70fce56a279843deb4141a3ab82d42e875bac`  
		Last Modified: Wed, 11 Dec 2024 20:30:42 GMT  
		Size: 446.7 MB (446719796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:aab5f73a2efb5b56430ca015f2cda43f62f52528ee9ec342b391d56b484ee1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027039802db0b73abdf28b8819b0a5db0b40d1b436a3c5a7585854f76a03380c`

```dockerfile
```

-	Layers:
	-	`sha256:b9903fecd8bbac4e56beb432601f0786b2faf9eba461cf34bf4f90642a279235`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 6.7 MB (6711329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80362427837bd120a6f4e803d44ca5ba1331f4c0e5260c692cb699febf5bc156`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 20.6 KB (20588 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0082eef4d95f0ce597227e2e19fdbbf01d2dc21adbcb58701837caadc6c8c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.2 MB (618219110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d88e2b4e12af2d3cc2f6301d04b390ebc5a171674f6b826c34e73dcfeebb599`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e3709cf841bc19ef451c077eafcac2a0d807b9aaff5f0c93e1c588e92b4e66`  
		Last Modified: Wed, 11 Dec 2024 20:51:01 GMT  
		Size: 446.7 MB (446719834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17082a1854941eb3148276237e9ab494263ab1a37e5d7386e7f6fbe052ff75ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6711595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe04d39a37f9c52a4d1956cc73bd4531156724bd66d699e9fefb9dc4844061e`

```dockerfile
```

-	Layers:
	-	`sha256:c1b2002ab188c60f328786069d783605ed0f7435250b720b4f661ce812332ecd`  
		Last Modified: Wed, 11 Dec 2024 20:50:52 GMT  
		Size: 6.7 MB (6690894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53facf7f437fd7125aaed6899ff4dc092806bbfde05b9450749ecd797aa87baa`  
		Last Modified: Wed, 11 Dec 2024 20:50:51 GMT  
		Size: 20.7 KB (20701 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-ubi9`

```console
$ docker pull neo4j@sha256:8ca1b48108451dc79dc78280471143e98e4f42761bf0352c4d40ecacddd971f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3a07d4c3514a3a140209179bbc989ae6dcfe2221926e81c6b0278fcc69ec11bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332261595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c61a88c53b2d3ccad523075dd77353a4ec3cbffb564ee108d22309ed6e7878`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb449271df182b23f612d36d13b2e3fbeb7c8b1b801a03c4836b8879acd3c2d`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 133.9 MB (133857635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4271fb21b47adc8526a5203c5a0ac7cfa91a8482d7ecd0019f00460de4f6a`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d08690d60e34b502dd155f05d369a0b7e05f59e570cfe7340653f84b5cd2ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 159.0 MB (158974600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5b7cea601a7170bc77285f257cbb01968e70faf65984d8b914c4ef0da18bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6420457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df82eb069e58c33116ff7dd217664c7df6d7fe96a27d4219a3bddb47954c82`

```dockerfile
```

-	Layers:
	-	`sha256:c5dbe9e0cd47923c10317270d46d877e20c83c036267038f63379a751c56e736`  
		Last Modified: Wed, 11 Dec 2024 20:30:21 GMT  
		Size: 6.4 MB (6398690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857345cd65c672d5a9f26c7182964ed1b8ad7101683a9bce8bd5ea22237f08ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:41b127d076695b95d714b8d7e9a1c12bac2ea34eb4f7919be5cf643cd90fe849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330473904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b0209c870dd34862be29fdb99607414d532f07a600e3ecd9306d537deff00a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec867fd87e18f223055f7512b18b0403db034a194bc9eaf4e9fe8dcb6398010`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 159.0 MB (158974628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e93c85ec2fd0ac6c21f5cb6658ceca7f3c3b7156d6ca2c0bcdbd31e1f2fedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac93d9ae9358b1959a3a49541df90a2f94f3dea762cf6a2533203e6da32aa480`

```dockerfile
```

-	Layers:
	-	`sha256:1fd3c7e653a94849d95f1d07a42e4b60bf1dba88b7a7718ba1e4e1578e7e84c3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 6.4 MB (6378303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d3591854f94c9463c485dab703af1b00d944ee9e86d246a1304499197be158`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:8ca1b48108451dc79dc78280471143e98e4f42761bf0352c4d40ecacddd971f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3a07d4c3514a3a140209179bbc989ae6dcfe2221926e81c6b0278fcc69ec11bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332261595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c61a88c53b2d3ccad523075dd77353a4ec3cbffb564ee108d22309ed6e7878`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb449271df182b23f612d36d13b2e3fbeb7c8b1b801a03c4836b8879acd3c2d`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 133.9 MB (133857635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4271fb21b47adc8526a5203c5a0ac7cfa91a8482d7ecd0019f00460de4f6a`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d08690d60e34b502dd155f05d369a0b7e05f59e570cfe7340653f84b5cd2ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 159.0 MB (158974600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5b7cea601a7170bc77285f257cbb01968e70faf65984d8b914c4ef0da18bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6420457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df82eb069e58c33116ff7dd217664c7df6d7fe96a27d4219a3bddb47954c82`

```dockerfile
```

-	Layers:
	-	`sha256:c5dbe9e0cd47923c10317270d46d877e20c83c036267038f63379a751c56e736`  
		Last Modified: Wed, 11 Dec 2024 20:30:21 GMT  
		Size: 6.4 MB (6398690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857345cd65c672d5a9f26c7182964ed1b8ad7101683a9bce8bd5ea22237f08ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:41b127d076695b95d714b8d7e9a1c12bac2ea34eb4f7919be5cf643cd90fe849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330473904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b0209c870dd34862be29fdb99607414d532f07a600e3ecd9306d537deff00a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec867fd87e18f223055f7512b18b0403db034a194bc9eaf4e9fe8dcb6398010`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 159.0 MB (158974628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e93c85ec2fd0ac6c21f5cb6658ceca7f3c3b7156d6ca2c0bcdbd31e1f2fedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac93d9ae9358b1959a3a49541df90a2f94f3dea762cf6a2533203e6da32aa480`

```dockerfile
```

-	Layers:
	-	`sha256:1fd3c7e653a94849d95f1d07a42e4b60bf1dba88b7a7718ba1e4e1578e7e84c3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 6.4 MB (6378303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d3591854f94c9463c485dab703af1b00d944ee9e86d246a1304499197be158`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:cc0383c2422befc8f18436e4d0ac10ccb1ec8dfaa1059274e4b1c8ef68a88f6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1a344bec7aa22801f8161da45e9315cbd0ee675bf609a0c2bcd818a16884c1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624452280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd37cb1e2f9ee6b72c807625151e3df1cb69ffca720b1765bf37ecaa8b2669`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7883af60572206c2c155ee75ad9f7cbbdabb1bf196d91d8c9cf5fd5e433b0d8`  
		Last Modified: Mon, 09 Dec 2024 19:31:42 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072cd16f67817e8bb1fe9b546bb6203d98bcc057ec858a31dc1a7186aa5eadd6`  
		Last Modified: Mon, 09 Dec 2024 19:31:46 GMT  
		Size: 449.6 MB (449649015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4d3109bfd5bf5c2ecd5ed1986162d5e07708e674e166a1e9b512288cd0b8658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9687a9804b3faaa31901ca5a6dffb282b33c9ccb810d8d1f5a257f930e63238`

```dockerfile
```

-	Layers:
	-	`sha256:6d86386f6a77721f37a1fdbe3095922982a5432bb50c68c1cf008396d17b62c6`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 3.6 MB (3551481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950fe4bcedc78eb5f67fb4c0b87ef9c1018819ab9b740e4e7789fd69896ff0ef`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9a9e36ad05c7acc4f53c377b7af0c3e5fd2292406304b2ca780dd6613f3a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621734165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9306b866e1458428b58ca461cad204812e23659a768aa100e3f06a6fdc203d44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e66b4604c710e62a04b89e80fb806ac571b28e00c8337016b9b3870852110`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58037f66f958514fd05b12544c5c499cdecff55b3f2ed3dbca9b6b6032247f3`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7097958692f8fbd70eb15887b22d3dfb26b7d54c8b4c7bfb36ea4e4fb49b045`  
		Last Modified: Tue, 10 Dec 2024 01:20:40 GMT  
		Size: 449.6 MB (449614350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b729c49bee0ba5de19eb0cf8d34cc0151c8de41effb0fd089911585d0a0efc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda59757c40e04ee6d376740096190ff94b64fd2efa6b0702f402b59a3bbe0ad`

```dockerfile
```

-	Layers:
	-	`sha256:36090a5a4c81d065885cb3b7dd3108cc3dcd1bf90af68e9e2bdf75eac80cf38b`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.6 MB (3551173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554db7c08a0e27d6cae88b0214e8b54b679a151ee920c15c7cc551bba9dbe8db`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:cc0383c2422befc8f18436e4d0ac10ccb1ec8dfaa1059274e4b1c8ef68a88f6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:1a344bec7aa22801f8161da45e9315cbd0ee675bf609a0c2bcd818a16884c1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.5 MB (624452280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd37cb1e2f9ee6b72c807625151e3df1cb69ffca720b1765bf37ecaa8b2669`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7883af60572206c2c155ee75ad9f7cbbdabb1bf196d91d8c9cf5fd5e433b0d8`  
		Last Modified: Mon, 09 Dec 2024 19:31:42 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072cd16f67817e8bb1fe9b546bb6203d98bcc057ec858a31dc1a7186aa5eadd6`  
		Last Modified: Mon, 09 Dec 2024 19:31:46 GMT  
		Size: 449.6 MB (449649015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:4d3109bfd5bf5c2ecd5ed1986162d5e07708e674e166a1e9b512288cd0b8658e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9687a9804b3faaa31901ca5a6dffb282b33c9ccb810d8d1f5a257f930e63238`

```dockerfile
```

-	Layers:
	-	`sha256:6d86386f6a77721f37a1fdbe3095922982a5432bb50c68c1cf008396d17b62c6`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 3.6 MB (3551481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950fe4bcedc78eb5f67fb4c0b87ef9c1018819ab9b740e4e7789fd69896ff0ef`  
		Last Modified: Mon, 09 Dec 2024 19:31:40 GMT  
		Size: 21.4 KB (21384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f9a9e36ad05c7acc4f53c377b7af0c3e5fd2292406304b2ca780dd6613f3a63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.7 MB (621734165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9306b866e1458428b58ca461cad204812e23659a768aa100e3f06a6fdc203d44`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430e66b4604c710e62a04b89e80fb806ac571b28e00c8337016b9b3870852110`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58037f66f958514fd05b12544c5c499cdecff55b3f2ed3dbca9b6b6032247f3`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7097958692f8fbd70eb15887b22d3dfb26b7d54c8b4c7bfb36ea4e4fb49b045`  
		Last Modified: Tue, 10 Dec 2024 01:20:40 GMT  
		Size: 449.6 MB (449614350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b729c49bee0ba5de19eb0cf8d34cc0151c8de41effb0fd089911585d0a0efc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda59757c40e04ee6d376740096190ff94b64fd2efa6b0702f402b59a3bbe0ad`

```dockerfile
```

-	Layers:
	-	`sha256:36090a5a4c81d065885cb3b7dd3108cc3dcd1bf90af68e9e2bdf75eac80cf38b`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 3.6 MB (3551173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554db7c08a0e27d6cae88b0214e8b54b679a151ee920c15c7cc551bba9dbe8db`  
		Last Modified: Tue, 10 Dec 2024 01:20:31 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:3c5fd2df54d8963f534234798ffeb1aba32efb451e49857f32aff43049d1c397
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ea5cfcf54fd2687dbcbd7c0d8b80e7d2c7c12455d0a11dc59115025cae75adf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (620008790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c665da7365d4d53b4c876bda24890d305a7435552a9a8d23d3bb4b20e46d4af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc6524ff49eab59fdce5378d4e8dd567adbe0fbef3cf2ea61cc645f2766466a`  
		Last Modified: Wed, 11 Dec 2024 20:30:37 GMT  
		Size: 133.9 MB (133859633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7565601d292d8e9a14f6b5efe3b771cdbd9043129838158de80eb482051d7a`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88ffcb43fa11e336a37abfa4aa70fce56a279843deb4141a3ab82d42e875bac`  
		Last Modified: Wed, 11 Dec 2024 20:30:42 GMT  
		Size: 446.7 MB (446719796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:aab5f73a2efb5b56430ca015f2cda43f62f52528ee9ec342b391d56b484ee1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6731917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027039802db0b73abdf28b8819b0a5db0b40d1b436a3c5a7585854f76a03380c`

```dockerfile
```

-	Layers:
	-	`sha256:b9903fecd8bbac4e56beb432601f0786b2faf9eba461cf34bf4f90642a279235`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 6.7 MB (6711329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80362427837bd120a6f4e803d44ca5ba1331f4c0e5260c692cb699febf5bc156`  
		Last Modified: Wed, 11 Dec 2024 20:30:35 GMT  
		Size: 20.6 KB (20588 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0082eef4d95f0ce597227e2e19fdbbf01d2dc21adbcb58701837caadc6c8c76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.2 MB (618219110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d88e2b4e12af2d3cc2f6301d04b390ebc5a171674f6b826c34e73dcfeebb599`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=6a753836adb5bd3a355a32a8f0b1c4dd5509aeba22c50a027be1e0e9553175e8 NEO4J_TARBALL=neo4j-enterprise-5.26.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e3709cf841bc19ef451c077eafcac2a0d807b9aaff5f0c93e1c588e92b4e66`  
		Last Modified: Wed, 11 Dec 2024 20:51:01 GMT  
		Size: 446.7 MB (446719834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17082a1854941eb3148276237e9ab494263ab1a37e5d7386e7f6fbe052ff75ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6711595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe04d39a37f9c52a4d1956cc73bd4531156724bd66d699e9fefb9dc4844061e`

```dockerfile
```

-	Layers:
	-	`sha256:c1b2002ab188c60f328786069d783605ed0f7435250b720b4f661ce812332ecd`  
		Last Modified: Wed, 11 Dec 2024 20:50:52 GMT  
		Size: 6.7 MB (6690894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53facf7f437fd7125aaed6899ff4dc092806bbfde05b9450749ecd797aa87baa`  
		Last Modified: Wed, 11 Dec 2024 20:50:51 GMT  
		Size: 20.7 KB (20701 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:e50d0b04e9260586712d7012a98d6286e4502a0a9666c5a791e20c9ccbbfb7a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:02633a43403034a5afb4100d7247ec2d079033e3160bc4d1cfd14c082fccf04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336709103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56fc1cd06f8d3d98493ca3c766abd99ae31b54fb93fcb24691686206ae3abaa`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc7c3bf219b42e1f7dc7a54f62d871e89aa54d602f02deb175836f67e361e49`  
		Last Modified: Mon, 09 Dec 2024 19:30:20 GMT  
		Size: 144.5 MB (144536717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b5abf1ce4d7728aedb7ce4de0cc2c2abb229ce17077f51925eac80a12b985f`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9b7e56f432347055dca1b04aef25e0c2bdf2387c813da8cedcbe4b40acda61`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c967aced981bbbe9e9b3d4dddfb2d60224f18967729394899c95bc3a6357e684`  
		Last Modified: Mon, 09 Dec 2024 19:30:19 GMT  
		Size: 161.9 MB (161905837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:eaace86f18640e810d24bbdab603f2058f728d8e5974e7d14770c1e6e8966255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef28ecd4a7406d0c80948ea86e709b97d2b02eb82e589e1f0ea34ace060a`

```dockerfile
```

-	Layers:
	-	`sha256:5e46689ef7f40097b9be730733bdb2b9303d95869d0da0ee79972fa4318d3b9a`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 3.2 MB (3240036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf07a126391c6e133a1b609452158e657752952f664d2f38f26a731e6b7cbb69`  
		Last Modified: Mon, 09 Dec 2024 19:30:17 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:76c831f4f25c17c3b918929393ba3b25ea93c370c4e36704274d0fbd8a6d155f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (333991480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6121a8df7d035321e7c7278d3f4c7abc618d02fccf9a658c3b85de0773685016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Mon, 09 Dec 2024 12:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Dec 2024 12:11:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97953d382f74c35ee9b998b2e17face64959d8bb79a94b000c0cc96532f4f5`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f0b8e86b5d7f2bc31c4529126716bded86d762f6784cb719e8d436d3e72e68`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b7f8af4e95ea2dfd7983ba3ee0fd5135f08da605a71af15b8af3f9636c6079`  
		Last Modified: Tue, 10 Dec 2024 00:24:16 GMT  
		Size: 161.9 MB (161871671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:86b605ab9b785f50b861c56fbefb598e5e4ac89d34256dfd870a037a7dc7a555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3263866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b95b9e7ee6985ba0edb504a56fb6304ec321887e58ab40eaf1180a9a651f27`

```dockerfile
```

-	Layers:
	-	`sha256:2962ccadae4cab7e6bfaac01be567b3b37c28faf41d23a852a4435a600e51cd1`  
		Last Modified: Tue, 10 Dec 2024 00:24:12 GMT  
		Size: 3.2 MB (3239824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c30e052637eb7754b10db1440d1baf09de5dbd9296303c575d32d9febf9e3fc8`  
		Last Modified: Tue, 10 Dec 2024 00:24:11 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:8ca1b48108451dc79dc78280471143e98e4f42761bf0352c4d40ecacddd971f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3a07d4c3514a3a140209179bbc989ae6dcfe2221926e81c6b0278fcc69ec11bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332261595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c61a88c53b2d3ccad523075dd77353a4ec3cbffb564ee108d22309ed6e7878`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:ce392e97b0a18d36dffa0c783a840f3ab28026ae011aa3a1855943fa61c597d8 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:15:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:8afba38a614e150d5cec9d32c41bedfe2fe3cc1a11fbd33c712e10abb9e65de9`  
		Last Modified: Mon, 09 Dec 2024 19:12:44 GMT  
		Size: 39.4 MB (39419294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb449271df182b23f612d36d13b2e3fbeb7c8b1b801a03c4836b8879acd3c2d`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 133.9 MB (133857635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c4271fb21b47adc8526a5203c5a0ac7cfa91a8482d7ecd0019f00460de4f6a`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d08690d60e34b502dd155f05d369a0b7e05f59e570cfe7340653f84b5cd2ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:25 GMT  
		Size: 159.0 MB (158974600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:d5b7cea601a7170bc77285f257cbb01968e70faf65984d8b914c4ef0da18bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6420457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59df82eb069e58c33116ff7dd217664c7df6d7fe96a27d4219a3bddb47954c82`

```dockerfile
```

-	Layers:
	-	`sha256:c5dbe9e0cd47923c10317270d46d877e20c83c036267038f63379a751c56e736`  
		Last Modified: Wed, 11 Dec 2024 20:30:21 GMT  
		Size: 6.4 MB (6398690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857345cd65c672d5a9f26c7182964ed1b8ad7101683a9bce8bd5ea22237f08ac`  
		Last Modified: Wed, 11 Dec 2024 20:30:20 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:41b127d076695b95d714b8d7e9a1c12bac2ea34eb4f7919be5cf643cd90fe849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.5 MB (330473904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b0209c870dd34862be29fdb99607414d532f07a600e3ecd9306d537deff00a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL url="https://www.redhat.com"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 09 Dec 2024 12:11:17 GMT
ENV container oci
# Mon, 09 Dec 2024 12:11:17 GMT
COPY dir:bb4d3e8bf66b9361ce2c66099dbb4009a49deed7f655ac787c49d395bf0c8ed0 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-09T18:18:20" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="fee5a8f3e74ac2340dca04210f5456952058c9f4" "build-date"="2024-12-09T18:11:07Z" "release"="1733767867"
# Mon, 09 Dec 2024 12:11:17 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV NEO4J_SHA256=ad8ac3398606145502b8f489530bbd39333707ae4668156af16b6086b5b037d7 NEO4J_TARBALL=neo4j-community-5.26.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 09 Dec 2024 12:11:17 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
# Mon, 09 Dec 2024 12:11:17 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 09 Dec 2024 12:11:17 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Dec 2024 12:11:17 GMT
WORKDIR /var/lib/neo4j
# Mon, 09 Dec 2024 12:11:17 GMT
VOLUME [/data /logs]
# Mon, 09 Dec 2024 12:11:17 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 09 Dec 2024 12:11:17 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0ed94f65e4fba4435c4119e46186c8cd6e06d97d466980566e3061cc1a6a19a2`  
		Last Modified: Mon, 09 Dec 2024 21:46:51 GMT  
		Size: 37.6 MB (37647525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593921b4b3e233bcf9a4b5306a9d67552d00745c999c268a3ffb643320ef225`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 133.8 MB (133841686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f45d57934768c57b0731c02ad2ecb26ff73af69c6950a1b7274001686bbaf3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 10.0 KB (10033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec867fd87e18f223055f7512b18b0403db034a194bc9eaf4e9fe8dcb6398010`  
		Last Modified: Wed, 11 Dec 2024 20:49:57 GMT  
		Size: 159.0 MB (158974628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5e93c85ec2fd0ac6c21f5cb6658ceca7f3c3b7156d6ca2c0bcdbd31e1f2fedab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6400231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac93d9ae9358b1959a3a49541df90a2f94f3dea762cf6a2533203e6da32aa480`

```dockerfile
```

-	Layers:
	-	`sha256:1fd3c7e653a94849d95f1d07a42e4b60bf1dba88b7a7718ba1e4e1578e7e84c3`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 6.4 MB (6378303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67d3591854f94c9463c485dab703af1b00d944ee9e86d246a1304499197be158`  
		Last Modified: Wed, 11 Dec 2024 20:49:53 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json
