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
$ docker pull neo4j@sha256:1d436532c2047cc428182167744b0ae07c59c1eb9d894af5e594a5ae05fe8e1b
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
$ docker pull neo4j@sha256:28b2390c4dc319f6c3079cf689347fc46a07952be528a89ba7398592df8fa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315200080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ad5378f72b900be490874e2d9a9f20582eb5efda43d7d2ac30e13eed4ed6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4f7fdfab7981c1fd1ce39b349e6d2283d10dcdfcc3a26cdfaec40e92c2f974`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f45aef30b574f2766fa472920f01b410f5ce42f2abaf1e7ad36071d2ce4e0b`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5984a007343e4980cef2a376e94f816e0f476d5ba2ce5a7c5ba4d16513562`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.1 MB (143080277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:3094943aea8f9bc29afdf481ceed9a6790568472d2c0cd93d8d075f217bc5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648ee22f153335283ee2269f8b880b1831c2531435101b2c211b83f92612000`

```dockerfile
```

-	Layers:
	-	`sha256:12bafcaeb8940310546c17937b3a1f821c7ec053efd59d8557d573cbb90e9c95`  
		Last Modified: Tue, 03 Dec 2024 13:58:16 GMT  
		Size: 3.2 MB (3238459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1251aff1ae04b8aac0ad07793e7d21a39b29b2e5795fa6a4d27d6e0c398b85a`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:1d436532c2047cc428182167744b0ae07c59c1eb9d894af5e594a5ae05fe8e1b
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
$ docker pull neo4j@sha256:28b2390c4dc319f6c3079cf689347fc46a07952be528a89ba7398592df8fa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315200080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ad5378f72b900be490874e2d9a9f20582eb5efda43d7d2ac30e13eed4ed6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4f7fdfab7981c1fd1ce39b349e6d2283d10dcdfcc3a26cdfaec40e92c2f974`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f45aef30b574f2766fa472920f01b410f5ce42f2abaf1e7ad36071d2ce4e0b`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5984a007343e4980cef2a376e94f816e0f476d5ba2ce5a7c5ba4d16513562`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.1 MB (143080277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3094943aea8f9bc29afdf481ceed9a6790568472d2c0cd93d8d075f217bc5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648ee22f153335283ee2269f8b880b1831c2531435101b2c211b83f92612000`

```dockerfile
```

-	Layers:
	-	`sha256:12bafcaeb8940310546c17937b3a1f821c7ec053efd59d8557d573cbb90e9c95`  
		Last Modified: Tue, 03 Dec 2024 13:58:16 GMT  
		Size: 3.2 MB (3238459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1251aff1ae04b8aac0ad07793e7d21a39b29b2e5795fa6a4d27d6e0c398b85a`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:1d436532c2047cc428182167744b0ae07c59c1eb9d894af5e594a5ae05fe8e1b
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
$ docker pull neo4j@sha256:28b2390c4dc319f6c3079cf689347fc46a07952be528a89ba7398592df8fa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315200080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ad5378f72b900be490874e2d9a9f20582eb5efda43d7d2ac30e13eed4ed6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4f7fdfab7981c1fd1ce39b349e6d2283d10dcdfcc3a26cdfaec40e92c2f974`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f45aef30b574f2766fa472920f01b410f5ce42f2abaf1e7ad36071d2ce4e0b`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5984a007343e4980cef2a376e94f816e0f476d5ba2ce5a7c5ba4d16513562`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.1 MB (143080277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:3094943aea8f9bc29afdf481ceed9a6790568472d2c0cd93d8d075f217bc5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648ee22f153335283ee2269f8b880b1831c2531435101b2c211b83f92612000`

```dockerfile
```

-	Layers:
	-	`sha256:12bafcaeb8940310546c17937b3a1f821c7ec053efd59d8557d573cbb90e9c95`  
		Last Modified: Tue, 03 Dec 2024 13:58:16 GMT  
		Size: 3.2 MB (3238459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1251aff1ae04b8aac0ad07793e7d21a39b29b2e5795fa6a4d27d6e0c398b85a`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:1d436532c2047cc428182167744b0ae07c59c1eb9d894af5e594a5ae05fe8e1b
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
$ docker pull neo4j@sha256:28b2390c4dc319f6c3079cf689347fc46a07952be528a89ba7398592df8fa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315200080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ad5378f72b900be490874e2d9a9f20582eb5efda43d7d2ac30e13eed4ed6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4f7fdfab7981c1fd1ce39b349e6d2283d10dcdfcc3a26cdfaec40e92c2f974`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f45aef30b574f2766fa472920f01b410f5ce42f2abaf1e7ad36071d2ce4e0b`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5984a007343e4980cef2a376e94f816e0f476d5ba2ce5a7c5ba4d16513562`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.1 MB (143080277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3094943aea8f9bc29afdf481ceed9a6790568472d2c0cd93d8d075f217bc5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648ee22f153335283ee2269f8b880b1831c2531435101b2c211b83f92612000`

```dockerfile
```

-	Layers:
	-	`sha256:12bafcaeb8940310546c17937b3a1f821c7ec053efd59d8557d573cbb90e9c95`  
		Last Modified: Tue, 03 Dec 2024 13:58:16 GMT  
		Size: 3.2 MB (3238459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1251aff1ae04b8aac0ad07793e7d21a39b29b2e5795fa6a4d27d6e0c398b85a`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:7b46175dfc9855c1d8f462ac381c8fa085319817f6193608c83c86aa1248e047
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f23f0f2c8ed171db712d6c05b4a94aeb3e15c0d09d70e18b2cd9bf17ae13502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332779229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f75ce9997cfc41875dd63d05141e68dbc8c4d5bd43ff561f4fafb39ee365d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9d54f5a4e3dba90c8f6065d6c1283fada3b1a4634b04e54992dd81d97f6b0`  
		Last Modified: Mon, 09 Dec 2024 19:30:34 GMT  
		Size: 133.9 MB (133856178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d645aa38ebcb276123f702a1741dca6d324dfa4ce8760e70efa3fb04edd4b750`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d2e1e8a5d7610702416d1f5ccc5f704795163edaefc57cf716f5bb184fd9f`  
		Last Modified: Mon, 09 Dec 2024 19:30:35 GMT  
		Size: 159.0 MB (158974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3a444e5f0f76de96049308674434b5ea9465cccd5e1f8656b843d65ddf6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c94faa2f1d9c0b5679f5b6875eac038c7f2d389fb7c91f7ef8d3327f0e5fce2`

```dockerfile
```

-	Layers:
	-	`sha256:04af3710b5ab86d1ed125dbd02e0dcfcf358a76174741728e75aec38d3c3933b`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 7.5 MB (7524164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b48ecd143d0baa4a6bd5d8d829c8450443443878721a532c9d0742d7a84518f`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 22.5 KB (22547 bytes)  
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
$ docker pull neo4j@sha256:231a8a2ac4a6730095fcf9d708508a5fcb833eddcbcfb6a16b93db0382e071f4
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
$ docker pull neo4j@sha256:1df2af8b8f3ee49348f6a3f5682af43f84671b1dcd1ad0268df9323616bb7c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.2 MB (604209215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8f49895a5270e9777e67808efa98bbaa7928e7eb9af5f0fc84507687f0f79d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e855bf10e113c55796b6701c030063cda3fa54bbd10a9685ba94d50075bd262`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ca5b1573156c79a11262681fd302d537128b1460631a33409a4c960f7b27d4`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7df1739716f51fed39d6e5210d94a104be8fc31fbf0bfac0c7710e73073cd9`  
		Last Modified: Tue, 03 Dec 2024 14:02:35 GMT  
		Size: 432.1 MB (432089411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc86074e86e95bf093729c8a9099f1e76b937e2672177fee40a9837362e2307d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a068df547f24698bb43073aef60e3658b8e4e63fe458051ebbb1c1fbab2edd`

```dockerfile
```

-	Layers:
	-	`sha256:7225150abacfd5e03239c24d05ce36685e9f2358844fd532f853edef53ddb8da`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 3.6 MB (3559661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79582a586689d0db32f3ac0fa978f5538aaf6db24d25e1726abcff036af07cc`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:231a8a2ac4a6730095fcf9d708508a5fcb833eddcbcfb6a16b93db0382e071f4
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
$ docker pull neo4j@sha256:1df2af8b8f3ee49348f6a3f5682af43f84671b1dcd1ad0268df9323616bb7c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.2 MB (604209215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8f49895a5270e9777e67808efa98bbaa7928e7eb9af5f0fc84507687f0f79d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e855bf10e113c55796b6701c030063cda3fa54bbd10a9685ba94d50075bd262`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ca5b1573156c79a11262681fd302d537128b1460631a33409a4c960f7b27d4`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7df1739716f51fed39d6e5210d94a104be8fc31fbf0bfac0c7710e73073cd9`  
		Last Modified: Tue, 03 Dec 2024 14:02:35 GMT  
		Size: 432.1 MB (432089411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc86074e86e95bf093729c8a9099f1e76b937e2672177fee40a9837362e2307d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a068df547f24698bb43073aef60e3658b8e4e63fe458051ebbb1c1fbab2edd`

```dockerfile
```

-	Layers:
	-	`sha256:7225150abacfd5e03239c24d05ce36685e9f2358844fd532f853edef53ddb8da`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 3.6 MB (3559661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79582a586689d0db32f3ac0fa978f5538aaf6db24d25e1726abcff036af07cc`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:b592cb8b05b248b355090ebf8dcc50800ef3c8c5ece6e18d4107a858cdad4150
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fa960ea13b7b67b47285161e939d1c94441c2466a94140b2612954b4620ed85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.5 MB (620524595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bb7ce76ac46f9f36af26bbdcc92c1c45016e5494a1f9600950f9cbfab58b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a008bc859acefbb69269ca0266e1a84588a4583f0f5d35c04607c2ac02ae85b`  
		Last Modified: Mon, 09 Dec 2024 19:32:07 GMT  
		Size: 133.9 MB (133856413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6704cd9b2a2505a59b039f7c119fda70df737330cdbdd60a8ac6537fc4497e85`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9afc23533a5edd76dababc2bf4b1f3d5d6eaddb8df2925ead0e4aad42ab1aa`  
		Last Modified: Mon, 09 Dec 2024 19:32:16 GMT  
		Size: 446.7 MB (446719781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a126cbd0243c9887ea00278c65ac3f2a38811f5124cde205ba4b433aee905285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7858170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767071c9ac5277017ad9a448e414221092bccc6713cc65b99f36e803d53bcb87`

```dockerfile
```

-	Layers:
	-	`sha256:ae39eeade411229d9a707066f10298d5dc65558f7ca2cf7943598fa81e218f96`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 7.8 MB (7836803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:754275e5825d2b04e5615af60d375644a117229dda2b443a062bde68068d0e4a`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 21.4 KB (21367 bytes)  
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
$ docker pull neo4j@sha256:7b46175dfc9855c1d8f462ac381c8fa085319817f6193608c83c86aa1248e047
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f23f0f2c8ed171db712d6c05b4a94aeb3e15c0d09d70e18b2cd9bf17ae13502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332779229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f75ce9997cfc41875dd63d05141e68dbc8c4d5bd43ff561f4fafb39ee365d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9d54f5a4e3dba90c8f6065d6c1283fada3b1a4634b04e54992dd81d97f6b0`  
		Last Modified: Mon, 09 Dec 2024 19:30:34 GMT  
		Size: 133.9 MB (133856178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d645aa38ebcb276123f702a1741dca6d324dfa4ce8760e70efa3fb04edd4b750`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d2e1e8a5d7610702416d1f5ccc5f704795163edaefc57cf716f5bb184fd9f`  
		Last Modified: Mon, 09 Dec 2024 19:30:35 GMT  
		Size: 159.0 MB (158974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3a444e5f0f76de96049308674434b5ea9465cccd5e1f8656b843d65ddf6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c94faa2f1d9c0b5679f5b6875eac038c7f2d389fb7c91f7ef8d3327f0e5fce2`

```dockerfile
```

-	Layers:
	-	`sha256:04af3710b5ab86d1ed125dbd02e0dcfcf358a76174741728e75aec38d3c3933b`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 7.5 MB (7524164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b48ecd143d0baa4a6bd5d8d829c8450443443878721a532c9d0742d7a84518f`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 22.5 KB (22547 bytes)  
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

## `neo4j:5.26`

```console
$ docker pull neo4j@sha256:d8e4872e5b33b5d561fa8e4c06c72b90031990f52a1db12e460d9cb39a383b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26-bullseye`

```console
$ docker pull neo4j@sha256:d8e4872e5b33b5d561fa8e4c06c72b90031990f52a1db12e460d9cb39a383b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26-community`

```console
$ docker pull neo4j@sha256:d8e4872e5b33b5d561fa8e4c06c72b90031990f52a1db12e460d9cb39a383b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26-community-bullseye`

```console
$ docker pull neo4j@sha256:d8e4872e5b33b5d561fa8e4c06c72b90031990f52a1db12e460d9cb39a383b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26-community-ubi9`

```console
$ docker pull neo4j@sha256:c254bb0284aba883306f63f427fda58246360bfc067b4f08f71c95c02a902f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `neo4j:5.26-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f23f0f2c8ed171db712d6c05b4a94aeb3e15c0d09d70e18b2cd9bf17ae13502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332779229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f75ce9997cfc41875dd63d05141e68dbc8c4d5bd43ff561f4fafb39ee365d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9d54f5a4e3dba90c8f6065d6c1283fada3b1a4634b04e54992dd81d97f6b0`  
		Last Modified: Mon, 09 Dec 2024 19:30:34 GMT  
		Size: 133.9 MB (133856178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d645aa38ebcb276123f702a1741dca6d324dfa4ce8760e70efa3fb04edd4b750`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d2e1e8a5d7610702416d1f5ccc5f704795163edaefc57cf716f5bb184fd9f`  
		Last Modified: Mon, 09 Dec 2024 19:30:35 GMT  
		Size: 159.0 MB (158974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3a444e5f0f76de96049308674434b5ea9465cccd5e1f8656b843d65ddf6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c94faa2f1d9c0b5679f5b6875eac038c7f2d389fb7c91f7ef8d3327f0e5fce2`

```dockerfile
```

-	Layers:
	-	`sha256:04af3710b5ab86d1ed125dbd02e0dcfcf358a76174741728e75aec38d3c3933b`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 7.5 MB (7524164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b48ecd143d0baa4a6bd5d8d829c8450443443878721a532c9d0742d7a84518f`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-enterprise`

```console
$ docker pull neo4j@sha256:2a969721e5341d43a5eed7f9544020fb59956298fdcdea5cd9f1c1887dcac6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:2a969721e5341d43a5eed7f9544020fb59956298fdcdea5cd9f1c1887dcac6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:ebc978ab61d8ad6bd9f3c820bc147105f594360cb88b87e4c4ee495cdab0c735
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `neo4j:5.26-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fa960ea13b7b67b47285161e939d1c94441c2466a94140b2612954b4620ed85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.5 MB (620524595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bb7ce76ac46f9f36af26bbdcc92c1c45016e5494a1f9600950f9cbfab58b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a008bc859acefbb69269ca0266e1a84588a4583f0f5d35c04607c2ac02ae85b`  
		Last Modified: Mon, 09 Dec 2024 19:32:07 GMT  
		Size: 133.9 MB (133856413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6704cd9b2a2505a59b039f7c119fda70df737330cdbdd60a8ac6537fc4497e85`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9afc23533a5edd76dababc2bf4b1f3d5d6eaddb8df2925ead0e4aad42ab1aa`  
		Last Modified: Mon, 09 Dec 2024 19:32:16 GMT  
		Size: 446.7 MB (446719781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a126cbd0243c9887ea00278c65ac3f2a38811f5124cde205ba4b433aee905285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7858170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767071c9ac5277017ad9a448e414221092bccc6713cc65b99f36e803d53bcb87`

```dockerfile
```

-	Layers:
	-	`sha256:ae39eeade411229d9a707066f10298d5dc65558f7ca2cf7943598fa81e218f96`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 7.8 MB (7836803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:754275e5825d2b04e5615af60d375644a117229dda2b443a062bde68068d0e4a`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 21.4 KB (21367 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-ubi9`

```console
$ docker pull neo4j@sha256:c254bb0284aba883306f63f427fda58246360bfc067b4f08f71c95c02a902f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `neo4j:5.26-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f23f0f2c8ed171db712d6c05b4a94aeb3e15c0d09d70e18b2cd9bf17ae13502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332779229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f75ce9997cfc41875dd63d05141e68dbc8c4d5bd43ff561f4fafb39ee365d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9d54f5a4e3dba90c8f6065d6c1283fada3b1a4634b04e54992dd81d97f6b0`  
		Last Modified: Mon, 09 Dec 2024 19:30:34 GMT  
		Size: 133.9 MB (133856178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d645aa38ebcb276123f702a1741dca6d324dfa4ce8760e70efa3fb04edd4b750`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d2e1e8a5d7610702416d1f5ccc5f704795163edaefc57cf716f5bb184fd9f`  
		Last Modified: Mon, 09 Dec 2024 19:30:35 GMT  
		Size: 159.0 MB (158974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3a444e5f0f76de96049308674434b5ea9465cccd5e1f8656b843d65ddf6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c94faa2f1d9c0b5679f5b6875eac038c7f2d389fb7c91f7ef8d3327f0e5fce2`

```dockerfile
```

-	Layers:
	-	`sha256:04af3710b5ab86d1ed125dbd02e0dcfcf358a76174741728e75aec38d3c3933b`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 7.5 MB (7524164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b48ecd143d0baa4a6bd5d8d829c8450443443878721a532c9d0742d7a84518f`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0`

```console
$ docker pull neo4j@sha256:d8e4872e5b33b5d561fa8e4c06c72b90031990f52a1db12e460d9cb39a383b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26.0-bullseye`

```console
$ docker pull neo4j@sha256:d8e4872e5b33b5d561fa8e4c06c72b90031990f52a1db12e460d9cb39a383b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26.0-community`

```console
$ docker pull neo4j@sha256:d8e4872e5b33b5d561fa8e4c06c72b90031990f52a1db12e460d9cb39a383b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26.0-community-bullseye`

```console
$ docker pull neo4j@sha256:d8e4872e5b33b5d561fa8e4c06c72b90031990f52a1db12e460d9cb39a383b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26.0-community-ubi9`

```console
$ docker pull neo4j@sha256:c254bb0284aba883306f63f427fda58246360bfc067b4f08f71c95c02a902f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `neo4j:5.26.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f23f0f2c8ed171db712d6c05b4a94aeb3e15c0d09d70e18b2cd9bf17ae13502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332779229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f75ce9997cfc41875dd63d05141e68dbc8c4d5bd43ff561f4fafb39ee365d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9d54f5a4e3dba90c8f6065d6c1283fada3b1a4634b04e54992dd81d97f6b0`  
		Last Modified: Mon, 09 Dec 2024 19:30:34 GMT  
		Size: 133.9 MB (133856178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d645aa38ebcb276123f702a1741dca6d324dfa4ce8760e70efa3fb04edd4b750`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d2e1e8a5d7610702416d1f5ccc5f704795163edaefc57cf716f5bb184fd9f`  
		Last Modified: Mon, 09 Dec 2024 19:30:35 GMT  
		Size: 159.0 MB (158974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3a444e5f0f76de96049308674434b5ea9465cccd5e1f8656b843d65ddf6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c94faa2f1d9c0b5679f5b6875eac038c7f2d389fb7c91f7ef8d3327f0e5fce2`

```dockerfile
```

-	Layers:
	-	`sha256:04af3710b5ab86d1ed125dbd02e0dcfcf358a76174741728e75aec38d3c3933b`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 7.5 MB (7524164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b48ecd143d0baa4a6bd5d8d829c8450443443878721a532c9d0742d7a84518f`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-enterprise`

```console
$ docker pull neo4j@sha256:2a969721e5341d43a5eed7f9544020fb59956298fdcdea5cd9f1c1887dcac6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:2a969721e5341d43a5eed7f9544020fb59956298fdcdea5cd9f1c1887dcac6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
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

## `neo4j:5.26.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:ebc978ab61d8ad6bd9f3c820bc147105f594360cb88b87e4c4ee495cdab0c735
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `neo4j:5.26.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fa960ea13b7b67b47285161e939d1c94441c2466a94140b2612954b4620ed85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.5 MB (620524595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bb7ce76ac46f9f36af26bbdcc92c1c45016e5494a1f9600950f9cbfab58b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a008bc859acefbb69269ca0266e1a84588a4583f0f5d35c04607c2ac02ae85b`  
		Last Modified: Mon, 09 Dec 2024 19:32:07 GMT  
		Size: 133.9 MB (133856413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6704cd9b2a2505a59b039f7c119fda70df737330cdbdd60a8ac6537fc4497e85`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9afc23533a5edd76dababc2bf4b1f3d5d6eaddb8df2925ead0e4aad42ab1aa`  
		Last Modified: Mon, 09 Dec 2024 19:32:16 GMT  
		Size: 446.7 MB (446719781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a126cbd0243c9887ea00278c65ac3f2a38811f5124cde205ba4b433aee905285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7858170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767071c9ac5277017ad9a448e414221092bccc6713cc65b99f36e803d53bcb87`

```dockerfile
```

-	Layers:
	-	`sha256:ae39eeade411229d9a707066f10298d5dc65558f7ca2cf7943598fa81e218f96`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 7.8 MB (7836803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:754275e5825d2b04e5615af60d375644a117229dda2b443a062bde68068d0e4a`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 21.4 KB (21367 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-ubi9`

```console
$ docker pull neo4j@sha256:c254bb0284aba883306f63f427fda58246360bfc067b4f08f71c95c02a902f75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `neo4j:5.26.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f23f0f2c8ed171db712d6c05b4a94aeb3e15c0d09d70e18b2cd9bf17ae13502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332779229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f75ce9997cfc41875dd63d05141e68dbc8c4d5bd43ff561f4fafb39ee365d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9d54f5a4e3dba90c8f6065d6c1283fada3b1a4634b04e54992dd81d97f6b0`  
		Last Modified: Mon, 09 Dec 2024 19:30:34 GMT  
		Size: 133.9 MB (133856178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d645aa38ebcb276123f702a1741dca6d324dfa4ce8760e70efa3fb04edd4b750`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d2e1e8a5d7610702416d1f5ccc5f704795163edaefc57cf716f5bb184fd9f`  
		Last Modified: Mon, 09 Dec 2024 19:30:35 GMT  
		Size: 159.0 MB (158974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3a444e5f0f76de96049308674434b5ea9465cccd5e1f8656b843d65ddf6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c94faa2f1d9c0b5679f5b6875eac038c7f2d389fb7c91f7ef8d3327f0e5fce2`

```dockerfile
```

-	Layers:
	-	`sha256:04af3710b5ab86d1ed125dbd02e0dcfcf358a76174741728e75aec38d3c3933b`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 7.5 MB (7524164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b48ecd143d0baa4a6bd5d8d829c8450443443878721a532c9d0742d7a84518f`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 22.5 KB (22547 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:1d436532c2047cc428182167744b0ae07c59c1eb9d894af5e594a5ae05fe8e1b
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
$ docker pull neo4j@sha256:28b2390c4dc319f6c3079cf689347fc46a07952be528a89ba7398592df8fa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315200080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ad5378f72b900be490874e2d9a9f20582eb5efda43d7d2ac30e13eed4ed6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4f7fdfab7981c1fd1ce39b349e6d2283d10dcdfcc3a26cdfaec40e92c2f974`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f45aef30b574f2766fa472920f01b410f5ce42f2abaf1e7ad36071d2ce4e0b`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5984a007343e4980cef2a376e94f816e0f476d5ba2ce5a7c5ba4d16513562`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.1 MB (143080277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3094943aea8f9bc29afdf481ceed9a6790568472d2c0cd93d8d075f217bc5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648ee22f153335283ee2269f8b880b1831c2531435101b2c211b83f92612000`

```dockerfile
```

-	Layers:
	-	`sha256:12bafcaeb8940310546c17937b3a1f821c7ec053efd59d8557d573cbb90e9c95`  
		Last Modified: Tue, 03 Dec 2024 13:58:16 GMT  
		Size: 3.2 MB (3238459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1251aff1ae04b8aac0ad07793e7d21a39b29b2e5795fa6a4d27d6e0c398b85a`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:1d436532c2047cc428182167744b0ae07c59c1eb9d894af5e594a5ae05fe8e1b
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
$ docker pull neo4j@sha256:28b2390c4dc319f6c3079cf689347fc46a07952be528a89ba7398592df8fa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315200080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ad5378f72b900be490874e2d9a9f20582eb5efda43d7d2ac30e13eed4ed6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4f7fdfab7981c1fd1ce39b349e6d2283d10dcdfcc3a26cdfaec40e92c2f974`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f45aef30b574f2766fa472920f01b410f5ce42f2abaf1e7ad36071d2ce4e0b`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5984a007343e4980cef2a376e94f816e0f476d5ba2ce5a7c5ba4d16513562`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.1 MB (143080277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:3094943aea8f9bc29afdf481ceed9a6790568472d2c0cd93d8d075f217bc5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648ee22f153335283ee2269f8b880b1831c2531435101b2c211b83f92612000`

```dockerfile
```

-	Layers:
	-	`sha256:12bafcaeb8940310546c17937b3a1f821c7ec053efd59d8557d573cbb90e9c95`  
		Last Modified: Tue, 03 Dec 2024 13:58:16 GMT  
		Size: 3.2 MB (3238459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1251aff1ae04b8aac0ad07793e7d21a39b29b2e5795fa6a4d27d6e0c398b85a`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:1d436532c2047cc428182167744b0ae07c59c1eb9d894af5e594a5ae05fe8e1b
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
$ docker pull neo4j@sha256:28b2390c4dc319f6c3079cf689347fc46a07952be528a89ba7398592df8fa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315200080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ad5378f72b900be490874e2d9a9f20582eb5efda43d7d2ac30e13eed4ed6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4f7fdfab7981c1fd1ce39b349e6d2283d10dcdfcc3a26cdfaec40e92c2f974`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f45aef30b574f2766fa472920f01b410f5ce42f2abaf1e7ad36071d2ce4e0b`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5984a007343e4980cef2a376e94f816e0f476d5ba2ce5a7c5ba4d16513562`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.1 MB (143080277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3094943aea8f9bc29afdf481ceed9a6790568472d2c0cd93d8d075f217bc5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648ee22f153335283ee2269f8b880b1831c2531435101b2c211b83f92612000`

```dockerfile
```

-	Layers:
	-	`sha256:12bafcaeb8940310546c17937b3a1f821c7ec053efd59d8557d573cbb90e9c95`  
		Last Modified: Tue, 03 Dec 2024 13:58:16 GMT  
		Size: 3.2 MB (3238459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1251aff1ae04b8aac0ad07793e7d21a39b29b2e5795fa6a4d27d6e0c398b85a`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:7b46175dfc9855c1d8f462ac381c8fa085319817f6193608c83c86aa1248e047
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f23f0f2c8ed171db712d6c05b4a94aeb3e15c0d09d70e18b2cd9bf17ae13502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332779229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f75ce9997cfc41875dd63d05141e68dbc8c4d5bd43ff561f4fafb39ee365d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9d54f5a4e3dba90c8f6065d6c1283fada3b1a4634b04e54992dd81d97f6b0`  
		Last Modified: Mon, 09 Dec 2024 19:30:34 GMT  
		Size: 133.9 MB (133856178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d645aa38ebcb276123f702a1741dca6d324dfa4ce8760e70efa3fb04edd4b750`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d2e1e8a5d7610702416d1f5ccc5f704795163edaefc57cf716f5bb184fd9f`  
		Last Modified: Mon, 09 Dec 2024 19:30:35 GMT  
		Size: 159.0 MB (158974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3a444e5f0f76de96049308674434b5ea9465cccd5e1f8656b843d65ddf6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c94faa2f1d9c0b5679f5b6875eac038c7f2d389fb7c91f7ef8d3327f0e5fce2`

```dockerfile
```

-	Layers:
	-	`sha256:04af3710b5ab86d1ed125dbd02e0dcfcf358a76174741728e75aec38d3c3933b`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 7.5 MB (7524164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b48ecd143d0baa4a6bd5d8d829c8450443443878721a532c9d0742d7a84518f`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 22.5 KB (22547 bytes)  
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
$ docker pull neo4j@sha256:231a8a2ac4a6730095fcf9d708508a5fcb833eddcbcfb6a16b93db0382e071f4
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
$ docker pull neo4j@sha256:1df2af8b8f3ee49348f6a3f5682af43f84671b1dcd1ad0268df9323616bb7c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.2 MB (604209215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8f49895a5270e9777e67808efa98bbaa7928e7eb9af5f0fc84507687f0f79d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e855bf10e113c55796b6701c030063cda3fa54bbd10a9685ba94d50075bd262`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ca5b1573156c79a11262681fd302d537128b1460631a33409a4c960f7b27d4`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7df1739716f51fed39d6e5210d94a104be8fc31fbf0bfac0c7710e73073cd9`  
		Last Modified: Tue, 03 Dec 2024 14:02:35 GMT  
		Size: 432.1 MB (432089411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc86074e86e95bf093729c8a9099f1e76b937e2672177fee40a9837362e2307d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a068df547f24698bb43073aef60e3658b8e4e63fe458051ebbb1c1fbab2edd`

```dockerfile
```

-	Layers:
	-	`sha256:7225150abacfd5e03239c24d05ce36685e9f2358844fd532f853edef53ddb8da`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 3.6 MB (3559661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79582a586689d0db32f3ac0fa978f5538aaf6db24d25e1726abcff036af07cc`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:231a8a2ac4a6730095fcf9d708508a5fcb833eddcbcfb6a16b93db0382e071f4
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
$ docker pull neo4j@sha256:1df2af8b8f3ee49348f6a3f5682af43f84671b1dcd1ad0268df9323616bb7c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.2 MB (604209215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8f49895a5270e9777e67808efa98bbaa7928e7eb9af5f0fc84507687f0f79d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e855bf10e113c55796b6701c030063cda3fa54bbd10a9685ba94d50075bd262`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ca5b1573156c79a11262681fd302d537128b1460631a33409a4c960f7b27d4`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7df1739716f51fed39d6e5210d94a104be8fc31fbf0bfac0c7710e73073cd9`  
		Last Modified: Tue, 03 Dec 2024 14:02:35 GMT  
		Size: 432.1 MB (432089411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:fc86074e86e95bf093729c8a9099f1e76b937e2672177fee40a9837362e2307d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a068df547f24698bb43073aef60e3658b8e4e63fe458051ebbb1c1fbab2edd`

```dockerfile
```

-	Layers:
	-	`sha256:7225150abacfd5e03239c24d05ce36685e9f2358844fd532f853edef53ddb8da`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 3.6 MB (3559661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79582a586689d0db32f3ac0fa978f5538aaf6db24d25e1726abcff036af07cc`  
		Last Modified: Tue, 03 Dec 2024 14:02:26 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:b592cb8b05b248b355090ebf8dcc50800ef3c8c5ece6e18d4107a858cdad4150
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fa960ea13b7b67b47285161e939d1c94441c2466a94140b2612954b4620ed85f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.5 MB (620524595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0bb7ce76ac46f9f36af26bbdcc92c1c45016e5494a1f9600950f9cbfab58b8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a008bc859acefbb69269ca0266e1a84588a4583f0f5d35c04607c2ac02ae85b`  
		Last Modified: Mon, 09 Dec 2024 19:32:07 GMT  
		Size: 133.9 MB (133856413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6704cd9b2a2505a59b039f7c119fda70df737330cdbdd60a8ac6537fc4497e85`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9afc23533a5edd76dababc2bf4b1f3d5d6eaddb8df2925ead0e4aad42ab1aa`  
		Last Modified: Mon, 09 Dec 2024 19:32:16 GMT  
		Size: 446.7 MB (446719781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:a126cbd0243c9887ea00278c65ac3f2a38811f5124cde205ba4b433aee905285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7858170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767071c9ac5277017ad9a448e414221092bccc6713cc65b99f36e803d53bcb87`

```dockerfile
```

-	Layers:
	-	`sha256:ae39eeade411229d9a707066f10298d5dc65558f7ca2cf7943598fa81e218f96`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 7.8 MB (7836803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:754275e5825d2b04e5615af60d375644a117229dda2b443a062bde68068d0e4a`  
		Last Modified: Mon, 09 Dec 2024 19:32:03 GMT  
		Size: 21.4 KB (21367 bytes)  
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
$ docker pull neo4j@sha256:1d436532c2047cc428182167744b0ae07c59c1eb9d894af5e594a5ae05fe8e1b
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
$ docker pull neo4j@sha256:28b2390c4dc319f6c3079cf689347fc46a07952be528a89ba7398592df8fa536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315200080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313ad5378f72b900be490874e2d9a9f20582eb5efda43d7d2ac30e13eed4ed6a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 30 Oct 2024 15:39:25 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95af4f2d579fe0d913fdf359771ac4abf601329210b5a97101e9f1020cf9a73`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.4 MB (143360957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4f7fdfab7981c1fd1ce39b349e6d2283d10dcdfcc3a26cdfaec40e92c2f974`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f45aef30b574f2766fa472920f01b410f5ce42f2abaf1e7ad36071d2ce4e0b`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 10.0 KB (10027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5984a007343e4980cef2a376e94f816e0f476d5ba2ce5a7c5ba4d16513562`  
		Last Modified: Tue, 03 Dec 2024 13:58:19 GMT  
		Size: 143.1 MB (143080277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:3094943aea8f9bc29afdf481ceed9a6790568472d2c0cd93d8d075f217bc5cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3262501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a648ee22f153335283ee2269f8b880b1831c2531435101b2c211b83f92612000`

```dockerfile
```

-	Layers:
	-	`sha256:12bafcaeb8940310546c17937b3a1f821c7ec053efd59d8557d573cbb90e9c95`  
		Last Modified: Tue, 03 Dec 2024 13:58:16 GMT  
		Size: 3.2 MB (3238459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1251aff1ae04b8aac0ad07793e7d21a39b29b2e5795fa6a4d27d6e0c398b85a`  
		Last Modified: Tue, 03 Dec 2024 13:58:15 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:7b46175dfc9855c1d8f462ac381c8fa085319817f6193608c83c86aa1248e047
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:f23f0f2c8ed171db712d6c05b4a94aeb3e15c0d09d70e18b2cd9bf17ae13502b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.8 MB (332779229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5f75ce9997cfc41875dd63d05141e68dbc8c4d5bd43ff561f4fafb39ee365d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 14 Nov 2024 14:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 14 Nov 2024 14:18:01 GMT
ENV container oci
# Thu, 14 Nov 2024 14:18:02 GMT
COPY dir:26d047f52016e2a9f64a7f20013880d3158f648f83df82762d23c38cacbb891e in / 
# Thu, 14 Nov 2024 14:18:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 14 Nov 2024 14:18:02 GMT
CMD ["/bin/bash"]
# Thu, 14 Nov 2024 14:18:03 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 14 Nov 2024 14:18:03 GMT
LABEL "build-date"="2024-11-14T14:09:46" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ed8745a7a03752cc96aedcff40c4eb3ee49117c5" "build-date"="2024-11-14T14:03:48Z" "release"="1731593028"
# Thu, 14 Nov 2024 14:18:27 GMT
RUN /bin/sh
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
	-	`sha256:3d252ab42824f0f833f0fcf3c660065bd878cb4de12b9c69b6a1758287e338e8`  
		Last Modified: Thu, 14 Nov 2024 22:57:36 GMT  
		Size: 39.9 MB (39874786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b98276ead8a9c2b7961856002e38957b2d575a92f9fe178dc86ecb063fcb219`  
		Last Modified: Thu, 14 Nov 2024 22:57:33 GMT  
		Size: 63.5 KB (63547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e9d54f5a4e3dba90c8f6065d6c1283fada3b1a4634b04e54992dd81d97f6b0`  
		Last Modified: Mon, 09 Dec 2024 19:30:34 GMT  
		Size: 133.9 MB (133856178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d645aa38ebcb276123f702a1741dca6d324dfa4ce8760e70efa3fb04edd4b750`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d2e1e8a5d7610702416d1f5ccc5f704795163edaefc57cf716f5bb184fd9f`  
		Last Modified: Mon, 09 Dec 2024 19:30:35 GMT  
		Size: 159.0 MB (158974652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0c3a444e5f0f76de96049308674434b5ea9465cccd5e1f8656b843d65ddf6c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7546711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c94faa2f1d9c0b5679f5b6875eac038c7f2d389fb7c91f7ef8d3327f0e5fce2`

```dockerfile
```

-	Layers:
	-	`sha256:04af3710b5ab86d1ed125dbd02e0dcfcf358a76174741728e75aec38d3c3933b`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 7.5 MB (7524164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b48ecd143d0baa4a6bd5d8d829c8450443443878721a532c9d0742d7a84518f`  
		Last Modified: Mon, 09 Dec 2024 19:30:33 GMT  
		Size: 22.5 KB (22547 bytes)  
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
