<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.40`](#neo4j4440)
-	[`neo4j:4.4.40-community`](#neo4j4440-community)
-	[`neo4j:4.4.40-enterprise`](#neo4j4440-enterprise)
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
$ docker pull neo4j@sha256:3687b84c5f602aee451b52da6007e1f346abb992e9d7d06d6f22ca91c74eb9e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:fbae07aaf72e6082ce855cc5d343e9c9dc8bf2017ef526b0229074c26eac37fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323182963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9dd05f596b6e5b998ff2690c7d560dfb6f766f391e83a70131c74305393bc6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c3c63b0fc26bf709baaf9ce5d16b99bacccfcf31b8e170043b804ec0d6c948`  
		Last Modified: Thu, 19 Dec 2024 21:31:38 GMT  
		Size: 145.6 MB (145601479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c65b2b6c47ed9da81d97578777d428c3318a1766335b685fdefde7604473c94`  
		Last Modified: Thu, 19 Dec 2024 21:31:34 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543803d51af98631b0663652eabf154af557331b40b2bd11708aebec32eaa6e`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 10.0 KB (9981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbd65ebff2e2a4154e34358dc2eb44f5617948b72b25e559bee13976b3afd0`  
		Last Modified: Thu, 19 Dec 2024 21:31:39 GMT  
		Size: 147.3 MB (147314986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9e3aaa195a0c1185e62ca1a33819165573f2c8719424a9a9f2bcec1434b56eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b4f27c5b33a987763fef9be16aac0be1b86b9cca9a76ee674567467b3b918`

```dockerfile
```

-	Layers:
	-	`sha256:1d21194bf6e22834596040303874f6149daa8d1c0ed2c62e293ec13007225a65`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 3.2 MB (3190657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1635db2313596510eae49365bd76a580f2d3c8f46027e6b5781b03a10f4dd3`  
		Last Modified: Thu, 19 Dec 2024 21:31:34 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1acfa36016e5e979439b16134526892e660322133266932b548d8d10047bd814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318431041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e8cb2a0eeb13c5b22102ea5e20dddbdd7c7a39bde701f953212abefce038e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c43c7dc3627c038c29c9a20adae28736cadb0af9bd4536c9b1adce956dcccb`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 142.4 MB (142389008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0b982dae001b1042a9b612bed4208fa8490753427838c833cd529fd28c962`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 3.9 KB (3871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5ca84e335e14a5c69e947279eecc1fd69ff70e7971d646664c21408d3d6c12`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b610eda39fa954ff9fd543c1d19d22448bd8a23425c5985b8246dec94f4d19bf`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 147.3 MB (147283222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f08e7467a4725e5a2c311e88a9312a1caf71fb562e140f13e0c571fdf2db9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134409233471ef5bed137198106eafa9d5c8f5750da9e4034af950e7185a315c`

```dockerfile
```

-	Layers:
	-	`sha256:e7f2efadb58441bc386e3ec28b88f7df448f446529b1142c3d97a07d80cacc42`  
		Last Modified: Thu, 19 Dec 2024 22:36:45 GMT  
		Size: 3.2 MB (3190921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5615b6b70353d1b0b712b709bf66fa3e99c0c3482817ccfd750ac44e75a6a65f`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:3687b84c5f602aee451b52da6007e1f346abb992e9d7d06d6f22ca91c74eb9e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fbae07aaf72e6082ce855cc5d343e9c9dc8bf2017ef526b0229074c26eac37fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323182963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9dd05f596b6e5b998ff2690c7d560dfb6f766f391e83a70131c74305393bc6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c3c63b0fc26bf709baaf9ce5d16b99bacccfcf31b8e170043b804ec0d6c948`  
		Last Modified: Thu, 19 Dec 2024 21:31:38 GMT  
		Size: 145.6 MB (145601479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c65b2b6c47ed9da81d97578777d428c3318a1766335b685fdefde7604473c94`  
		Last Modified: Thu, 19 Dec 2024 21:31:34 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543803d51af98631b0663652eabf154af557331b40b2bd11708aebec32eaa6e`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 10.0 KB (9981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbd65ebff2e2a4154e34358dc2eb44f5617948b72b25e559bee13976b3afd0`  
		Last Modified: Thu, 19 Dec 2024 21:31:39 GMT  
		Size: 147.3 MB (147314986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9e3aaa195a0c1185e62ca1a33819165573f2c8719424a9a9f2bcec1434b56eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b4f27c5b33a987763fef9be16aac0be1b86b9cca9a76ee674567467b3b918`

```dockerfile
```

-	Layers:
	-	`sha256:1d21194bf6e22834596040303874f6149daa8d1c0ed2c62e293ec13007225a65`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 3.2 MB (3190657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1635db2313596510eae49365bd76a580f2d3c8f46027e6b5781b03a10f4dd3`  
		Last Modified: Thu, 19 Dec 2024 21:31:34 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1acfa36016e5e979439b16134526892e660322133266932b548d8d10047bd814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318431041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e8cb2a0eeb13c5b22102ea5e20dddbdd7c7a39bde701f953212abefce038e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c43c7dc3627c038c29c9a20adae28736cadb0af9bd4536c9b1adce956dcccb`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 142.4 MB (142389008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0b982dae001b1042a9b612bed4208fa8490753427838c833cd529fd28c962`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 3.9 KB (3871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5ca84e335e14a5c69e947279eecc1fd69ff70e7971d646664c21408d3d6c12`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b610eda39fa954ff9fd543c1d19d22448bd8a23425c5985b8246dec94f4d19bf`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 147.3 MB (147283222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f08e7467a4725e5a2c311e88a9312a1caf71fb562e140f13e0c571fdf2db9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134409233471ef5bed137198106eafa9d5c8f5750da9e4034af950e7185a315c`

```dockerfile
```

-	Layers:
	-	`sha256:e7f2efadb58441bc386e3ec28b88f7df448f446529b1142c3d97a07d80cacc42`  
		Last Modified: Thu, 19 Dec 2024 22:36:45 GMT  
		Size: 3.2 MB (3190921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5615b6b70353d1b0b712b709bf66fa3e99c0c3482817ccfd750ac44e75a6a65f`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:c2a9e861a5fd3b9670985df3ffff83cf82fc0366a97e00f1ef3e8b43616ab374
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:117034ed0d9f1f7b6a472dd7b5677e0963c2064ecbd4710e76aed7db0320c402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.1 MB (425103801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234c0f9a934bc1950a4e6d15c6d382fbc74dd41caadfd338afa255b7d936c3f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9342a9a89be1598a218b155fa6924be63f709c5a7278d2704869e0586b489`  
		Last Modified: Thu, 19 Dec 2024 21:31:58 GMT  
		Size: 145.6 MB (145601479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3d1f7822eb09e787d3ea13b960895f84c6083e10141733258f0b91cdcb67b9`  
		Last Modified: Thu, 19 Dec 2024 21:31:55 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2273a89ac4e9ed4364badb838287bc1f298724cdd77e2fb5195c1852bed21077`  
		Last Modified: Thu, 19 Dec 2024 21:31:54 GMT  
		Size: 10.0 KB (9983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df2a25a8bd9b34707c524cfd6c914b8266ccbd5399b9cbcf18a577cbf6a68db`  
		Last Modified: Thu, 19 Dec 2024 21:32:00 GMT  
		Size: 249.2 MB (249235823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:cabdfbe000c80a8c0f1c8b282c49178694ab93658b3504bfa99346bc8454f8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103bed1e8a6bd8c8886cbe36f3e12d84ec121cca0de89dc0be3f8f7fb60cb3e4`

```dockerfile
```

-	Layers:
	-	`sha256:25ac56b7d4b60f98e55e1ef1b1b4ebc8db3a8a460d3c1c35fb2cd06df8b1490e`  
		Last Modified: Thu, 19 Dec 2024 21:31:55 GMT  
		Size: 3.3 MB (3339066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d65ee52f44a80bacb9d99f117cf59c5d78d1e24598672b38ed99d4520c4dde0`  
		Last Modified: Thu, 19 Dec 2024 21:31:55 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d5584b8ac0d25316a4d3b7f07b1af58359372d2c0a61c6b213d329b2eebf0a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.4 MB (420350263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f655c36c98e23dba091004e4ec4a834d1ce30ea292dcaded4d8da1feb0479e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c43c7dc3627c038c29c9a20adae28736cadb0af9bd4536c9b1adce956dcccb`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 142.4 MB (142389008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9bd5d069439a9dfb646ba6bf67cb2196f4dfddd4c61ac8ef091d7a4c725f61`  
		Last Modified: Thu, 19 Dec 2024 22:37:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3e5434c8c9a9fb9646aace774bcce0184eb65614eef733df5ddd4ac4529b04`  
		Last Modified: Thu, 19 Dec 2024 22:37:54 GMT  
		Size: 10.0 KB (9978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0d4a39f11314524329eeb207a2bcd8769d5be7735dfe41aa1ae05c2a0768c8`  
		Last Modified: Thu, 19 Dec 2024 22:38:00 GMT  
		Size: 249.2 MB (249202455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4cfc93774cbb30255c1507e5df33bd25e931b883e4b02b24534f05a778d437c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1943b8555aaac12f5e864fdaeac122942259bd3682f9131f74c525676db726e7`

```dockerfile
```

-	Layers:
	-	`sha256:f2b1da3edb78c306143bc5cf5aa3bb5f20136c9ca5e9e791fdf317bc007369fe`  
		Last Modified: Thu, 19 Dec 2024 22:37:55 GMT  
		Size: 3.3 MB (3339306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b470514bb377948e3b14205211a465906e34bbf901b8ea52babc59c79f3da18`  
		Last Modified: Thu, 19 Dec 2024 22:37:54 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.40`

```console
$ docker pull neo4j@sha256:3687b84c5f602aee451b52da6007e1f346abb992e9d7d06d6f22ca91c74eb9e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.40` - linux; amd64

```console
$ docker pull neo4j@sha256:fbae07aaf72e6082ce855cc5d343e9c9dc8bf2017ef526b0229074c26eac37fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323182963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9dd05f596b6e5b998ff2690c7d560dfb6f766f391e83a70131c74305393bc6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c3c63b0fc26bf709baaf9ce5d16b99bacccfcf31b8e170043b804ec0d6c948`  
		Last Modified: Thu, 19 Dec 2024 21:31:38 GMT  
		Size: 145.6 MB (145601479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c65b2b6c47ed9da81d97578777d428c3318a1766335b685fdefde7604473c94`  
		Last Modified: Thu, 19 Dec 2024 21:31:34 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543803d51af98631b0663652eabf154af557331b40b2bd11708aebec32eaa6e`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 10.0 KB (9981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbd65ebff2e2a4154e34358dc2eb44f5617948b72b25e559bee13976b3afd0`  
		Last Modified: Thu, 19 Dec 2024 21:31:39 GMT  
		Size: 147.3 MB (147314986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.40` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9e3aaa195a0c1185e62ca1a33819165573f2c8719424a9a9f2bcec1434b56eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b4f27c5b33a987763fef9be16aac0be1b86b9cca9a76ee674567467b3b918`

```dockerfile
```

-	Layers:
	-	`sha256:1d21194bf6e22834596040303874f6149daa8d1c0ed2c62e293ec13007225a65`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 3.2 MB (3190657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1635db2313596510eae49365bd76a580f2d3c8f46027e6b5781b03a10f4dd3`  
		Last Modified: Thu, 19 Dec 2024 21:31:34 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.40` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1acfa36016e5e979439b16134526892e660322133266932b548d8d10047bd814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318431041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e8cb2a0eeb13c5b22102ea5e20dddbdd7c7a39bde701f953212abefce038e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c43c7dc3627c038c29c9a20adae28736cadb0af9bd4536c9b1adce956dcccb`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 142.4 MB (142389008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0b982dae001b1042a9b612bed4208fa8490753427838c833cd529fd28c962`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 3.9 KB (3871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5ca84e335e14a5c69e947279eecc1fd69ff70e7971d646664c21408d3d6c12`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b610eda39fa954ff9fd543c1d19d22448bd8a23425c5985b8246dec94f4d19bf`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 147.3 MB (147283222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.40` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f08e7467a4725e5a2c311e88a9312a1caf71fb562e140f13e0c571fdf2db9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134409233471ef5bed137198106eafa9d5c8f5750da9e4034af950e7185a315c`

```dockerfile
```

-	Layers:
	-	`sha256:e7f2efadb58441bc386e3ec28b88f7df448f446529b1142c3d97a07d80cacc42`  
		Last Modified: Thu, 19 Dec 2024 22:36:45 GMT  
		Size: 3.2 MB (3190921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5615b6b70353d1b0b712b709bf66fa3e99c0c3482817ccfd750ac44e75a6a65f`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.40-community`

```console
$ docker pull neo4j@sha256:3687b84c5f602aee451b52da6007e1f346abb992e9d7d06d6f22ca91c74eb9e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.40-community` - linux; amd64

```console
$ docker pull neo4j@sha256:fbae07aaf72e6082ce855cc5d343e9c9dc8bf2017ef526b0229074c26eac37fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323182963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9dd05f596b6e5b998ff2690c7d560dfb6f766f391e83a70131c74305393bc6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c3c63b0fc26bf709baaf9ce5d16b99bacccfcf31b8e170043b804ec0d6c948`  
		Last Modified: Thu, 19 Dec 2024 21:31:38 GMT  
		Size: 145.6 MB (145601479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c65b2b6c47ed9da81d97578777d428c3318a1766335b685fdefde7604473c94`  
		Last Modified: Thu, 19 Dec 2024 21:31:34 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543803d51af98631b0663652eabf154af557331b40b2bd11708aebec32eaa6e`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 10.0 KB (9981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bbd65ebff2e2a4154e34358dc2eb44f5617948b72b25e559bee13976b3afd0`  
		Last Modified: Thu, 19 Dec 2024 21:31:39 GMT  
		Size: 147.3 MB (147314986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.40-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b9e3aaa195a0c1185e62ca1a33819165573f2c8719424a9a9f2bcec1434b56eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3210613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839b4f27c5b33a987763fef9be16aac0be1b86b9cca9a76ee674567467b3b918`

```dockerfile
```

-	Layers:
	-	`sha256:1d21194bf6e22834596040303874f6149daa8d1c0ed2c62e293ec13007225a65`  
		Last Modified: Thu, 19 Dec 2024 21:31:35 GMT  
		Size: 3.2 MB (3190657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1635db2313596510eae49365bd76a580f2d3c8f46027e6b5781b03a10f4dd3`  
		Last Modified: Thu, 19 Dec 2024 21:31:34 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.40-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1acfa36016e5e979439b16134526892e660322133266932b548d8d10047bd814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318431041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e8cb2a0eeb13c5b22102ea5e20dddbdd7c7a39bde701f953212abefce038e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c43c7dc3627c038c29c9a20adae28736cadb0af9bd4536c9b1adce956dcccb`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 142.4 MB (142389008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0b982dae001b1042a9b612bed4208fa8490753427838c833cd529fd28c962`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 3.9 KB (3871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5ca84e335e14a5c69e947279eecc1fd69ff70e7971d646664c21408d3d6c12`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 10.0 KB (9985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b610eda39fa954ff9fd543c1d19d22448bd8a23425c5985b8246dec94f4d19bf`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 147.3 MB (147283222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.40-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0f08e7467a4725e5a2c311e88a9312a1caf71fb562e140f13e0c571fdf2db9e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3211023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134409233471ef5bed137198106eafa9d5c8f5750da9e4034af950e7185a315c`

```dockerfile
```

-	Layers:
	-	`sha256:e7f2efadb58441bc386e3ec28b88f7df448f446529b1142c3d97a07d80cacc42`  
		Last Modified: Thu, 19 Dec 2024 22:36:45 GMT  
		Size: 3.2 MB (3190921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5615b6b70353d1b0b712b709bf66fa3e99c0c3482817ccfd750ac44e75a6a65f`  
		Last Modified: Thu, 19 Dec 2024 22:36:44 GMT  
		Size: 20.1 KB (20102 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.40-enterprise`

```console
$ docker pull neo4j@sha256:c2a9e861a5fd3b9670985df3ffff83cf82fc0366a97e00f1ef3e8b43616ab374
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.40-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:117034ed0d9f1f7b6a472dd7b5677e0963c2064ecbd4710e76aed7db0320c402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.1 MB (425103801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234c0f9a934bc1950a4e6d15c6d382fbc74dd41caadfd338afa255b7d936c3f0`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9342a9a89be1598a218b155fa6924be63f709c5a7278d2704869e0586b489`  
		Last Modified: Thu, 19 Dec 2024 21:31:58 GMT  
		Size: 145.6 MB (145601479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3d1f7822eb09e787d3ea13b960895f84c6083e10141733258f0b91cdcb67b9`  
		Last Modified: Thu, 19 Dec 2024 21:31:55 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2273a89ac4e9ed4364badb838287bc1f298724cdd77e2fb5195c1852bed21077`  
		Last Modified: Thu, 19 Dec 2024 21:31:54 GMT  
		Size: 10.0 KB (9983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df2a25a8bd9b34707c524cfd6c914b8266ccbd5399b9cbcf18a577cbf6a68db`  
		Last Modified: Thu, 19 Dec 2024 21:32:00 GMT  
		Size: 249.2 MB (249235823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.40-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:cabdfbe000c80a8c0f1c8b282c49178694ab93658b3504bfa99346bc8454f8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103bed1e8a6bd8c8886cbe36f3e12d84ec121cca0de89dc0be3f8f7fb60cb3e4`

```dockerfile
```

-	Layers:
	-	`sha256:25ac56b7d4b60f98e55e1ef1b1b4ebc8db3a8a460d3c1c35fb2cd06df8b1490e`  
		Last Modified: Thu, 19 Dec 2024 21:31:55 GMT  
		Size: 3.3 MB (3339066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d65ee52f44a80bacb9d99f117cf59c5d78d1e24598672b38ed99d4520c4dde0`  
		Last Modified: Thu, 19 Dec 2024 21:31:55 GMT  
		Size: 19.4 KB (19388 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.40-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d5584b8ac0d25316a4d3b7f07b1af58359372d2c0a61c6b213d329b2eebf0a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.4 MB (420350263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f655c36c98e23dba091004e4ec4a834d1ce30ea292dcaded4d8da1feb0479e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Mon, 02 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c43c7dc3627c038c29c9a20adae28736cadb0af9bd4536c9b1adce956dcccb`  
		Last Modified: Thu, 19 Dec 2024 22:36:48 GMT  
		Size: 142.4 MB (142389008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9bd5d069439a9dfb646ba6bf67cb2196f4dfddd4c61ac8ef091d7a4c725f61`  
		Last Modified: Thu, 19 Dec 2024 22:37:54 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3e5434c8c9a9fb9646aace774bcce0184eb65614eef733df5ddd4ac4529b04`  
		Last Modified: Thu, 19 Dec 2024 22:37:54 GMT  
		Size: 10.0 KB (9978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0d4a39f11314524329eeb207a2bcd8769d5be7735dfe41aa1ae05c2a0768c8`  
		Last Modified: Thu, 19 Dec 2024 22:38:00 GMT  
		Size: 249.2 MB (249202455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.40-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:4cfc93774cbb30255c1507e5df33bd25e931b883e4b02b24534f05a778d437c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3358815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1943b8555aaac12f5e864fdaeac122942259bd3682f9131f74c525676db726e7`

```dockerfile
```

-	Layers:
	-	`sha256:f2b1da3edb78c306143bc5cf5aa3bb5f20136c9ca5e9e791fdf317bc007369fe`  
		Last Modified: Thu, 19 Dec 2024 22:37:55 GMT  
		Size: 3.3 MB (3339306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b470514bb377948e3b14205211a465906e34bbf901b8ea52babc59c79f3da18`  
		Last Modified: Thu, 19 Dec 2024 22:37:54 GMT  
		Size: 19.5 KB (19509 bytes)  
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
$ docker pull neo4j@sha256:a90439b6b0b1ac393983f4287c5ca3727c68936bb517bf701c058c5413d1b0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1870ed6a2684880ad99ed226a87c01b99b89a301821342c1f49cdd2eba945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332281997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3649debdcab197938b4fe5c708c919ea488d1b435f7db2350046f4152a9ce6`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354187e0d6a01833883ba8539ece581102bed9b5e2f6ace00107c9c502fa249f`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 133.9 MB (133864896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b55efc172ac6f8bd17c3560911e50854c3420214bc2a1c1e8d51deb4910685`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48780c92dcc75e3c87cd57a77ef0753e92e715ce2a7fe147035c3330782992`  
		Last Modified: Thu, 19 Dec 2024 06:28:40 GMT  
		Size: 159.0 MB (158974626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c10ffa3943eec40c973f1f619b557039de44f845748a74e567679266060d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18cb8ad7c102e2911dfa1bf7fb9981c8ff8faa1934aa558c4ffb77d7a180bf`

```dockerfile
```

-	Layers:
	-	`sha256:31b54c83fefef66d103d15813062c501925e009289093f013e4f872f23d679e8`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c672bab58d7edcd5c1b880afbebd9250a5190740ddddd6dcf3961b19caa1f2fe`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5c3aae55cfbd373038f4d196353dc819d8f929d2d1268629c33fde830354ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330402411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d6a0bf1881f306df5dba8481621afbbb2545a4388194904db2f36906b73627`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1c3a2df462ad32949d3883ba9d9d13c6b74c628eab0adea2da713a53d6200`  
		Last Modified: Thu, 19 Dec 2024 06:48:30 GMT  
		Size: 159.0 MB (158974651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5816cfc0f21f741552310c118e41298a65b565bc6db32f9dde1106bf73666a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6376619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2a5a0c0f76203956d43b2ae9d98c8135897d5c62ef2f0afcdb2e049673031`

```dockerfile
```

-	Layers:
	-	`sha256:eca51ca055b407b5e512fedeb674d7e9782f25713b0ca11c15394e659b9268b0`  
		Last Modified: Thu, 19 Dec 2024 06:48:27 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c88e2a670c3015c330ef7980e884d2c7a10e545bffc98e619bef87d8db3bf3d`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
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
$ docker pull neo4j@sha256:9f08c929f592658714859ed70b974205fa8d196dbb132f2ea5ddf801493a3a78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:42160d4e26da63343ee660812ecb919119cee7be4cc5e275e9be56d35d236012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (620031069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dad9d96dd1e07a9579ed22a00937c6c4af9afa75d610be1432cb2f2966769d9`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58206fe82bc7bbcbfebfe8cd78f50119ccb22a9273c088ee856de5402f7914ef`  
		Last Modified: Thu, 19 Dec 2024 06:28:41 GMT  
		Size: 133.9 MB (133868780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99cb19e7c8bda459fcc2bcc8e995234b76845d8f86fe201b3ff72860775f42`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e11fc9276f3b98b27c0a427de033c8c85af9e3dea4aaa84462ed870a249479`  
		Last Modified: Thu, 19 Dec 2024 06:28:45 GMT  
		Size: 446.7 MB (446719818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca1260361075f7df7bd373b8b30087e44046880fba2ce068b51e1091f8eca780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6706046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8313dba0f00e75976fc14cb368cf4ac582be0e153a0cc8782e7631f533c096b6`

```dockerfile
```

-	Layers:
	-	`sha256:5db7c191c5318c2c18faee07ab151fbb3ccc6c8b8c696c45717582d038b76347`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 6.7 MB (6685457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb25cf80a52736208da5ed15f4692be15b7750701985a2c20ce9ce66b2d9ad4`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 20.6 KB (20589 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:75b23b009902f6395a3aca1b5261f16f62bd7917feaac4247a1d0b928240fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.1 MB (618147551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb91915f28bab4034a640453f36a2e0e17cc4159a2caa3e96dbbc1fb4676c3cd`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1ef7a7cf2bec238d9481b96f5f88bc3c3d1c057e99687db1e858ea06385738`  
		Last Modified: Thu, 19 Dec 2024 06:49:39 GMT  
		Size: 446.7 MB (446719791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:dd8f92a2c4c8e1c79fe37b506c134ff75e858ca8763e6039b8a9b3b5c5ef3ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27367b175f928a29a72b27f868ad8a10e2b226d207a3ecdd751e2596734996b`

```dockerfile
```

-	Layers:
	-	`sha256:8666af547a0d3ddd14639cb8a9804d673aca6f1d08ec4b1cd4bf5a9632fae04e`  
		Last Modified: Thu, 19 Dec 2024 06:49:30 GMT  
		Size: 6.7 MB (6664832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1666b2723fabfb7c6e4ef2dabc6e0892937adcc113a57b781d07073c37a65860`  
		Last Modified: Thu, 19 Dec 2024 06:49:30 GMT  
		Size: 20.7 KB (20702 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:a90439b6b0b1ac393983f4287c5ca3727c68936bb517bf701c058c5413d1b0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1870ed6a2684880ad99ed226a87c01b99b89a301821342c1f49cdd2eba945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332281997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3649debdcab197938b4fe5c708c919ea488d1b435f7db2350046f4152a9ce6`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354187e0d6a01833883ba8539ece581102bed9b5e2f6ace00107c9c502fa249f`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 133.9 MB (133864896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b55efc172ac6f8bd17c3560911e50854c3420214bc2a1c1e8d51deb4910685`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48780c92dcc75e3c87cd57a77ef0753e92e715ce2a7fe147035c3330782992`  
		Last Modified: Thu, 19 Dec 2024 06:28:40 GMT  
		Size: 159.0 MB (158974626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c10ffa3943eec40c973f1f619b557039de44f845748a74e567679266060d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18cb8ad7c102e2911dfa1bf7fb9981c8ff8faa1934aa558c4ffb77d7a180bf`

```dockerfile
```

-	Layers:
	-	`sha256:31b54c83fefef66d103d15813062c501925e009289093f013e4f872f23d679e8`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c672bab58d7edcd5c1b880afbebd9250a5190740ddddd6dcf3961b19caa1f2fe`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5c3aae55cfbd373038f4d196353dc819d8f929d2d1268629c33fde830354ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330402411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d6a0bf1881f306df5dba8481621afbbb2545a4388194904db2f36906b73627`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1c3a2df462ad32949d3883ba9d9d13c6b74c628eab0adea2da713a53d6200`  
		Last Modified: Thu, 19 Dec 2024 06:48:30 GMT  
		Size: 159.0 MB (158974651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5816cfc0f21f741552310c118e41298a65b565bc6db32f9dde1106bf73666a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6376619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2a5a0c0f76203956d43b2ae9d98c8135897d5c62ef2f0afcdb2e049673031`

```dockerfile
```

-	Layers:
	-	`sha256:eca51ca055b407b5e512fedeb674d7e9782f25713b0ca11c15394e659b9268b0`  
		Last Modified: Thu, 19 Dec 2024 06:48:27 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c88e2a670c3015c330ef7980e884d2c7a10e545bffc98e619bef87d8db3bf3d`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
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
$ docker pull neo4j@sha256:a90439b6b0b1ac393983f4287c5ca3727c68936bb517bf701c058c5413d1b0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1870ed6a2684880ad99ed226a87c01b99b89a301821342c1f49cdd2eba945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332281997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3649debdcab197938b4fe5c708c919ea488d1b435f7db2350046f4152a9ce6`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354187e0d6a01833883ba8539ece581102bed9b5e2f6ace00107c9c502fa249f`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 133.9 MB (133864896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b55efc172ac6f8bd17c3560911e50854c3420214bc2a1c1e8d51deb4910685`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48780c92dcc75e3c87cd57a77ef0753e92e715ce2a7fe147035c3330782992`  
		Last Modified: Thu, 19 Dec 2024 06:28:40 GMT  
		Size: 159.0 MB (158974626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c10ffa3943eec40c973f1f619b557039de44f845748a74e567679266060d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18cb8ad7c102e2911dfa1bf7fb9981c8ff8faa1934aa558c4ffb77d7a180bf`

```dockerfile
```

-	Layers:
	-	`sha256:31b54c83fefef66d103d15813062c501925e009289093f013e4f872f23d679e8`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c672bab58d7edcd5c1b880afbebd9250a5190740ddddd6dcf3961b19caa1f2fe`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5c3aae55cfbd373038f4d196353dc819d8f929d2d1268629c33fde830354ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330402411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d6a0bf1881f306df5dba8481621afbbb2545a4388194904db2f36906b73627`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1c3a2df462ad32949d3883ba9d9d13c6b74c628eab0adea2da713a53d6200`  
		Last Modified: Thu, 19 Dec 2024 06:48:30 GMT  
		Size: 159.0 MB (158974651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5816cfc0f21f741552310c118e41298a65b565bc6db32f9dde1106bf73666a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6376619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2a5a0c0f76203956d43b2ae9d98c8135897d5c62ef2f0afcdb2e049673031`

```dockerfile
```

-	Layers:
	-	`sha256:eca51ca055b407b5e512fedeb674d7e9782f25713b0ca11c15394e659b9268b0`  
		Last Modified: Thu, 19 Dec 2024 06:48:27 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c88e2a670c3015c330ef7980e884d2c7a10e545bffc98e619bef87d8db3bf3d`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
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
$ docker pull neo4j@sha256:9f08c929f592658714859ed70b974205fa8d196dbb132f2ea5ddf801493a3a78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:42160d4e26da63343ee660812ecb919119cee7be4cc5e275e9be56d35d236012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (620031069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dad9d96dd1e07a9579ed22a00937c6c4af9afa75d610be1432cb2f2966769d9`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58206fe82bc7bbcbfebfe8cd78f50119ccb22a9273c088ee856de5402f7914ef`  
		Last Modified: Thu, 19 Dec 2024 06:28:41 GMT  
		Size: 133.9 MB (133868780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99cb19e7c8bda459fcc2bcc8e995234b76845d8f86fe201b3ff72860775f42`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e11fc9276f3b98b27c0a427de033c8c85af9e3dea4aaa84462ed870a249479`  
		Last Modified: Thu, 19 Dec 2024 06:28:45 GMT  
		Size: 446.7 MB (446719818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca1260361075f7df7bd373b8b30087e44046880fba2ce068b51e1091f8eca780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6706046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8313dba0f00e75976fc14cb368cf4ac582be0e153a0cc8782e7631f533c096b6`

```dockerfile
```

-	Layers:
	-	`sha256:5db7c191c5318c2c18faee07ab151fbb3ccc6c8b8c696c45717582d038b76347`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 6.7 MB (6685457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb25cf80a52736208da5ed15f4692be15b7750701985a2c20ce9ce66b2d9ad4`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 20.6 KB (20589 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:75b23b009902f6395a3aca1b5261f16f62bd7917feaac4247a1d0b928240fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.1 MB (618147551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb91915f28bab4034a640453f36a2e0e17cc4159a2caa3e96dbbc1fb4676c3cd`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1ef7a7cf2bec238d9481b96f5f88bc3c3d1c057e99687db1e858ea06385738`  
		Last Modified: Thu, 19 Dec 2024 06:49:39 GMT  
		Size: 446.7 MB (446719791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:dd8f92a2c4c8e1c79fe37b506c134ff75e858ca8763e6039b8a9b3b5c5ef3ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27367b175f928a29a72b27f868ad8a10e2b226d207a3ecdd751e2596734996b`

```dockerfile
```

-	Layers:
	-	`sha256:8666af547a0d3ddd14639cb8a9804d673aca6f1d08ec4b1cd4bf5a9632fae04e`  
		Last Modified: Thu, 19 Dec 2024 06:49:30 GMT  
		Size: 6.7 MB (6664832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1666b2723fabfb7c6e4ef2dabc6e0892937adcc113a57b781d07073c37a65860`  
		Last Modified: Thu, 19 Dec 2024 06:49:30 GMT  
		Size: 20.7 KB (20702 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26-ubi9`

```console
$ docker pull neo4j@sha256:a90439b6b0b1ac393983f4287c5ca3727c68936bb517bf701c058c5413d1b0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1870ed6a2684880ad99ed226a87c01b99b89a301821342c1f49cdd2eba945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332281997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3649debdcab197938b4fe5c708c919ea488d1b435f7db2350046f4152a9ce6`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354187e0d6a01833883ba8539ece581102bed9b5e2f6ace00107c9c502fa249f`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 133.9 MB (133864896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b55efc172ac6f8bd17c3560911e50854c3420214bc2a1c1e8d51deb4910685`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48780c92dcc75e3c87cd57a77ef0753e92e715ce2a7fe147035c3330782992`  
		Last Modified: Thu, 19 Dec 2024 06:28:40 GMT  
		Size: 159.0 MB (158974626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c10ffa3943eec40c973f1f619b557039de44f845748a74e567679266060d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18cb8ad7c102e2911dfa1bf7fb9981c8ff8faa1934aa558c4ffb77d7a180bf`

```dockerfile
```

-	Layers:
	-	`sha256:31b54c83fefef66d103d15813062c501925e009289093f013e4f872f23d679e8`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c672bab58d7edcd5c1b880afbebd9250a5190740ddddd6dcf3961b19caa1f2fe`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5c3aae55cfbd373038f4d196353dc819d8f929d2d1268629c33fde830354ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330402411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d6a0bf1881f306df5dba8481621afbbb2545a4388194904db2f36906b73627`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1c3a2df462ad32949d3883ba9d9d13c6b74c628eab0adea2da713a53d6200`  
		Last Modified: Thu, 19 Dec 2024 06:48:30 GMT  
		Size: 159.0 MB (158974651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5816cfc0f21f741552310c118e41298a65b565bc6db32f9dde1106bf73666a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6376619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2a5a0c0f76203956d43b2ae9d98c8135897d5c62ef2f0afcdb2e049673031`

```dockerfile
```

-	Layers:
	-	`sha256:eca51ca055b407b5e512fedeb674d7e9782f25713b0ca11c15394e659b9268b0`  
		Last Modified: Thu, 19 Dec 2024 06:48:27 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c88e2a670c3015c330ef7980e884d2c7a10e545bffc98e619bef87d8db3bf3d`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
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
$ docker pull neo4j@sha256:a90439b6b0b1ac393983f4287c5ca3727c68936bb517bf701c058c5413d1b0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1870ed6a2684880ad99ed226a87c01b99b89a301821342c1f49cdd2eba945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332281997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3649debdcab197938b4fe5c708c919ea488d1b435f7db2350046f4152a9ce6`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354187e0d6a01833883ba8539ece581102bed9b5e2f6ace00107c9c502fa249f`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 133.9 MB (133864896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b55efc172ac6f8bd17c3560911e50854c3420214bc2a1c1e8d51deb4910685`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48780c92dcc75e3c87cd57a77ef0753e92e715ce2a7fe147035c3330782992`  
		Last Modified: Thu, 19 Dec 2024 06:28:40 GMT  
		Size: 159.0 MB (158974626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c10ffa3943eec40c973f1f619b557039de44f845748a74e567679266060d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18cb8ad7c102e2911dfa1bf7fb9981c8ff8faa1934aa558c4ffb77d7a180bf`

```dockerfile
```

-	Layers:
	-	`sha256:31b54c83fefef66d103d15813062c501925e009289093f013e4f872f23d679e8`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c672bab58d7edcd5c1b880afbebd9250a5190740ddddd6dcf3961b19caa1f2fe`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5c3aae55cfbd373038f4d196353dc819d8f929d2d1268629c33fde830354ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330402411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d6a0bf1881f306df5dba8481621afbbb2545a4388194904db2f36906b73627`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1c3a2df462ad32949d3883ba9d9d13c6b74c628eab0adea2da713a53d6200`  
		Last Modified: Thu, 19 Dec 2024 06:48:30 GMT  
		Size: 159.0 MB (158974651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5816cfc0f21f741552310c118e41298a65b565bc6db32f9dde1106bf73666a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6376619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2a5a0c0f76203956d43b2ae9d98c8135897d5c62ef2f0afcdb2e049673031`

```dockerfile
```

-	Layers:
	-	`sha256:eca51ca055b407b5e512fedeb674d7e9782f25713b0ca11c15394e659b9268b0`  
		Last Modified: Thu, 19 Dec 2024 06:48:27 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c88e2a670c3015c330ef7980e884d2c7a10e545bffc98e619bef87d8db3bf3d`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
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
$ docker pull neo4j@sha256:9f08c929f592658714859ed70b974205fa8d196dbb132f2ea5ddf801493a3a78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:42160d4e26da63343ee660812ecb919119cee7be4cc5e275e9be56d35d236012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (620031069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dad9d96dd1e07a9579ed22a00937c6c4af9afa75d610be1432cb2f2966769d9`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58206fe82bc7bbcbfebfe8cd78f50119ccb22a9273c088ee856de5402f7914ef`  
		Last Modified: Thu, 19 Dec 2024 06:28:41 GMT  
		Size: 133.9 MB (133868780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99cb19e7c8bda459fcc2bcc8e995234b76845d8f86fe201b3ff72860775f42`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e11fc9276f3b98b27c0a427de033c8c85af9e3dea4aaa84462ed870a249479`  
		Last Modified: Thu, 19 Dec 2024 06:28:45 GMT  
		Size: 446.7 MB (446719818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca1260361075f7df7bd373b8b30087e44046880fba2ce068b51e1091f8eca780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6706046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8313dba0f00e75976fc14cb368cf4ac582be0e153a0cc8782e7631f533c096b6`

```dockerfile
```

-	Layers:
	-	`sha256:5db7c191c5318c2c18faee07ab151fbb3ccc6c8b8c696c45717582d038b76347`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 6.7 MB (6685457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb25cf80a52736208da5ed15f4692be15b7750701985a2c20ce9ce66b2d9ad4`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 20.6 KB (20589 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:75b23b009902f6395a3aca1b5261f16f62bd7917feaac4247a1d0b928240fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.1 MB (618147551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb91915f28bab4034a640453f36a2e0e17cc4159a2caa3e96dbbc1fb4676c3cd`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1ef7a7cf2bec238d9481b96f5f88bc3c3d1c057e99687db1e858ea06385738`  
		Last Modified: Thu, 19 Dec 2024 06:49:39 GMT  
		Size: 446.7 MB (446719791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:dd8f92a2c4c8e1c79fe37b506c134ff75e858ca8763e6039b8a9b3b5c5ef3ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27367b175f928a29a72b27f868ad8a10e2b226d207a3ecdd751e2596734996b`

```dockerfile
```

-	Layers:
	-	`sha256:8666af547a0d3ddd14639cb8a9804d673aca6f1d08ec4b1cd4bf5a9632fae04e`  
		Last Modified: Thu, 19 Dec 2024 06:49:30 GMT  
		Size: 6.7 MB (6664832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1666b2723fabfb7c6e4ef2dabc6e0892937adcc113a57b781d07073c37a65860`  
		Last Modified: Thu, 19 Dec 2024 06:49:30 GMT  
		Size: 20.7 KB (20702 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.26.0-ubi9`

```console
$ docker pull neo4j@sha256:a90439b6b0b1ac393983f4287c5ca3727c68936bb517bf701c058c5413d1b0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.26.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1870ed6a2684880ad99ed226a87c01b99b89a301821342c1f49cdd2eba945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332281997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3649debdcab197938b4fe5c708c919ea488d1b435f7db2350046f4152a9ce6`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354187e0d6a01833883ba8539ece581102bed9b5e2f6ace00107c9c502fa249f`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 133.9 MB (133864896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b55efc172ac6f8bd17c3560911e50854c3420214bc2a1c1e8d51deb4910685`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48780c92dcc75e3c87cd57a77ef0753e92e715ce2a7fe147035c3330782992`  
		Last Modified: Thu, 19 Dec 2024 06:28:40 GMT  
		Size: 159.0 MB (158974626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c10ffa3943eec40c973f1f619b557039de44f845748a74e567679266060d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18cb8ad7c102e2911dfa1bf7fb9981c8ff8faa1934aa558c4ffb77d7a180bf`

```dockerfile
```

-	Layers:
	-	`sha256:31b54c83fefef66d103d15813062c501925e009289093f013e4f872f23d679e8`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c672bab58d7edcd5c1b880afbebd9250a5190740ddddd6dcf3961b19caa1f2fe`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.26.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5c3aae55cfbd373038f4d196353dc819d8f929d2d1268629c33fde830354ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330402411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d6a0bf1881f306df5dba8481621afbbb2545a4388194904db2f36906b73627`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1c3a2df462ad32949d3883ba9d9d13c6b74c628eab0adea2da713a53d6200`  
		Last Modified: Thu, 19 Dec 2024 06:48:30 GMT  
		Size: 159.0 MB (158974651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.26.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5816cfc0f21f741552310c118e41298a65b565bc6db32f9dde1106bf73666a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6376619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2a5a0c0f76203956d43b2ae9d98c8135897d5c62ef2f0afcdb2e049673031`

```dockerfile
```

-	Layers:
	-	`sha256:eca51ca055b407b5e512fedeb674d7e9782f25713b0ca11c15394e659b9268b0`  
		Last Modified: Thu, 19 Dec 2024 06:48:27 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c88e2a670c3015c330ef7980e884d2c7a10e545bffc98e619bef87d8db3bf3d`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
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
$ docker pull neo4j@sha256:a90439b6b0b1ac393983f4287c5ca3727c68936bb517bf701c058c5413d1b0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1870ed6a2684880ad99ed226a87c01b99b89a301821342c1f49cdd2eba945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332281997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3649debdcab197938b4fe5c708c919ea488d1b435f7db2350046f4152a9ce6`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354187e0d6a01833883ba8539ece581102bed9b5e2f6ace00107c9c502fa249f`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 133.9 MB (133864896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b55efc172ac6f8bd17c3560911e50854c3420214bc2a1c1e8d51deb4910685`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48780c92dcc75e3c87cd57a77ef0753e92e715ce2a7fe147035c3330782992`  
		Last Modified: Thu, 19 Dec 2024 06:28:40 GMT  
		Size: 159.0 MB (158974626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c10ffa3943eec40c973f1f619b557039de44f845748a74e567679266060d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18cb8ad7c102e2911dfa1bf7fb9981c8ff8faa1934aa558c4ffb77d7a180bf`

```dockerfile
```

-	Layers:
	-	`sha256:31b54c83fefef66d103d15813062c501925e009289093f013e4f872f23d679e8`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c672bab58d7edcd5c1b880afbebd9250a5190740ddddd6dcf3961b19caa1f2fe`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5c3aae55cfbd373038f4d196353dc819d8f929d2d1268629c33fde830354ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330402411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d6a0bf1881f306df5dba8481621afbbb2545a4388194904db2f36906b73627`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1c3a2df462ad32949d3883ba9d9d13c6b74c628eab0adea2da713a53d6200`  
		Last Modified: Thu, 19 Dec 2024 06:48:30 GMT  
		Size: 159.0 MB (158974651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5816cfc0f21f741552310c118e41298a65b565bc6db32f9dde1106bf73666a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6376619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2a5a0c0f76203956d43b2ae9d98c8135897d5c62ef2f0afcdb2e049673031`

```dockerfile
```

-	Layers:
	-	`sha256:eca51ca055b407b5e512fedeb674d7e9782f25713b0ca11c15394e659b9268b0`  
		Last Modified: Thu, 19 Dec 2024 06:48:27 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c88e2a670c3015c330ef7980e884d2c7a10e545bffc98e619bef87d8db3bf3d`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
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
$ docker pull neo4j@sha256:9f08c929f592658714859ed70b974205fa8d196dbb132f2ea5ddf801493a3a78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:42160d4e26da63343ee660812ecb919119cee7be4cc5e275e9be56d35d236012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.0 MB (620031069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dad9d96dd1e07a9579ed22a00937c6c4af9afa75d610be1432cb2f2966769d9`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58206fe82bc7bbcbfebfe8cd78f50119ccb22a9273c088ee856de5402f7914ef`  
		Last Modified: Thu, 19 Dec 2024 06:28:41 GMT  
		Size: 133.9 MB (133868780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af99cb19e7c8bda459fcc2bcc8e995234b76845d8f86fe201b3ff72860775f42`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 10.0 KB (10030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e11fc9276f3b98b27c0a427de033c8c85af9e3dea4aaa84462ed870a249479`  
		Last Modified: Thu, 19 Dec 2024 06:28:45 GMT  
		Size: 446.7 MB (446719818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ca1260361075f7df7bd373b8b30087e44046880fba2ce068b51e1091f8eca780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6706046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8313dba0f00e75976fc14cb368cf4ac582be0e153a0cc8782e7631f533c096b6`

```dockerfile
```

-	Layers:
	-	`sha256:5db7c191c5318c2c18faee07ab151fbb3ccc6c8b8c696c45717582d038b76347`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 6.7 MB (6685457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb25cf80a52736208da5ed15f4692be15b7750701985a2c20ce9ce66b2d9ad4`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 20.6 KB (20589 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:75b23b009902f6395a3aca1b5261f16f62bd7917feaac4247a1d0b928240fc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.1 MB (618147551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb91915f28bab4034a640453f36a2e0e17cc4159a2caa3e96dbbc1fb4676c3cd`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1ef7a7cf2bec238d9481b96f5f88bc3c3d1c057e99687db1e858ea06385738`  
		Last Modified: Thu, 19 Dec 2024 06:49:39 GMT  
		Size: 446.7 MB (446719791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:dd8f92a2c4c8e1c79fe37b506c134ff75e858ca8763e6039b8a9b3b5c5ef3ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6685534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27367b175f928a29a72b27f868ad8a10e2b226d207a3ecdd751e2596734996b`

```dockerfile
```

-	Layers:
	-	`sha256:8666af547a0d3ddd14639cb8a9804d673aca6f1d08ec4b1cd4bf5a9632fae04e`  
		Last Modified: Thu, 19 Dec 2024 06:49:30 GMT  
		Size: 6.7 MB (6664832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1666b2723fabfb7c6e4ef2dabc6e0892937adcc113a57b781d07073c37a65860`  
		Last Modified: Thu, 19 Dec 2024 06:49:30 GMT  
		Size: 20.7 KB (20702 bytes)  
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
$ docker pull neo4j@sha256:a90439b6b0b1ac393983f4287c5ca3727c68936bb517bf701c058c5413d1b0ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:8e1870ed6a2684880ad99ed226a87c01b99b89a301821342c1f49cdd2eba945c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332281997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3649debdcab197938b4fe5c708c919ea488d1b435f7db2350046f4152a9ce6`
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
COPY dir:0485e287b26ef73c199c820b8915015ba33a659f620dc17eafe7e7a33f8bf780 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T04:56:25" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:1e6b7297048ae70484705dda4e582fb8ad5778ea4c8ae464cf3e6a02ac439012`  
		Last Modified: Wed, 18 Dec 2024 06:15:23 GMT  
		Size: 39.4 MB (39432409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354187e0d6a01833883ba8539ece581102bed9b5e2f6ace00107c9c502fa249f`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 133.9 MB (133864896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b55efc172ac6f8bd17c3560911e50854c3420214bc2a1c1e8d51deb4910685`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 10.0 KB (10034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee48780c92dcc75e3c87cd57a77ef0753e92e715ce2a7fe147035c3330782992`  
		Last Modified: Thu, 19 Dec 2024 06:28:40 GMT  
		Size: 159.0 MB (158974626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7c10ffa3943eec40c973f1f619b557039de44f845748a74e567679266060d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18cb8ad7c102e2911dfa1bf7fb9981c8ff8faa1934aa558c4ffb77d7a180bf`

```dockerfile
```

-	Layers:
	-	`sha256:31b54c83fefef66d103d15813062c501925e009289093f013e4f872f23d679e8`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 6.4 MB (6375268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c672bab58d7edcd5c1b880afbebd9250a5190740ddddd6dcf3961b19caa1f2fe`  
		Last Modified: Thu, 19 Dec 2024 06:28:35 GMT  
		Size: 21.8 KB (21767 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:5c3aae55cfbd373038f4d196353dc819d8f929d2d1268629c33fde830354ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330402411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d6a0bf1881f306df5dba8481621afbbb2545a4388194904db2f36906b73627`
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
COPY dir:2b8ad1e81974d4feec292500267d9d72634438f9ec07a466db827a8114ef0993 in / 
# Mon, 09 Dec 2024 12:11:17 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 09 Dec 2024 12:11:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 12:11:17 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Mon, 09 Dec 2024 12:11:17 GMT
LABEL "build-date"="2024-12-18T05:01:43" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0724d65b854a0151fb7d10b0e6510d8aee28e115" "build-date"="2024-12-18T04:52:16Z" "release"="1734497536"
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
	-	`sha256:3415b32764d8c185fafcd0c946a41d5028c72a76a1c10bcd8690f139ff79eb40`  
		Last Modified: Wed, 18 Dec 2024 06:15:28 GMT  
		Size: 37.6 MB (37577418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7470bd920e3c6747f662e410803d72f780ffc40a94d1ef221684b3273c163`  
		Last Modified: Thu, 19 Dec 2024 06:48:29 GMT  
		Size: 133.8 MB (133840274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9778ad29aab81ad4844ee57c291c5fd1406a6e998f64fa13566779e1f801c`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee1c3a2df462ad32949d3883ba9d9d13c6b74c628eab0adea2da713a53d6200`  
		Last Modified: Thu, 19 Dec 2024 06:48:30 GMT  
		Size: 159.0 MB (158974651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:5816cfc0f21f741552310c118e41298a65b565bc6db32f9dde1106bf73666a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6376619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2a5a0c0f76203956d43b2ae9d98c8135897d5c62ef2f0afcdb2e049673031`

```dockerfile
```

-	Layers:
	-	`sha256:eca51ca055b407b5e512fedeb674d7e9782f25713b0ca11c15394e659b9268b0`  
		Last Modified: Thu, 19 Dec 2024 06:48:27 GMT  
		Size: 6.4 MB (6354691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c88e2a670c3015c330ef7980e884d2c7a10e545bffc98e619bef87d8db3bf3d`  
		Last Modified: Thu, 19 Dec 2024 06:48:26 GMT  
		Size: 21.9 KB (21928 bytes)  
		MIME: application/vnd.in-toto+json
