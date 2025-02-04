<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.41`](#neo4j4441)
-	[`neo4j:4.4.41-community`](#neo4j4441-community)
-	[`neo4j:4.4.41-enterprise`](#neo4j4441-enterprise)
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
-	[`neo4j:5.26.1`](#neo4j5261)
-	[`neo4j:5.26.1-bullseye`](#neo4j5261-bullseye)
-	[`neo4j:5.26.1-community`](#neo4j5261-community)
-	[`neo4j:5.26.1-community-bullseye`](#neo4j5261-community-bullseye)
-	[`neo4j:5.26.1-community-ubi9`](#neo4j5261-community-ubi9)
-	[`neo4j:5.26.1-enterprise`](#neo4j5261-enterprise)
-	[`neo4j:5.26.1-enterprise-bullseye`](#neo4j5261-enterprise-bullseye)
-	[`neo4j:5.26.1-enterprise-ubi9`](#neo4j5261-enterprise-ubi9)
-	[`neo4j:5.26.1-ubi9`](#neo4j5261-ubi9)
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
$ docker pull neo4j@sha256:5ed0d1dee447a0d486902aa90ec939ccbdcd008eace359fc9de82af0cec01657
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:9615ae5e6292e7d917f46bb56c6c8e52221e1013d12d2cf1a6daec226241ca73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323180380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fec7366b094bbec1f8e7cf56c5ec325770bf6462082431966ceb935eac0fe0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 17 Dec 2024 20:59:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Tue, 17 Dec 2024 20:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Dec 2024 20:59:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=329761a647bfcee9b729d09a353c4a811772a6aa6b22dad451d3d065538c3447 NEO4J_TARBALL=neo4j-community-4.4.40-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Dec 2024 20:59:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 20:59:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Dec 2024 20:59:18 GMT
VOLUME [/data /logs]
# Tue, 17 Dec 2024 20:59:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Dec 2024 20:59:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 20:59:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0ae6360091eaad78b79c7ea2cd6a187036631b60889512eb1bbeec81e87b98`  
		Last Modified: Tue, 04 Feb 2025 05:18:53 GMT  
		Size: 145.6 MB (145598914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c30ff2193724d42334f1f019ba9b00b3be0555f7428c31c8c3ecd9b040cc0`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10e7e6d970a4d5729836504061b590969d7b39b710821ce4eb4178165240038`  
		Last Modified: Tue, 04 Feb 2025 05:18:54 GMT  
		Size: 147.3 MB (147315023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:67a2bc03cca78655856d1ef55cfac08a621ea233bf184e0d7b08c376782c367a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de22f507753a98453cef138677cb43e6cf1948b4cb8a3994cf6ee76ff93a9ff9`

```dockerfile
```

-	Layers:
	-	`sha256:c1a3ae191ab6aa349c2ac75ff221b83cf9656effe0f6711df9e68eb2390f9066`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 3.2 MB (3190657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf74c20585cabe460285ea1fd886f7c0a3afa3734c4b2235a4049bb8af1039e`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3f16c5399b7aae333c7f740e940c58964bb92f0404c3483ef2baa6c7a840fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318427395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0398d8104d4a49b9ce25f2f88ae159947c21993dbc4c01c468e3e1a2c2272f24`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 17 Dec 2024 20:59:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 17 Dec 2024 20:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Dec 2024 20:59:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=329761a647bfcee9b729d09a353c4a811772a6aa6b22dad451d3d065538c3447 NEO4J_TARBALL=neo4j-community-4.4.40-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Dec 2024 20:59:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 20:59:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Dec 2024 20:59:18 GMT
VOLUME [/data /logs]
# Tue, 17 Dec 2024 20:59:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Dec 2024 20:59:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 20:59:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75f2a1647a2213cea5bd866fc62a6cb80c08c0c97a030b53f5ae8e5be7bc170`  
		Last Modified: Fri, 31 Jan 2025 03:36:23 GMT  
		Size: 142.4 MB (142385501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26800e74d4f320f8f2983d7cdda29606a285cb459688af7d0354068c4832a4fc`  
		Last Modified: Fri, 31 Jan 2025 03:36:19 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c781d3a34100b2f1b990589a48052ff0c060a35bdda82e4764f6a530c01023`  
		Last Modified: Fri, 31 Jan 2025 03:36:19 GMT  
		Size: 10.0 KB (9983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef08968ef9457641c0e689acdbc01bf1e55d8d12197f6173bdf29a40a3f5bcf`  
		Last Modified: Fri, 31 Jan 2025 03:36:23 GMT  
		Size: 147.3 MB (147283102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:1535c4f1183eadde07549a27ed7dc8f21f10cf57de739a787f8a69e00d31457b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcc619d4995d9dc51a6e764ce4f3e3d07b1b76bd124ddf5f155c6ecb3fd1726`

```dockerfile
```

-	Layers:
	-	`sha256:1d48c82c5407a49ef8ee40b4ff1f0c70c5d8f1f8fb1145327409004532f6e68f`  
		Last Modified: Fri, 31 Jan 2025 03:36:20 GMT  
		Size: 3.2 MB (3190921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77bea20d1f609e7c2a056dd3bda33939659f57d3bdec1bdfebf638239a756304`  
		Last Modified: Fri, 31 Jan 2025 03:36:19 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:5ed0d1dee447a0d486902aa90ec939ccbdcd008eace359fc9de82af0cec01657
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:9615ae5e6292e7d917f46bb56c6c8e52221e1013d12d2cf1a6daec226241ca73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323180380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5fec7366b094bbec1f8e7cf56c5ec325770bf6462082431966ceb935eac0fe0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 17 Dec 2024 20:59:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Tue, 17 Dec 2024 20:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Dec 2024 20:59:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=329761a647bfcee9b729d09a353c4a811772a6aa6b22dad451d3d065538c3447 NEO4J_TARBALL=neo4j-community-4.4.40-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Dec 2024 20:59:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 20:59:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Dec 2024 20:59:18 GMT
VOLUME [/data /logs]
# Tue, 17 Dec 2024 20:59:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Dec 2024 20:59:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 20:59:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0ae6360091eaad78b79c7ea2cd6a187036631b60889512eb1bbeec81e87b98`  
		Last Modified: Tue, 04 Feb 2025 05:18:53 GMT  
		Size: 145.6 MB (145598914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c30ff2193724d42334f1f019ba9b00b3be0555f7428c31c8c3ecd9b040cc0`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10e7e6d970a4d5729836504061b590969d7b39b710821ce4eb4178165240038`  
		Last Modified: Tue, 04 Feb 2025 05:18:54 GMT  
		Size: 147.3 MB (147315023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:67a2bc03cca78655856d1ef55cfac08a621ea233bf184e0d7b08c376782c367a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de22f507753a98453cef138677cb43e6cf1948b4cb8a3994cf6ee76ff93a9ff9`

```dockerfile
```

-	Layers:
	-	`sha256:c1a3ae191ab6aa349c2ac75ff221b83cf9656effe0f6711df9e68eb2390f9066`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 3.2 MB (3190657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf74c20585cabe460285ea1fd886f7c0a3afa3734c4b2235a4049bb8af1039e`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c3f16c5399b7aae333c7f740e940c58964bb92f0404c3483ef2baa6c7a840fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318427395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0398d8104d4a49b9ce25f2f88ae159947c21993dbc4c01c468e3e1a2c2272f24`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 17 Dec 2024 20:59:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 17 Dec 2024 20:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Dec 2024 20:59:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=329761a647bfcee9b729d09a353c4a811772a6aa6b22dad451d3d065538c3447 NEO4J_TARBALL=neo4j-community-4.4.40-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Dec 2024 20:59:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.40-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 20:59:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Dec 2024 20:59:18 GMT
VOLUME [/data /logs]
# Tue, 17 Dec 2024 20:59:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Dec 2024 20:59:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 20:59:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75f2a1647a2213cea5bd866fc62a6cb80c08c0c97a030b53f5ae8e5be7bc170`  
		Last Modified: Fri, 31 Jan 2025 03:36:23 GMT  
		Size: 142.4 MB (142385501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26800e74d4f320f8f2983d7cdda29606a285cb459688af7d0354068c4832a4fc`  
		Last Modified: Fri, 31 Jan 2025 03:36:19 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c781d3a34100b2f1b990589a48052ff0c060a35bdda82e4764f6a530c01023`  
		Last Modified: Fri, 31 Jan 2025 03:36:19 GMT  
		Size: 10.0 KB (9983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef08968ef9457641c0e689acdbc01bf1e55d8d12197f6173bdf29a40a3f5bcf`  
		Last Modified: Fri, 31 Jan 2025 03:36:23 GMT  
		Size: 147.3 MB (147283102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:1535c4f1183eadde07549a27ed7dc8f21f10cf57de739a787f8a69e00d31457b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcc619d4995d9dc51a6e764ce4f3e3d07b1b76bd124ddf5f155c6ecb3fd1726`

```dockerfile
```

-	Layers:
	-	`sha256:1d48c82c5407a49ef8ee40b4ff1f0c70c5d8f1f8fb1145327409004532f6e68f`  
		Last Modified: Fri, 31 Jan 2025 03:36:20 GMT  
		Size: 3.2 MB (3190921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77bea20d1f609e7c2a056dd3bda33939659f57d3bdec1bdfebf638239a756304`  
		Last Modified: Fri, 31 Jan 2025 03:36:19 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:89c0fe25753be3adb3896b0335686b72b5ab8457691321e78c61ce54e385be31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:99628485eec930d603269431163d8725dc9ce744d7921f323422a797ec063871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.1 MB (425101434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba33b31f5231686f14cfe91d214f6d6794e2b8ac01b69898af81ee16c933cd9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 17 Dec 2024 20:59:18 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Tue, 17 Dec 2024 20:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Dec 2024 20:59:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6e844a76066d8f7bf200a97e077a385347e9f7ca780392d5f70b19ceea782016 NEO4J_TARBALL=neo4j-enterprise-4.4.40-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Dec 2024 20:59:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.40-unix.tar.gz
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.40-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.40-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 20:59:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Dec 2024 20:59:18 GMT
VOLUME [/data /logs]
# Tue, 17 Dec 2024 20:59:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Dec 2024 20:59:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 20:59:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0ae6360091eaad78b79c7ea2cd6a187036631b60889512eb1bbeec81e87b98`  
		Last Modified: Tue, 04 Feb 2025 05:18:53 GMT  
		Size: 145.6 MB (145598914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb53c141b39af5c63455dcdaf3b0332992a9892d142af37044ce1e7b11a35e1`  
		Last Modified: Tue, 04 Feb 2025 05:18:59 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b723b843ea1efffe5a776da59e6a6866ceccf209320822bf7e349b88f60089d1`  
		Last Modified: Tue, 04 Feb 2025 05:18:59 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4f529b6ede8f5f3459720ff64c8f3fa6f9db251a6b48c6842f3007f05a2ec5`  
		Last Modified: Tue, 04 Feb 2025 05:19:03 GMT  
		Size: 249.2 MB (249236076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:97ee1ad60bc1284bf620096b986a147458eec457e7a94f569e6d4d140d341132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0402b80f85a39597cf466f7d6e5ca9bb198b80f279cd9fefaa7b947e1e698bf2`

```dockerfile
```

-	Layers:
	-	`sha256:f3d6826832e720c5fa5663496663dc29472b435ec5795cf9ec0ac89f8ec7070f`  
		Last Modified: Tue, 04 Feb 2025 05:18:59 GMT  
		Size: 3.3 MB (3339066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47fd5621ab880f6f1ba2605b9779790f5d751d1640ecba5443f4633c0e34292a`  
		Last Modified: Tue, 04 Feb 2025 05:18:59 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a3b5ca477461ccc61955da1d55c1a8626514cef6bf3eabb060646dbf42d9d89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.3 MB (420346761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9386a991490253f3f9f03154c74e64c233e8ba4253b54b81139d08a68c456fae`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 17 Dec 2024 20:59:18 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Tue, 17 Dec 2024 20:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Dec 2024 20:59:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6e844a76066d8f7bf200a97e077a385347e9f7ca780392d5f70b19ceea782016 NEO4J_TARBALL=neo4j-enterprise-4.4.40-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 17 Dec 2024 20:59:18 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.40-unix.tar.gz
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.40-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.40-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 17 Dec 2024 20:59:18 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Dec 2024 20:59:18 GMT
WORKDIR /var/lib/neo4j
# Tue, 17 Dec 2024 20:59:18 GMT
VOLUME [/data /logs]
# Tue, 17 Dec 2024 20:59:18 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 17 Dec 2024 20:59:18 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 17 Dec 2024 20:59:18 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75f2a1647a2213cea5bd866fc62a6cb80c08c0c97a030b53f5ae8e5be7bc170`  
		Last Modified: Fri, 31 Jan 2025 03:36:23 GMT  
		Size: 142.4 MB (142385501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1218d5013db47884c910047b753b08201b3352858467a0fd9d76d81b33b1307e`  
		Last Modified: Fri, 31 Jan 2025 03:37:31 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad62143625f9c9428bb2971f9cfd7e6ea8cc36f68bb514583a13123a53e5b8e`  
		Last Modified: Fri, 31 Jan 2025 03:37:31 GMT  
		Size: 10.0 KB (9984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5b6b48411eedd8910cb481c7f8aad10fa0cf86cd6ee2ba515a542aa555d749`  
		Last Modified: Fri, 31 Jan 2025 03:37:37 GMT  
		Size: 249.2 MB (249202466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:f28af9a48043247cbd4c0219e731cb4b32be7daa91d5a569109572b78ba638c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebac4113097ac80dbce090eac5c82ac9766808c7f7537d2d845f8da36a7c298`

```dockerfile
```

-	Layers:
	-	`sha256:dda7234291c54f9b798ad09450d2cd422519a10620ef9f1012d9df7caeec720c`  
		Last Modified: Fri, 31 Jan 2025 03:37:32 GMT  
		Size: 3.3 MB (3339306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ecd102bda2c695f05e15b9450d049a7716492f14e9044525a71df2927fbc3c8`  
		Last Modified: Fri, 31 Jan 2025 03:37:31 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.41`

**does not exist** (yet?)

## `neo4j:4.4.41-community`

**does not exist** (yet?)

## `neo4j:4.4.41-enterprise`

**does not exist** (yet?)

## `neo4j:5`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:1e419aff849ae03173f09e16c4f749ba83615e31acaa024d440c03a543cf1de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:956c82bd140ef18bf56e3d5aec3da71a784d741e5695d2b6cab5253e55c8aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332290415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c15602b100597031e9c91137eb74a52adb0df57cd516921ebe40fd9b1f8d9c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc914da1493d9049c0acbd1a8bf4d2a1addc4f950a238eee02a4c8cb8a6ff6e8`  
		Last Modified: Tue, 21 Jan 2025 19:29:22 GMT  
		Size: 133.9 MB (133868250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6736710fe7f53a64e03a662d3c860fdfc48bd0eb630dcdd726a349cf7717da`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c987625061d86c8ffcc30ef53809b182e8cf7c8bfc60d2165413c8137e7057`  
		Last Modified: Tue, 21 Jan 2025 19:29:23 GMT  
		Size: 159.0 MB (158979279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9ed78698fc3f696193f52c11d6b36c3acdb8a30a206f08b86e00fe8f1c08c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48c6810ed369d57a3eee598b3c21185fa67ce448c948f17c60d7d438e0e50`

```dockerfile
```

-	Layers:
	-	`sha256:9dc15b2397bb49a88990a47ce2924de67f17a9fa1d4134732636864213fe8197`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1345b98e8ee16338f7dcd94270a6cfd06a248077988426a609b5eecdbee253b1`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 22.5 KB (22536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:85f5b4b35bf25ba55ab0b1b72d0499b79148efbf09212af9b9bdcc5fd07adb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330407822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c916a7dc93af0f09c209520aeafc3b1ebb15d03e0af23924945f77d0ea469ace`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6cab068e4386031aa026205ba20abeb203a59805244ddeaf2cc56a55e3359`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 159.0 MB (158979285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:21731617e98b85e75967d5fc6913962b1d1bd09afc5b4553f35c876935f98657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6377389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d33455d6ec398cf90b4fac4203f8d290add519a53e564830bf111527f00a11`

```dockerfile
```

-	Layers:
	-	`sha256:57a0aa561f73bd19f71c7fa0af923dfd3b96c4d6ae172344e56489a161082650`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6f044d7d69c1e43bb3007a29d718665226067daafcfcfadf1b3719432d4e61`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 22.7 KB (22698 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:37734e08262d5183a9c44523a13e9b2c09828afc358ac36ee5c28b7b40485a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:add97b342b48daa8c5a2c59425f9262851b150c2be7210a4ad6493a9b28e576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528920fa82d08dd3caa077a4abe9c39e5c96d74ca3a96470fcb25add2572d46`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d8e39f72a1736e6d56e5a80cdb1c9d517d2bc4585140f31c3312f4ddd5e11`  
		Last Modified: Tue, 04 Feb 2025 05:19:21 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f3e6e2487defd5fa5b2636e2cf47e4912822538b215481768a758b093bf677`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a45755db635d17e3cdf98848174dd5d66c20e63c55893d8636e8d8a4e686`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60116b7e4342f72435a6aa154723cd4c1a29f44890a19389dc25e30846967e3b`  
		Last Modified: Tue, 04 Feb 2025 05:19:27 GMT  
		Size: 449.4 MB (449419700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e102750f331dd990eb0def0d15994597268a7734fe5851155a5ad154c88f9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e4db11082d76dfc951e3adb0b005e33a79025960818d5d6214dbf4c519a509`

```dockerfile
```

-	Layers:
	-	`sha256:3cc2f69e41a606faf1e9d3c6c4579255af6c4014a5f72cdb805026d8936bf088`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.5 MB (3538273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b2d9367ef1c4035372da64d1ec4c708df4d5e7cd361c96121a0b8b25b15385`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5bdf080b228c245cc68f1fc551605a977a88490b0eba3ba9dfa2852df95d9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621598666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd0cefa11659db229d221beca50f3e89b3ed1912cc0bae5999d3444934e5e70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11754d019316a799ba01b7d7274e18d8fecfddc1f996008b21a8ad547ffd33ff`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691a1fc0a09d3dfb8d49ee79c33145ddeef9efe482c6d2085dfc58a183ec3f15`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6783d4a96df097431f1d0849547d8172b0fa8dd05e30653d5b20d2e9d77d12`  
		Last Modified: Fri, 31 Jan 2025 03:35:08 GMT  
		Size: 449.4 MB (449385232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b58cb9221871bdd2b1453b1d16153e100b641dc304ae4238944b350fc8b81893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c12b54766c6af0b8cb64c18e532cd04b63f3697747c881aa13f394ffd4662e`

```dockerfile
```

-	Layers:
	-	`sha256:fa1df9c187013395a5fdf209685d1744d72916d99af0af4f0fe3942663777366`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.5 MB (3537967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff325ceffc2964321da89801218017b7af1b584b6c2b2e7ddc172d2971a2888c`  
		Last Modified: Fri, 31 Jan 2025 03:34:55 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:37734e08262d5183a9c44523a13e9b2c09828afc358ac36ee5c28b7b40485a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:add97b342b48daa8c5a2c59425f9262851b150c2be7210a4ad6493a9b28e576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528920fa82d08dd3caa077a4abe9c39e5c96d74ca3a96470fcb25add2572d46`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d8e39f72a1736e6d56e5a80cdb1c9d517d2bc4585140f31c3312f4ddd5e11`  
		Last Modified: Tue, 04 Feb 2025 05:19:21 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f3e6e2487defd5fa5b2636e2cf47e4912822538b215481768a758b093bf677`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a45755db635d17e3cdf98848174dd5d66c20e63c55893d8636e8d8a4e686`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60116b7e4342f72435a6aa154723cd4c1a29f44890a19389dc25e30846967e3b`  
		Last Modified: Tue, 04 Feb 2025 05:19:27 GMT  
		Size: 449.4 MB (449419700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e102750f331dd990eb0def0d15994597268a7734fe5851155a5ad154c88f9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e4db11082d76dfc951e3adb0b005e33a79025960818d5d6214dbf4c519a509`

```dockerfile
```

-	Layers:
	-	`sha256:3cc2f69e41a606faf1e9d3c6c4579255af6c4014a5f72cdb805026d8936bf088`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.5 MB (3538273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b2d9367ef1c4035372da64d1ec4c708df4d5e7cd361c96121a0b8b25b15385`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5bdf080b228c245cc68f1fc551605a977a88490b0eba3ba9dfa2852df95d9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621598666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd0cefa11659db229d221beca50f3e89b3ed1912cc0bae5999d3444934e5e70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11754d019316a799ba01b7d7274e18d8fecfddc1f996008b21a8ad547ffd33ff`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691a1fc0a09d3dfb8d49ee79c33145ddeef9efe482c6d2085dfc58a183ec3f15`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6783d4a96df097431f1d0849547d8172b0fa8dd05e30653d5b20d2e9d77d12`  
		Last Modified: Fri, 31 Jan 2025 03:35:08 GMT  
		Size: 449.4 MB (449385232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b58cb9221871bdd2b1453b1d16153e100b641dc304ae4238944b350fc8b81893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c12b54766c6af0b8cb64c18e532cd04b63f3697747c881aa13f394ffd4662e`

```dockerfile
```

-	Layers:
	-	`sha256:fa1df9c187013395a5fdf209685d1744d72916d99af0af4f0fe3942663777366`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.5 MB (3537967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff325ceffc2964321da89801218017b7af1b584b6c2b2e7ddc172d2971a2888c`  
		Last Modified: Fri, 31 Jan 2025 03:34:55 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9cda5476927bbdcd9001b3be34b35413904896bc86a9bb0ad23fead363c1bac1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:02588abebf1fd6a982e7b2cb7b80f928532abc499b99dd7a31920c8ee44a9e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.8 MB (619799448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb4967c321091f13fbd664ac973129b49eb45c69df4f76d626208377b7e66a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6781bd3c11fd8e26fbc353a6dbfc4d8888c6dd2ab14e5c743091c84c25a0554c`  
		Last Modified: Tue, 21 Jan 2025 19:29:35 GMT  
		Size: 133.9 MB (133868620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925455945241f3a6df224f9f3daa6b94240d6a704da5858fe5809c003f08ac4e`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab30e64f50685cb3019d3765c33399602cbc9aa2dbd709434f6e3eec5c33fa1`  
		Last Modified: Tue, 21 Jan 2025 19:29:39 GMT  
		Size: 446.5 MB (446487939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2ba7bd64022113b6b54c131eea41c727d0ad8827875f5ac3706c36312d88cdb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6706816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ce3ee8075ae280dce06d2d6494f1ba50cddd6005d6f8d3670bd94066a462a`

```dockerfile
```

-	Layers:
	-	`sha256:9d64bb2bcd78e986694a9f22a3d4965411b0b316dbcc18dc5c57e0957e190f23`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 6.7 MB (6685457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d3665e9b5fca450d5c677e112ba55c0fb4c2f010b592e63383724f5512496a`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 21.4 KB (21359 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:966e0b9dace304a11b6e50095bc869f5b7a0cacabc6bb15c008ade266cc48570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.9 MB (617916538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ecd3da8c3dfd864d856236a378e6986b5b002e6a0e8c638566bb9db3375c8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596d13afc954415f8b3e3cb5f77d41d95f3f5e008c24ba504a2ca8108c96a1c1`  
		Last Modified: Tue, 21 Jan 2025 20:28:19 GMT  
		Size: 446.5 MB (446488001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b094bc862fd9f0521e6680debd07f98b140749ef35d89964032dda2bf1e6a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6686303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0e6e718a94f8044be0e609575ef098048c52184cc4695ebc17de8048ef0460`

```dockerfile
```

-	Layers:
	-	`sha256:8d8bbb90e824c8c9b170503f16f4c2555b77bb502e26dd9d6f2dba985587eb2b`  
		Last Modified: Tue, 21 Jan 2025 20:28:10 GMT  
		Size: 6.7 MB (6664832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0769f336b16d2c1e724496207ddb77ec763b609f095fa88224ccbe8fbcb7479`  
		Last Modified: Tue, 21 Jan 2025 20:28:09 GMT  
		Size: 21.5 KB (21471 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:1e419aff849ae03173f09e16c4f749ba83615e31acaa024d440c03a543cf1de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:956c82bd140ef18bf56e3d5aec3da71a784d741e5695d2b6cab5253e55c8aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332290415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c15602b100597031e9c91137eb74a52adb0df57cd516921ebe40fd9b1f8d9c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc914da1493d9049c0acbd1a8bf4d2a1addc4f950a238eee02a4c8cb8a6ff6e8`  
		Last Modified: Tue, 21 Jan 2025 19:29:22 GMT  
		Size: 133.9 MB (133868250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6736710fe7f53a64e03a662d3c860fdfc48bd0eb630dcdd726a349cf7717da`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c987625061d86c8ffcc30ef53809b182e8cf7c8bfc60d2165413c8137e7057`  
		Last Modified: Tue, 21 Jan 2025 19:29:23 GMT  
		Size: 159.0 MB (158979279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9ed78698fc3f696193f52c11d6b36c3acdb8a30a206f08b86e00fe8f1c08c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48c6810ed369d57a3eee598b3c21185fa67ce448c948f17c60d7d438e0e50`

```dockerfile
```

-	Layers:
	-	`sha256:9dc15b2397bb49a88990a47ce2924de67f17a9fa1d4134732636864213fe8197`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1345b98e8ee16338f7dcd94270a6cfd06a248077988426a609b5eecdbee253b1`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 22.5 KB (22536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:85f5b4b35bf25ba55ab0b1b72d0499b79148efbf09212af9b9bdcc5fd07adb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330407822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c916a7dc93af0f09c209520aeafc3b1ebb15d03e0af23924945f77d0ea469ace`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6cab068e4386031aa026205ba20abeb203a59805244ddeaf2cc56a55e3359`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 159.0 MB (158979285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:21731617e98b85e75967d5fc6913962b1d1bd09afc5b4553f35c876935f98657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6377389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d33455d6ec398cf90b4fac4203f8d290add519a53e564830bf111527f00a11`

```dockerfile
```

-	Layers:
	-	`sha256:57a0aa561f73bd19f71c7fa0af923dfd3b96c4d6ae172344e56489a161082650`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6f044d7d69c1e43bb3007a29d718665226067daafcfcfadf1b3719432d4e61`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 22.7 KB (22698 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-bullseye`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-community`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-community-bullseye`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-community-ubi9`

```console
$ docker pull neo4j@sha256:1e419aff849ae03173f09e16c4f749ba83615e31acaa024d440c03a543cf1de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:956c82bd140ef18bf56e3d5aec3da71a784d741e5695d2b6cab5253e55c8aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332290415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c15602b100597031e9c91137eb74a52adb0df57cd516921ebe40fd9b1f8d9c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc914da1493d9049c0acbd1a8bf4d2a1addc4f950a238eee02a4c8cb8a6ff6e8`  
		Last Modified: Tue, 21 Jan 2025 19:29:22 GMT  
		Size: 133.9 MB (133868250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6736710fe7f53a64e03a662d3c860fdfc48bd0eb630dcdd726a349cf7717da`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c987625061d86c8ffcc30ef53809b182e8cf7c8bfc60d2165413c8137e7057`  
		Last Modified: Tue, 21 Jan 2025 19:29:23 GMT  
		Size: 159.0 MB (158979279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9ed78698fc3f696193f52c11d6b36c3acdb8a30a206f08b86e00fe8f1c08c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48c6810ed369d57a3eee598b3c21185fa67ce448c948f17c60d7d438e0e50`

```dockerfile
```

-	Layers:
	-	`sha256:9dc15b2397bb49a88990a47ce2924de67f17a9fa1d4134732636864213fe8197`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1345b98e8ee16338f7dcd94270a6cfd06a248077988426a609b5eecdbee253b1`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 22.5 KB (22536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:85f5b4b35bf25ba55ab0b1b72d0499b79148efbf09212af9b9bdcc5fd07adb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330407822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c916a7dc93af0f09c209520aeafc3b1ebb15d03e0af23924945f77d0ea469ace`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6cab068e4386031aa026205ba20abeb203a59805244ddeaf2cc56a55e3359`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 159.0 MB (158979285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:21731617e98b85e75967d5fc6913962b1d1bd09afc5b4553f35c876935f98657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6377389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d33455d6ec398cf90b4fac4203f8d290add519a53e564830bf111527f00a11`

```dockerfile
```

-	Layers:
	-	`sha256:57a0aa561f73bd19f71c7fa0af923dfd3b96c4d6ae172344e56489a161082650`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6f044d7d69c1e43bb3007a29d718665226067daafcfcfadf1b3719432d4e61`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 22.7 KB (22698 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-enterprise`

```console
$ docker pull neo4j@sha256:37734e08262d5183a9c44523a13e9b2c09828afc358ac36ee5c28b7b40485a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:add97b342b48daa8c5a2c59425f9262851b150c2be7210a4ad6493a9b28e576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528920fa82d08dd3caa077a4abe9c39e5c96d74ca3a96470fcb25add2572d46`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d8e39f72a1736e6d56e5a80cdb1c9d517d2bc4585140f31c3312f4ddd5e11`  
		Last Modified: Tue, 04 Feb 2025 05:19:21 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f3e6e2487defd5fa5b2636e2cf47e4912822538b215481768a758b093bf677`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a45755db635d17e3cdf98848174dd5d66c20e63c55893d8636e8d8a4e686`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60116b7e4342f72435a6aa154723cd4c1a29f44890a19389dc25e30846967e3b`  
		Last Modified: Tue, 04 Feb 2025 05:19:27 GMT  
		Size: 449.4 MB (449419700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e102750f331dd990eb0def0d15994597268a7734fe5851155a5ad154c88f9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e4db11082d76dfc951e3adb0b005e33a79025960818d5d6214dbf4c519a509`

```dockerfile
```

-	Layers:
	-	`sha256:3cc2f69e41a606faf1e9d3c6c4579255af6c4014a5f72cdb805026d8936bf088`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.5 MB (3538273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b2d9367ef1c4035372da64d1ec4c708df4d5e7cd361c96121a0b8b25b15385`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5bdf080b228c245cc68f1fc551605a977a88490b0eba3ba9dfa2852df95d9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621598666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd0cefa11659db229d221beca50f3e89b3ed1912cc0bae5999d3444934e5e70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11754d019316a799ba01b7d7274e18d8fecfddc1f996008b21a8ad547ffd33ff`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691a1fc0a09d3dfb8d49ee79c33145ddeef9efe482c6d2085dfc58a183ec3f15`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6783d4a96df097431f1d0849547d8172b0fa8dd05e30653d5b20d2e9d77d12`  
		Last Modified: Fri, 31 Jan 2025 03:35:08 GMT  
		Size: 449.4 MB (449385232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b58cb9221871bdd2b1453b1d16153e100b641dc304ae4238944b350fc8b81893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c12b54766c6af0b8cb64c18e532cd04b63f3697747c881aa13f394ffd4662e`

```dockerfile
```

-	Layers:
	-	`sha256:fa1df9c187013395a5fdf209685d1744d72916d99af0af4f0fe3942663777366`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.5 MB (3537967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff325ceffc2964321da89801218017b7af1b584b6c2b2e7ddc172d2971a2888c`  
		Last Modified: Fri, 31 Jan 2025 03:34:55 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:37734e08262d5183a9c44523a13e9b2c09828afc358ac36ee5c28b7b40485a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:add97b342b48daa8c5a2c59425f9262851b150c2be7210a4ad6493a9b28e576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528920fa82d08dd3caa077a4abe9c39e5c96d74ca3a96470fcb25add2572d46`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d8e39f72a1736e6d56e5a80cdb1c9d517d2bc4585140f31c3312f4ddd5e11`  
		Last Modified: Tue, 04 Feb 2025 05:19:21 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f3e6e2487defd5fa5b2636e2cf47e4912822538b215481768a758b093bf677`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a45755db635d17e3cdf98848174dd5d66c20e63c55893d8636e8d8a4e686`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60116b7e4342f72435a6aa154723cd4c1a29f44890a19389dc25e30846967e3b`  
		Last Modified: Tue, 04 Feb 2025 05:19:27 GMT  
		Size: 449.4 MB (449419700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e102750f331dd990eb0def0d15994597268a7734fe5851155a5ad154c88f9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e4db11082d76dfc951e3adb0b005e33a79025960818d5d6214dbf4c519a509`

```dockerfile
```

-	Layers:
	-	`sha256:3cc2f69e41a606faf1e9d3c6c4579255af6c4014a5f72cdb805026d8936bf088`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.5 MB (3538273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b2d9367ef1c4035372da64d1ec4c708df4d5e7cd361c96121a0b8b25b15385`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5bdf080b228c245cc68f1fc551605a977a88490b0eba3ba9dfa2852df95d9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621598666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd0cefa11659db229d221beca50f3e89b3ed1912cc0bae5999d3444934e5e70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11754d019316a799ba01b7d7274e18d8fecfddc1f996008b21a8ad547ffd33ff`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691a1fc0a09d3dfb8d49ee79c33145ddeef9efe482c6d2085dfc58a183ec3f15`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6783d4a96df097431f1d0849547d8172b0fa8dd05e30653d5b20d2e9d77d12`  
		Last Modified: Fri, 31 Jan 2025 03:35:08 GMT  
		Size: 449.4 MB (449385232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b58cb9221871bdd2b1453b1d16153e100b641dc304ae4238944b350fc8b81893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c12b54766c6af0b8cb64c18e532cd04b63f3697747c881aa13f394ffd4662e`

```dockerfile
```

-	Layers:
	-	`sha256:fa1df9c187013395a5fdf209685d1744d72916d99af0af4f0fe3942663777366`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.5 MB (3537967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff325ceffc2964321da89801218017b7af1b584b6c2b2e7ddc172d2971a2888c`  
		Last Modified: Fri, 31 Jan 2025 03:34:55 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9cda5476927bbdcd9001b3be34b35413904896bc86a9bb0ad23fead363c1bac1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:02588abebf1fd6a982e7b2cb7b80f928532abc499b99dd7a31920c8ee44a9e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.8 MB (619799448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb4967c321091f13fbd664ac973129b49eb45c69df4f76d626208377b7e66a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6781bd3c11fd8e26fbc353a6dbfc4d8888c6dd2ab14e5c743091c84c25a0554c`  
		Last Modified: Tue, 21 Jan 2025 19:29:35 GMT  
		Size: 133.9 MB (133868620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925455945241f3a6df224f9f3daa6b94240d6a704da5858fe5809c003f08ac4e`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab30e64f50685cb3019d3765c33399602cbc9aa2dbd709434f6e3eec5c33fa1`  
		Last Modified: Tue, 21 Jan 2025 19:29:39 GMT  
		Size: 446.5 MB (446487939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2ba7bd64022113b6b54c131eea41c727d0ad8827875f5ac3706c36312d88cdb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6706816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ce3ee8075ae280dce06d2d6494f1ba50cddd6005d6f8d3670bd94066a462a`

```dockerfile
```

-	Layers:
	-	`sha256:9d64bb2bcd78e986694a9f22a3d4965411b0b316dbcc18dc5c57e0957e190f23`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 6.7 MB (6685457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d3665e9b5fca450d5c677e112ba55c0fb4c2f010b592e63383724f5512496a`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 21.4 KB (21359 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:966e0b9dace304a11b6e50095bc869f5b7a0cacabc6bb15c008ade266cc48570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.9 MB (617916538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ecd3da8c3dfd864d856236a378e6986b5b002e6a0e8c638566bb9db3375c8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596d13afc954415f8b3e3cb5f77d41d95f3f5e008c24ba504a2ca8108c96a1c1`  
		Last Modified: Tue, 21 Jan 2025 20:28:19 GMT  
		Size: 446.5 MB (446488001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b094bc862fd9f0521e6680debd07f98b140749ef35d89964032dda2bf1e6a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6686303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0e6e718a94f8044be0e609575ef098048c52184cc4695ebc17de8048ef0460`

```dockerfile
```

-	Layers:
	-	`sha256:8d8bbb90e824c8c9b170503f16f4c2555b77bb502e26dd9d6f2dba985587eb2b`  
		Last Modified: Tue, 21 Jan 2025 20:28:10 GMT  
		Size: 6.7 MB (6664832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0769f336b16d2c1e724496207ddb77ec763b609f095fa88224ccbe8fbcb7479`  
		Last Modified: Tue, 21 Jan 2025 20:28:09 GMT  
		Size: 21.5 KB (21471 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-ubi9`

```console
$ docker pull neo4j@sha256:1e419aff849ae03173f09e16c4f749ba83615e31acaa024d440c03a543cf1de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:956c82bd140ef18bf56e3d5aec3da71a784d741e5695d2b6cab5253e55c8aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332290415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c15602b100597031e9c91137eb74a52adb0df57cd516921ebe40fd9b1f8d9c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc914da1493d9049c0acbd1a8bf4d2a1addc4f950a238eee02a4c8cb8a6ff6e8`  
		Last Modified: Tue, 21 Jan 2025 19:29:22 GMT  
		Size: 133.9 MB (133868250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6736710fe7f53a64e03a662d3c860fdfc48bd0eb630dcdd726a349cf7717da`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c987625061d86c8ffcc30ef53809b182e8cf7c8bfc60d2165413c8137e7057`  
		Last Modified: Tue, 21 Jan 2025 19:29:23 GMT  
		Size: 159.0 MB (158979279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9ed78698fc3f696193f52c11d6b36c3acdb8a30a206f08b86e00fe8f1c08c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48c6810ed369d57a3eee598b3c21185fa67ce448c948f17c60d7d438e0e50`

```dockerfile
```

-	Layers:
	-	`sha256:9dc15b2397bb49a88990a47ce2924de67f17a9fa1d4134732636864213fe8197`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1345b98e8ee16338f7dcd94270a6cfd06a248077988426a609b5eecdbee253b1`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 22.5 KB (22536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:85f5b4b35bf25ba55ab0b1b72d0499b79148efbf09212af9b9bdcc5fd07adb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330407822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c916a7dc93af0f09c209520aeafc3b1ebb15d03e0af23924945f77d0ea469ace`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6cab068e4386031aa026205ba20abeb203a59805244ddeaf2cc56a55e3359`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 159.0 MB (158979285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:21731617e98b85e75967d5fc6913962b1d1bd09afc5b4553f35c876935f98657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6377389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d33455d6ec398cf90b4fac4203f8d290add519a53e564830bf111527f00a11`

```dockerfile
```

-	Layers:
	-	`sha256:57a0aa561f73bd19f71c7fa0af923dfd3b96c4d6ae172344e56489a161082650`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6f044d7d69c1e43bb3007a29d718665226067daafcfcfadf1b3719432d4e61`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 22.7 KB (22698 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.1`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.1` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.1` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.1-bullseye`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.1-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.1-community`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.1-community` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.1-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.1-community-bullseye`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.1-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.1-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.1-community-ubi9`

```console
$ docker pull neo4j@sha256:1e419aff849ae03173f09e16c4f749ba83615e31acaa024d440c03a543cf1de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.1-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:956c82bd140ef18bf56e3d5aec3da71a784d741e5695d2b6cab5253e55c8aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332290415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c15602b100597031e9c91137eb74a52adb0df57cd516921ebe40fd9b1f8d9c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc914da1493d9049c0acbd1a8bf4d2a1addc4f950a238eee02a4c8cb8a6ff6e8`  
		Last Modified: Tue, 21 Jan 2025 19:29:22 GMT  
		Size: 133.9 MB (133868250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6736710fe7f53a64e03a662d3c860fdfc48bd0eb630dcdd726a349cf7717da`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c987625061d86c8ffcc30ef53809b182e8cf7c8bfc60d2165413c8137e7057`  
		Last Modified: Tue, 21 Jan 2025 19:29:23 GMT  
		Size: 159.0 MB (158979279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9ed78698fc3f696193f52c11d6b36c3acdb8a30a206f08b86e00fe8f1c08c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48c6810ed369d57a3eee598b3c21185fa67ce448c948f17c60d7d438e0e50`

```dockerfile
```

-	Layers:
	-	`sha256:9dc15b2397bb49a88990a47ce2924de67f17a9fa1d4134732636864213fe8197`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1345b98e8ee16338f7dcd94270a6cfd06a248077988426a609b5eecdbee253b1`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 22.5 KB (22536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.1-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:85f5b4b35bf25ba55ab0b1b72d0499b79148efbf09212af9b9bdcc5fd07adb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330407822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c916a7dc93af0f09c209520aeafc3b1ebb15d03e0af23924945f77d0ea469ace`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6cab068e4386031aa026205ba20abeb203a59805244ddeaf2cc56a55e3359`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 159.0 MB (158979285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:21731617e98b85e75967d5fc6913962b1d1bd09afc5b4553f35c876935f98657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6377389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d33455d6ec398cf90b4fac4203f8d290add519a53e564830bf111527f00a11`

```dockerfile
```

-	Layers:
	-	`sha256:57a0aa561f73bd19f71c7fa0af923dfd3b96c4d6ae172344e56489a161082650`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6f044d7d69c1e43bb3007a29d718665226067daafcfcfadf1b3719432d4e61`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 22.7 KB (22698 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.1-enterprise`

```console
$ docker pull neo4j@sha256:37734e08262d5183a9c44523a13e9b2c09828afc358ac36ee5c28b7b40485a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.1-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:add97b342b48daa8c5a2c59425f9262851b150c2be7210a4ad6493a9b28e576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528920fa82d08dd3caa077a4abe9c39e5c96d74ca3a96470fcb25add2572d46`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d8e39f72a1736e6d56e5a80cdb1c9d517d2bc4585140f31c3312f4ddd5e11`  
		Last Modified: Tue, 04 Feb 2025 05:19:21 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f3e6e2487defd5fa5b2636e2cf47e4912822538b215481768a758b093bf677`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a45755db635d17e3cdf98848174dd5d66c20e63c55893d8636e8d8a4e686`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60116b7e4342f72435a6aa154723cd4c1a29f44890a19389dc25e30846967e3b`  
		Last Modified: Tue, 04 Feb 2025 05:19:27 GMT  
		Size: 449.4 MB (449419700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e102750f331dd990eb0def0d15994597268a7734fe5851155a5ad154c88f9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e4db11082d76dfc951e3adb0b005e33a79025960818d5d6214dbf4c519a509`

```dockerfile
```

-	Layers:
	-	`sha256:3cc2f69e41a606faf1e9d3c6c4579255af6c4014a5f72cdb805026d8936bf088`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.5 MB (3538273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b2d9367ef1c4035372da64d1ec4c708df4d5e7cd361c96121a0b8b25b15385`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5bdf080b228c245cc68f1fc551605a977a88490b0eba3ba9dfa2852df95d9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621598666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd0cefa11659db229d221beca50f3e89b3ed1912cc0bae5999d3444934e5e70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11754d019316a799ba01b7d7274e18d8fecfddc1f996008b21a8ad547ffd33ff`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691a1fc0a09d3dfb8d49ee79c33145ddeef9efe482c6d2085dfc58a183ec3f15`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6783d4a96df097431f1d0849547d8172b0fa8dd05e30653d5b20d2e9d77d12`  
		Last Modified: Fri, 31 Jan 2025 03:35:08 GMT  
		Size: 449.4 MB (449385232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b58cb9221871bdd2b1453b1d16153e100b641dc304ae4238944b350fc8b81893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c12b54766c6af0b8cb64c18e532cd04b63f3697747c881aa13f394ffd4662e`

```dockerfile
```

-	Layers:
	-	`sha256:fa1df9c187013395a5fdf209685d1744d72916d99af0af4f0fe3942663777366`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.5 MB (3537967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff325ceffc2964321da89801218017b7af1b584b6c2b2e7ddc172d2971a2888c`  
		Last Modified: Fri, 31 Jan 2025 03:34:55 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.1-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:37734e08262d5183a9c44523a13e9b2c09828afc358ac36ee5c28b7b40485a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.1-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:add97b342b48daa8c5a2c59425f9262851b150c2be7210a4ad6493a9b28e576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528920fa82d08dd3caa077a4abe9c39e5c96d74ca3a96470fcb25add2572d46`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d8e39f72a1736e6d56e5a80cdb1c9d517d2bc4585140f31c3312f4ddd5e11`  
		Last Modified: Tue, 04 Feb 2025 05:19:21 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f3e6e2487defd5fa5b2636e2cf47e4912822538b215481768a758b093bf677`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a45755db635d17e3cdf98848174dd5d66c20e63c55893d8636e8d8a4e686`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60116b7e4342f72435a6aa154723cd4c1a29f44890a19389dc25e30846967e3b`  
		Last Modified: Tue, 04 Feb 2025 05:19:27 GMT  
		Size: 449.4 MB (449419700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e102750f331dd990eb0def0d15994597268a7734fe5851155a5ad154c88f9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e4db11082d76dfc951e3adb0b005e33a79025960818d5d6214dbf4c519a509`

```dockerfile
```

-	Layers:
	-	`sha256:3cc2f69e41a606faf1e9d3c6c4579255af6c4014a5f72cdb805026d8936bf088`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.5 MB (3538273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b2d9367ef1c4035372da64d1ec4c708df4d5e7cd361c96121a0b8b25b15385`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.1-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5bdf080b228c245cc68f1fc551605a977a88490b0eba3ba9dfa2852df95d9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621598666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd0cefa11659db229d221beca50f3e89b3ed1912cc0bae5999d3444934e5e70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11754d019316a799ba01b7d7274e18d8fecfddc1f996008b21a8ad547ffd33ff`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691a1fc0a09d3dfb8d49ee79c33145ddeef9efe482c6d2085dfc58a183ec3f15`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6783d4a96df097431f1d0849547d8172b0fa8dd05e30653d5b20d2e9d77d12`  
		Last Modified: Fri, 31 Jan 2025 03:35:08 GMT  
		Size: 449.4 MB (449385232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b58cb9221871bdd2b1453b1d16153e100b641dc304ae4238944b350fc8b81893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c12b54766c6af0b8cb64c18e532cd04b63f3697747c881aa13f394ffd4662e`

```dockerfile
```

-	Layers:
	-	`sha256:fa1df9c187013395a5fdf209685d1744d72916d99af0af4f0fe3942663777366`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.5 MB (3537967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff325ceffc2964321da89801218017b7af1b584b6c2b2e7ddc172d2971a2888c`  
		Last Modified: Fri, 31 Jan 2025 03:34:55 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.1-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9cda5476927bbdcd9001b3be34b35413904896bc86a9bb0ad23fead363c1bac1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.1-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:02588abebf1fd6a982e7b2cb7b80f928532abc499b99dd7a31920c8ee44a9e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.8 MB (619799448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb4967c321091f13fbd664ac973129b49eb45c69df4f76d626208377b7e66a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6781bd3c11fd8e26fbc353a6dbfc4d8888c6dd2ab14e5c743091c84c25a0554c`  
		Last Modified: Tue, 21 Jan 2025 19:29:35 GMT  
		Size: 133.9 MB (133868620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925455945241f3a6df224f9f3daa6b94240d6a704da5858fe5809c003f08ac4e`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab30e64f50685cb3019d3765c33399602cbc9aa2dbd709434f6e3eec5c33fa1`  
		Last Modified: Tue, 21 Jan 2025 19:29:39 GMT  
		Size: 446.5 MB (446487939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2ba7bd64022113b6b54c131eea41c727d0ad8827875f5ac3706c36312d88cdb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6706816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ce3ee8075ae280dce06d2d6494f1ba50cddd6005d6f8d3670bd94066a462a`

```dockerfile
```

-	Layers:
	-	`sha256:9d64bb2bcd78e986694a9f22a3d4965411b0b316dbcc18dc5c57e0957e190f23`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 6.7 MB (6685457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d3665e9b5fca450d5c677e112ba55c0fb4c2f010b592e63383724f5512496a`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 21.4 KB (21359 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.1-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:966e0b9dace304a11b6e50095bc869f5b7a0cacabc6bb15c008ade266cc48570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.9 MB (617916538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ecd3da8c3dfd864d856236a378e6986b5b002e6a0e8c638566bb9db3375c8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596d13afc954415f8b3e3cb5f77d41d95f3f5e008c24ba504a2ca8108c96a1c1`  
		Last Modified: Tue, 21 Jan 2025 20:28:19 GMT  
		Size: 446.5 MB (446488001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b094bc862fd9f0521e6680debd07f98b140749ef35d89964032dda2bf1e6a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6686303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0e6e718a94f8044be0e609575ef098048c52184cc4695ebc17de8048ef0460`

```dockerfile
```

-	Layers:
	-	`sha256:8d8bbb90e824c8c9b170503f16f4c2555b77bb502e26dd9d6f2dba985587eb2b`  
		Last Modified: Tue, 21 Jan 2025 20:28:10 GMT  
		Size: 6.7 MB (6664832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0769f336b16d2c1e724496207ddb77ec763b609f095fa88224ccbe8fbcb7479`  
		Last Modified: Tue, 21 Jan 2025 20:28:09 GMT  
		Size: 21.5 KB (21471 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.1-ubi9`

```console
$ docker pull neo4j@sha256:1e419aff849ae03173f09e16c4f749ba83615e31acaa024d440c03a543cf1de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.1-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:956c82bd140ef18bf56e3d5aec3da71a784d741e5695d2b6cab5253e55c8aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332290415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c15602b100597031e9c91137eb74a52adb0df57cd516921ebe40fd9b1f8d9c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc914da1493d9049c0acbd1a8bf4d2a1addc4f950a238eee02a4c8cb8a6ff6e8`  
		Last Modified: Tue, 21 Jan 2025 19:29:22 GMT  
		Size: 133.9 MB (133868250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6736710fe7f53a64e03a662d3c860fdfc48bd0eb630dcdd726a349cf7717da`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c987625061d86c8ffcc30ef53809b182e8cf7c8bfc60d2165413c8137e7057`  
		Last Modified: Tue, 21 Jan 2025 19:29:23 GMT  
		Size: 159.0 MB (158979279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9ed78698fc3f696193f52c11d6b36c3acdb8a30a206f08b86e00fe8f1c08c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48c6810ed369d57a3eee598b3c21185fa67ce448c948f17c60d7d438e0e50`

```dockerfile
```

-	Layers:
	-	`sha256:9dc15b2397bb49a88990a47ce2924de67f17a9fa1d4134732636864213fe8197`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1345b98e8ee16338f7dcd94270a6cfd06a248077988426a609b5eecdbee253b1`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 22.5 KB (22536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.1-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:85f5b4b35bf25ba55ab0b1b72d0499b79148efbf09212af9b9bdcc5fd07adb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330407822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c916a7dc93af0f09c209520aeafc3b1ebb15d03e0af23924945f77d0ea469ace`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6cab068e4386031aa026205ba20abeb203a59805244ddeaf2cc56a55e3359`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 159.0 MB (158979285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.1-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:21731617e98b85e75967d5fc6913962b1d1bd09afc5b4553f35c876935f98657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6377389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d33455d6ec398cf90b4fac4203f8d290add519a53e564830bf111527f00a11`

```dockerfile
```

-	Layers:
	-	`sha256:57a0aa561f73bd19f71c7fa0af923dfd3b96c4d6ae172344e56489a161082650`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6f044d7d69c1e43bb3007a29d718665226067daafcfcfadf1b3719432d4e61`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 22.7 KB (22698 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:1e419aff849ae03173f09e16c4f749ba83615e31acaa024d440c03a543cf1de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:956c82bd140ef18bf56e3d5aec3da71a784d741e5695d2b6cab5253e55c8aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332290415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c15602b100597031e9c91137eb74a52adb0df57cd516921ebe40fd9b1f8d9c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc914da1493d9049c0acbd1a8bf4d2a1addc4f950a238eee02a4c8cb8a6ff6e8`  
		Last Modified: Tue, 21 Jan 2025 19:29:22 GMT  
		Size: 133.9 MB (133868250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6736710fe7f53a64e03a662d3c860fdfc48bd0eb630dcdd726a349cf7717da`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c987625061d86c8ffcc30ef53809b182e8cf7c8bfc60d2165413c8137e7057`  
		Last Modified: Tue, 21 Jan 2025 19:29:23 GMT  
		Size: 159.0 MB (158979279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9ed78698fc3f696193f52c11d6b36c3acdb8a30a206f08b86e00fe8f1c08c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48c6810ed369d57a3eee598b3c21185fa67ce448c948f17c60d7d438e0e50`

```dockerfile
```

-	Layers:
	-	`sha256:9dc15b2397bb49a88990a47ce2924de67f17a9fa1d4134732636864213fe8197`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1345b98e8ee16338f7dcd94270a6cfd06a248077988426a609b5eecdbee253b1`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 22.5 KB (22536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:85f5b4b35bf25ba55ab0b1b72d0499b79148efbf09212af9b9bdcc5fd07adb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330407822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c916a7dc93af0f09c209520aeafc3b1ebb15d03e0af23924945f77d0ea469ace`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6cab068e4386031aa026205ba20abeb203a59805244ddeaf2cc56a55e3359`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 159.0 MB (158979285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:21731617e98b85e75967d5fc6913962b1d1bd09afc5b4553f35c876935f98657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6377389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d33455d6ec398cf90b4fac4203f8d290add519a53e564830bf111527f00a11`

```dockerfile
```

-	Layers:
	-	`sha256:57a0aa561f73bd19f71c7fa0af923dfd3b96c4d6ae172344e56489a161082650`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6f044d7d69c1e43bb3007a29d718665226067daafcfcfadf1b3719432d4e61`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 22.7 KB (22698 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:37734e08262d5183a9c44523a13e9b2c09828afc358ac36ee5c28b7b40485a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:add97b342b48daa8c5a2c59425f9262851b150c2be7210a4ad6493a9b28e576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528920fa82d08dd3caa077a4abe9c39e5c96d74ca3a96470fcb25add2572d46`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d8e39f72a1736e6d56e5a80cdb1c9d517d2bc4585140f31c3312f4ddd5e11`  
		Last Modified: Tue, 04 Feb 2025 05:19:21 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f3e6e2487defd5fa5b2636e2cf47e4912822538b215481768a758b093bf677`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a45755db635d17e3cdf98848174dd5d66c20e63c55893d8636e8d8a4e686`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60116b7e4342f72435a6aa154723cd4c1a29f44890a19389dc25e30846967e3b`  
		Last Modified: Tue, 04 Feb 2025 05:19:27 GMT  
		Size: 449.4 MB (449419700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e102750f331dd990eb0def0d15994597268a7734fe5851155a5ad154c88f9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e4db11082d76dfc951e3adb0b005e33a79025960818d5d6214dbf4c519a509`

```dockerfile
```

-	Layers:
	-	`sha256:3cc2f69e41a606faf1e9d3c6c4579255af6c4014a5f72cdb805026d8936bf088`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.5 MB (3538273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b2d9367ef1c4035372da64d1ec4c708df4d5e7cd361c96121a0b8b25b15385`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5bdf080b228c245cc68f1fc551605a977a88490b0eba3ba9dfa2852df95d9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621598666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd0cefa11659db229d221beca50f3e89b3ed1912cc0bae5999d3444934e5e70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11754d019316a799ba01b7d7274e18d8fecfddc1f996008b21a8ad547ffd33ff`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691a1fc0a09d3dfb8d49ee79c33145ddeef9efe482c6d2085dfc58a183ec3f15`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6783d4a96df097431f1d0849547d8172b0fa8dd05e30653d5b20d2e9d77d12`  
		Last Modified: Fri, 31 Jan 2025 03:35:08 GMT  
		Size: 449.4 MB (449385232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:b58cb9221871bdd2b1453b1d16153e100b641dc304ae4238944b350fc8b81893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c12b54766c6af0b8cb64c18e532cd04b63f3697747c881aa13f394ffd4662e`

```dockerfile
```

-	Layers:
	-	`sha256:fa1df9c187013395a5fdf209685d1744d72916d99af0af4f0fe3942663777366`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.5 MB (3537967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff325ceffc2964321da89801218017b7af1b584b6c2b2e7ddc172d2971a2888c`  
		Last Modified: Fri, 31 Jan 2025 03:34:55 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:37734e08262d5183a9c44523a13e9b2c09828afc358ac36ee5c28b7b40485a3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:add97b342b48daa8c5a2c59425f9262851b150c2be7210a4ad6493a9b28e576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.3 MB (624252718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528920fa82d08dd3caa077a4abe9c39e5c96d74ca3a96470fcb25add2572d46`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493d8e39f72a1736e6d56e5a80cdb1c9d517d2bc4585140f31c3312f4ddd5e11`  
		Last Modified: Tue, 04 Feb 2025 05:19:21 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f3e6e2487defd5fa5b2636e2cf47e4912822538b215481768a758b093bf677`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a45755db635d17e3cdf98848174dd5d66c20e63c55893d8636e8d8a4e686`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60116b7e4342f72435a6aa154723cd4c1a29f44890a19389dc25e30846967e3b`  
		Last Modified: Tue, 04 Feb 2025 05:19:27 GMT  
		Size: 449.4 MB (449419700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e102750f331dd990eb0def0d15994597268a7734fe5851155a5ad154c88f9956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e4db11082d76dfc951e3adb0b005e33a79025960818d5d6214dbf4c519a509`

```dockerfile
```

-	Layers:
	-	`sha256:3cc2f69e41a606faf1e9d3c6c4579255af6c4014a5f72cdb805026d8936bf088`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 3.5 MB (3538273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b2d9367ef1c4035372da64d1ec4c708df4d5e7cd361c96121a0b8b25b15385`  
		Last Modified: Tue, 04 Feb 2025 05:19:18 GMT  
		Size: 21.4 KB (21383 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:a5bdf080b228c245cc68f1fc551605a977a88490b0eba3ba9dfa2852df95d9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.6 MB (621598666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd0cefa11659db229d221beca50f3e89b3ed1912cc0bae5999d3444934e5e70`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11754d019316a799ba01b7d7274e18d8fecfddc1f996008b21a8ad547ffd33ff`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691a1fc0a09d3dfb8d49ee79c33145ddeef9efe482c6d2085dfc58a183ec3f15`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 10.0 KB (10031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6783d4a96df097431f1d0849547d8172b0fa8dd05e30653d5b20d2e9d77d12`  
		Last Modified: Fri, 31 Jan 2025 03:35:08 GMT  
		Size: 449.4 MB (449385232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b58cb9221871bdd2b1453b1d16153e100b641dc304ae4238944b350fc8b81893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c12b54766c6af0b8cb64c18e532cd04b63f3697747c881aa13f394ffd4662e`

```dockerfile
```

-	Layers:
	-	`sha256:fa1df9c187013395a5fdf209685d1744d72916d99af0af4f0fe3942663777366`  
		Last Modified: Fri, 31 Jan 2025 03:34:56 GMT  
		Size: 3.5 MB (3537967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff325ceffc2964321da89801218017b7af1b584b6c2b2e7ddc172d2971a2888c`  
		Last Modified: Fri, 31 Jan 2025 03:34:55 GMT  
		Size: 21.6 KB (21577 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:9cda5476927bbdcd9001b3be34b35413904896bc86a9bb0ad23fead363c1bac1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:02588abebf1fd6a982e7b2cb7b80f928532abc499b99dd7a31920c8ee44a9e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.8 MB (619799448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb4967c321091f13fbd664ac973129b49eb45c69df4f76d626208377b7e66a7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6781bd3c11fd8e26fbc353a6dbfc4d8888c6dd2ab14e5c743091c84c25a0554c`  
		Last Modified: Tue, 21 Jan 2025 19:29:35 GMT  
		Size: 133.9 MB (133868620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925455945241f3a6df224f9f3daa6b94240d6a704da5858fe5809c003f08ac4e`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 10.0 KB (10035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab30e64f50685cb3019d3765c33399602cbc9aa2dbd709434f6e3eec5c33fa1`  
		Last Modified: Tue, 21 Jan 2025 19:29:39 GMT  
		Size: 446.5 MB (446487939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:2ba7bd64022113b6b54c131eea41c727d0ad8827875f5ac3706c36312d88cdb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6706816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ce3ee8075ae280dce06d2d6494f1ba50cddd6005d6f8d3670bd94066a462a`

```dockerfile
```

-	Layers:
	-	`sha256:9d64bb2bcd78e986694a9f22a3d4965411b0b316dbcc18dc5c57e0957e190f23`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 6.7 MB (6685457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d3665e9b5fca450d5c677e112ba55c0fb4c2f010b592e63383724f5512496a`  
		Last Modified: Tue, 21 Jan 2025 19:29:33 GMT  
		Size: 21.4 KB (21359 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:966e0b9dace304a11b6e50095bc869f5b7a0cacabc6bb15c008ade266cc48570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.9 MB (617916538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84ecd3da8c3dfd864d856236a378e6986b5b002e6a0e8c638566bb9db3375c8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=1d28455cb116029973d2d51726e3c8afd02d5aa50f6f0bd423298917e958a452 NEO4J_TARBALL=neo4j-enterprise-5.26.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596d13afc954415f8b3e3cb5f77d41d95f3f5e008c24ba504a2ca8108c96a1c1`  
		Last Modified: Tue, 21 Jan 2025 20:28:19 GMT  
		Size: 446.5 MB (446488001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b094bc862fd9f0521e6680debd07f98b140749ef35d89964032dda2bf1e6a002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6686303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0e6e718a94f8044be0e609575ef098048c52184cc4695ebc17de8048ef0460`

```dockerfile
```

-	Layers:
	-	`sha256:8d8bbb90e824c8c9b170503f16f4c2555b77bb502e26dd9d6f2dba985587eb2b`  
		Last Modified: Tue, 21 Jan 2025 20:28:10 GMT  
		Size: 6.7 MB (6664832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0769f336b16d2c1e724496207ddb77ec763b609f095fa88224ccbe8fbcb7479`  
		Last Modified: Tue, 21 Jan 2025 20:28:09 GMT  
		Size: 21.5 KB (21471 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:a5030e84b63dd59c00c5eb8f1c319939bc087b2358734e4fce50abc2a53673bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:a4a0bc7804165f87e81889287c4bca4f5e627c06c0c1224bf340ae1167436fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336742888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7ddae7ccf01286e8de52bd32716394cba88f43f4e0740a3876cb2f62206f28`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 20 Jan 2025 15:28:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9a9c54708d72cfd0ebe5ef19669ccb0f85cc21fb7e9b5836b8fafbd0699da7`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 144.6 MB (144566525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7542fdc5dddfc4c4d9567547afe00f85786c0cabf9637b88bc4be90b2e0d19a5`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34fcf5ec5856bf8963709b4d30c309155fefef344a4b5dc8d0861646c002bfb`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3fbb0cc640d8bf66e7b8db0976d0d03ced415b006ad0fa02ff68ba49b68cb5`  
		Last Modified: Tue, 04 Feb 2025 05:18:51 GMT  
		Size: 161.9 MB (161909871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:29838cc53620747235ff9632ba9da983bf3b80921913c81ad30e387fc93cfb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b54ff20cd85695dce6a72b90c5976475afc68ae268b7d2955f131819eb174e`

```dockerfile
```

-	Layers:
	-	`sha256:e4df5ec885e3f4baf21b99515fa3c2ddc811ff3feb5f37e2ee28b9dc62750895`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 3.2 MB (3229278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca86ebf6c92caa5a4055b9900e738ab64452e4787489d5a804c99aff88e8e418`  
		Last Modified: Tue, 04 Feb 2025 05:18:49 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c1a6110fb48b0becdaa366b1121573567cb94afebbb151ec1182b55e0f071411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334087164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98386221724b1ae3d81c13193356211bb0f794b63af34b5c1a721d6c4c41d492`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 20 Jan 2025 15:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 20 Jan 2025 15:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b19a504f9eee4ffc979315c4a1c0824ec878cbeb0fad1ef4f88158695fc793e`  
		Last Modified: Fri, 31 Jan 2025 03:33:23 GMT  
		Size: 143.5 MB (143454589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1846e25212b8ca453709052081cb0fedd56d7e0530c3d54d1f5cada61485ef23`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d11e9e31aaf51c4c95f8782fd6d79908a1d5b92c92492e0271e4f2ffd7b410`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9093aef0b4eda19b2ece6ab24cda24aa1513763f5954c4f5d4b8d65fe97329f6`  
		Last Modified: Fri, 31 Jan 2025 03:33:24 GMT  
		Size: 161.9 MB (161873728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:226f2e50378ab2d23d955dbd31df9a9061e3f77c12e10c5ca687495c126cfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1db74341c87b096ef37d53eeee4ac52ac920663cd4c9974f7f40c15f57ab1a0`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c2a76033cf8785d712f72c516b71fb678c6fe140267441ef010840fbe8ea3`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 3.2 MB (3229068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2f868997f6817df71e3a80ea8f87d43067e7b1a4dee84e7c1639c32933976e`  
		Last Modified: Fri, 31 Jan 2025 03:33:20 GMT  
		Size: 24.0 KB (24042 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:1e419aff849ae03173f09e16c4f749ba83615e31acaa024d440c03a543cf1de4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:956c82bd140ef18bf56e3d5aec3da71a784d741e5695d2b6cab5253e55c8aeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332290415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c15602b100597031e9c91137eb74a52adb0df57cd516921ebe40fd9b1f8d9c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:41:15 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:41:15 GMT
ENV container oci
# Thu, 09 Jan 2025 06:41:15 GMT
COPY dir:ca56c4399f153561fdce7628edce358895393e72057424065cc9920dd3bc2dfc in / 
# Thu, 09 Jan 2025 06:41:15 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:41:15 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:41:16 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:41:16 GMT
LABEL "build-date"="2025-01-09T06:40:34" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:41:20 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:eeaa3613f51c4b5b7fcccfbff65d07d2d2db56a76e38e2e028020458a3016d3b`  
		Last Modified: Thu, 09 Jan 2025 07:47:12 GMT  
		Size: 39.4 MB (39432422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808a11b7bed4fb0f4e0161a315ca539c1c940faabe1402029784919a7dc4599`  
		Last Modified: Thu, 09 Jan 2025 07:47:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc914da1493d9049c0acbd1a8bf4d2a1addc4f950a238eee02a4c8cb8a6ff6e8`  
		Last Modified: Tue, 21 Jan 2025 19:29:22 GMT  
		Size: 133.9 MB (133868250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6736710fe7f53a64e03a662d3c860fdfc48bd0eb630dcdd726a349cf7717da`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 10.0 KB (10032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c987625061d86c8ffcc30ef53809b182e8cf7c8bfc60d2165413c8137e7057`  
		Last Modified: Tue, 21 Jan 2025 19:29:23 GMT  
		Size: 159.0 MB (158979279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9ed78698fc3f696193f52c11d6b36c3acdb8a30a206f08b86e00fe8f1c08c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee48c6810ed369d57a3eee598b3c21185fa67ce448c948f17c60d7d438e0e50`

```dockerfile
```

-	Layers:
	-	`sha256:9dc15b2397bb49a88990a47ce2924de67f17a9fa1d4134732636864213fe8197`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1345b98e8ee16338f7dcd94270a6cfd06a248077988426a609b5eecdbee253b1`  
		Last Modified: Tue, 21 Jan 2025 19:29:19 GMT  
		Size: 22.5 KB (22536 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:85f5b4b35bf25ba55ab0b1b72d0499b79148efbf09212af9b9bdcc5fd07adb3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330407822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c916a7dc93af0f09c209520aeafc3b1ebb15d03e0af23924945f77d0ea469ace`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL url="https://www.redhat.com"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.expose-services=""
# Thu, 09 Jan 2025 06:40:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 09 Jan 2025 06:40:01 GMT
ENV container oci
# Thu, 09 Jan 2025 06:40:02 GMT
COPY dir:a2d26ebdf33d503cef16329462fc71203b97f5498da2b33d90e85b40b7a5617a in / 
# Thu, 09 Jan 2025 06:40:02 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 09 Jan 2025 06:40:02 GMT
CMD ["/bin/bash"]
# Thu, 09 Jan 2025 06:40:02 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 09 Jan 2025 06:40:03 GMT
LABEL "build-date"="2025-01-09T06:39:36" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="98c9e4c67f5f2dfc85d12e0f1fd70b809f2a3132" "build-date"="2025-01-09T06:29:15Z" "release"="1736404155"
# Thu, 09 Jan 2025 06:40:13 GMT
RUN /bin/sh
# Mon, 20 Jan 2025 15:28:28 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV NEO4J_SHA256=462094a6c53151a312cf56b8a6d350f2ba7df5f7e3d2be033e082df118128fb5 NEO4J_TARBALL=neo4j-community-5.26.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Mon, 20 Jan 2025 15:28:28 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
# Mon, 20 Jan 2025 15:28:28 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.26.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Mon, 20 Jan 2025 15:28:28 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Jan 2025 15:28:28 GMT
WORKDIR /var/lib/neo4j
# Mon, 20 Jan 2025 15:28:28 GMT
VOLUME [/data /logs]
# Mon, 20 Jan 2025 15:28:28 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 20 Jan 2025 15:28:28 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 20 Jan 2025 15:28:28 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:993bfc176cd8d0372914aae800decf36d6fd3b827bddcc23db1ade8868617a10`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 37.6 MB (37577421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9200dd396fa930ba9b5e574dd1a7a802d293946384b1287a63757a8458d18bb`  
		Last Modified: Thu, 09 Jan 2025 07:47:11 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67275633637f076f9378ef3eedf96b512b34ff71801ba42a31470e90b3d48a4d`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 133.8 MB (133840648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a603c9d73dc70c8534dfb3b763d172be8e0f0736a40dbcf69986b90ed439236f`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f6cab068e4386031aa026205ba20abeb203a59805244ddeaf2cc56a55e3359`  
		Last Modified: Tue, 21 Jan 2025 20:27:05 GMT  
		Size: 159.0 MB (158979285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:21731617e98b85e75967d5fc6913962b1d1bd09afc5b4553f35c876935f98657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6377389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d33455d6ec398cf90b4fac4203f8d290add519a53e564830bf111527f00a11`

```dockerfile
```

-	Layers:
	-	`sha256:57a0aa561f73bd19f71c7fa0af923dfd3b96c4d6ae172344e56489a161082650`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd6f044d7d69c1e43bb3007a29d718665226067daafcfcfadf1b3719432d4e61`  
		Last Modified: Tue, 21 Jan 2025 20:27:01 GMT  
		Size: 22.7 KB (22698 bytes)  
		MIME: application/vnd.in-toto+json
