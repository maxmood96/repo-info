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
$ docker pull neo4j@sha256:23076d3d6fbbfeefb719d81e42b1abe2e4a36f5927e61e487a7b100d525a2df5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:e77771f7f88b65a9eb28cbb17b27ea39b857eb2728796addfccbbdabffd4745e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298275685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ba40a70b6f1d8cc9ec8bb8926ea6c76329a03bedcf5f5e6ea18861a037549`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5f7dbc6ba33486c14292c8a610c7e7ec98d4d89a82ed5648b26c8c603bde9f`  
		Last Modified: Tue, 14 May 2024 19:58:15 GMT  
		Size: 145.5 MB (145504828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b965231debec1bebd153542feafb8f76f9fc37374a2017859aee0f7ae82995`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36bfbefa2dc3211436f6fd298b2b11b99a156eb999877ea273f7699ce41fa4d`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f3d853dea93024e2570592c1fd3456db780ce2601008bd131c0474ac23006e`  
		Last Modified: Tue, 14 May 2024 19:58:15 GMT  
		Size: 121.3 MB (121323616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:d2359206639a051903eaa3c36f77a3420bb1af2bec2eb89693d9050d75a19ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa30f9e88b4f952505c07e04851aabecdcaa422ae404bbae03be73db16513537`

```dockerfile
```

-	Layers:
	-	`sha256:edf8f4fb12b8accda777e53aacd52a6d6c40382416bcca0a16a2f2fadb123225`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 2.9 MB (2940154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c638c78ea4f370a8b0a8c59a01ccd383fd360de6acfdccdcb03d0f22cf064cdd`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d20f6831c7b989821bb37cddd854ab2314360f8b9b6c2cb9e7af5d20fbeed28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293690934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e1de805ed8942e6e02ac3b855e1e04874be00b321b1467eb097290703dc275`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77d104492e6550053419391a4a2ef805d6d518e21cf2aa9b9b5692d15bbba6e`  
		Last Modified: Tue, 14 May 2024 17:55:36 GMT  
		Size: 142.3 MB (142304135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58880ff2225f3a624ee7240e212ca8ca12e778c2e80a5070e29ed5c6f7eac618`  
		Last Modified: Wed, 15 May 2024 10:31:41 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d3a869ac57a1a43b45622c9329080baeeb0ea0c642c6f248ddea9c20af514d`  
		Last Modified: Wed, 15 May 2024 10:31:40 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a260059e217dabd1f50775f105c5b26c0c3b3152efcea97170f79bb27ac4ac`  
		Last Modified: Wed, 15 May 2024 10:31:45 GMT  
		Size: 121.3 MB (121286552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:226eb2dfaeb818962ce80d36b6186717e3332ee200c77a5e4b567f4970bc4b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de71375a8cb897988a689cad26bf8caca6e76cd3a9bfac133ad8b2817f6991ca`

```dockerfile
```

-	Layers:
	-	`sha256:8c8633045328b04e559e02208a8a41eab39feb59390d02d769b1a37cedacc142`  
		Last Modified: Wed, 15 May 2024 10:31:41 GMT  
		Size: 2.9 MB (2940372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074bb9725a43dfc55571018038b4328f55a4a67f608206b4b53104537d495493`  
		Last Modified: Wed, 15 May 2024 10:31:40 GMT  
		Size: 18.7 KB (18667 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:23076d3d6fbbfeefb719d81e42b1abe2e4a36f5927e61e487a7b100d525a2df5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:e77771f7f88b65a9eb28cbb17b27ea39b857eb2728796addfccbbdabffd4745e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298275685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ba40a70b6f1d8cc9ec8bb8926ea6c76329a03bedcf5f5e6ea18861a037549`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5f7dbc6ba33486c14292c8a610c7e7ec98d4d89a82ed5648b26c8c603bde9f`  
		Last Modified: Tue, 14 May 2024 19:58:15 GMT  
		Size: 145.5 MB (145504828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b965231debec1bebd153542feafb8f76f9fc37374a2017859aee0f7ae82995`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36bfbefa2dc3211436f6fd298b2b11b99a156eb999877ea273f7699ce41fa4d`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f3d853dea93024e2570592c1fd3456db780ce2601008bd131c0474ac23006e`  
		Last Modified: Tue, 14 May 2024 19:58:15 GMT  
		Size: 121.3 MB (121323616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d2359206639a051903eaa3c36f77a3420bb1af2bec2eb89693d9050d75a19ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa30f9e88b4f952505c07e04851aabecdcaa422ae404bbae03be73db16513537`

```dockerfile
```

-	Layers:
	-	`sha256:edf8f4fb12b8accda777e53aacd52a6d6c40382416bcca0a16a2f2fadb123225`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 2.9 MB (2940154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c638c78ea4f370a8b0a8c59a01ccd383fd360de6acfdccdcb03d0f22cf064cdd`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d20f6831c7b989821bb37cddd854ab2314360f8b9b6c2cb9e7af5d20fbeed28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293690934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e1de805ed8942e6e02ac3b855e1e04874be00b321b1467eb097290703dc275`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77d104492e6550053419391a4a2ef805d6d518e21cf2aa9b9b5692d15bbba6e`  
		Last Modified: Tue, 14 May 2024 17:55:36 GMT  
		Size: 142.3 MB (142304135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58880ff2225f3a624ee7240e212ca8ca12e778c2e80a5070e29ed5c6f7eac618`  
		Last Modified: Wed, 15 May 2024 10:31:41 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d3a869ac57a1a43b45622c9329080baeeb0ea0c642c6f248ddea9c20af514d`  
		Last Modified: Wed, 15 May 2024 10:31:40 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a260059e217dabd1f50775f105c5b26c0c3b3152efcea97170f79bb27ac4ac`  
		Last Modified: Wed, 15 May 2024 10:31:45 GMT  
		Size: 121.3 MB (121286552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226eb2dfaeb818962ce80d36b6186717e3332ee200c77a5e4b567f4970bc4b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de71375a8cb897988a689cad26bf8caca6e76cd3a9bfac133ad8b2817f6991ca`

```dockerfile
```

-	Layers:
	-	`sha256:8c8633045328b04e559e02208a8a41eab39feb59390d02d769b1a37cedacc142`  
		Last Modified: Wed, 15 May 2024 10:31:41 GMT  
		Size: 2.9 MB (2940372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074bb9725a43dfc55571018038b4328f55a4a67f608206b4b53104537d495493`  
		Last Modified: Wed, 15 May 2024 10:31:40 GMT  
		Size: 18.7 KB (18667 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:a3df9dfedf41209e5276e58385eaf7afdcbe00845be045944fadc8b746e5868b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e9b013df9de21be463be2bc3e8752121ade3ec0ff4a0ef24a67591def0ef4474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (402986235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6cdc0cd2af77114c229b19c0d6f5ea00128a6da30c5beb3f4f7b2c51a6a07f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97444438679bb5dfdd20b3f72128d618bcd614b022eb32b4e2815cd2002e531`  
		Last Modified: Tue, 14 May 2024 19:58:32 GMT  
		Size: 145.5 MB (145504897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136602331c5a987e57b5468c5b09b0f5019f18425d1c92e50ca23cd58cadc69f`  
		Last Modified: Tue, 14 May 2024 19:58:28 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5491ca340a907b1322ee166f672faffd148b3a327df16982a4b7ffebcc145c`  
		Last Modified: Tue, 14 May 2024 19:58:28 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fa6d6e8b7528cce5b18b93423cadb1d869bb8f99b0000331fd360f96d15dd9`  
		Last Modified: Tue, 14 May 2024 19:58:34 GMT  
		Size: 226.0 MB (226034097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:a93749d16d19b1dbc715100d141584eee96c2e6d84b9599edfbcb279fd57886f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f549df1ebce3e5124cf0fc7066ab550f086192eb4b1c790e93e72b9cfeda1f3e`

```dockerfile
```

-	Layers:
	-	`sha256:b93eaf74278057dd1d6d5ee4658274d2eca29739912f9b6e5754037b9def4e29`  
		Last Modified: Tue, 14 May 2024 19:58:28 GMT  
		Size: 3.1 MB (3069464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6719fd7c9b43f16b544acaf9b5325c1436d75443643c9d1e09c62dd038aaae`  
		Last Modified: Tue, 14 May 2024 19:58:28 GMT  
		Size: 19.9 KB (19903 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8726e48162da539ad18c30bb38c8167b8592c9b7440100b2e3bac0889d7073a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398406306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cf5e4195ea533b116372fb920b9f644548af64c83e7a6559e252ffe0596dcf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77d104492e6550053419391a4a2ef805d6d518e21cf2aa9b9b5692d15bbba6e`  
		Last Modified: Tue, 14 May 2024 17:55:36 GMT  
		Size: 142.3 MB (142304135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f614706b956a3060a22bf1a5a9b6944c84d5fe5f6eafc1715d9da733f369545`  
		Last Modified: Wed, 15 May 2024 10:33:08 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be44285449b2b70132d66ffc1eb40a8b0bed6524b39c9dc89a257d548d37be`  
		Last Modified: Wed, 15 May 2024 10:33:08 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2348eb3dbab6c8ea7684fca32ab562c2df9db278567326534b4771d513d133`  
		Last Modified: Wed, 15 May 2024 10:33:13 GMT  
		Size: 226.0 MB (226001929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0003f60822538181fab1d2708e4ec68677db6a0213b3f4511560a58e7f605c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579b8170a19924b1651d809a12ab8028326019b80b84c6438e752d62429b1691`

```dockerfile
```

-	Layers:
	-	`sha256:f2d030ccd4ab43ad8d8572e3449fbb799602c03e2e7646c6709b82dd28e09047`  
		Last Modified: Wed, 15 May 2024 10:33:08 GMT  
		Size: 3.1 MB (3069678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74eb8a940f1c44fc0dbf90b706272c9b5e06e002092ee9439e238075cd2808a`  
		Last Modified: Wed, 15 May 2024 10:33:08 GMT  
		Size: 18.1 KB (18094 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.34`

```console
$ docker pull neo4j@sha256:23076d3d6fbbfeefb719d81e42b1abe2e4a36f5927e61e487a7b100d525a2df5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.34` - linux; amd64

```console
$ docker pull neo4j@sha256:e77771f7f88b65a9eb28cbb17b27ea39b857eb2728796addfccbbdabffd4745e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298275685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ba40a70b6f1d8cc9ec8bb8926ea6c76329a03bedcf5f5e6ea18861a037549`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5f7dbc6ba33486c14292c8a610c7e7ec98d4d89a82ed5648b26c8c603bde9f`  
		Last Modified: Tue, 14 May 2024 19:58:15 GMT  
		Size: 145.5 MB (145504828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b965231debec1bebd153542feafb8f76f9fc37374a2017859aee0f7ae82995`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36bfbefa2dc3211436f6fd298b2b11b99a156eb999877ea273f7699ce41fa4d`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f3d853dea93024e2570592c1fd3456db780ce2601008bd131c0474ac23006e`  
		Last Modified: Tue, 14 May 2024 19:58:15 GMT  
		Size: 121.3 MB (121323616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34` - unknown; unknown

```console
$ docker pull neo4j@sha256:d2359206639a051903eaa3c36f77a3420bb1af2bec2eb89693d9050d75a19ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa30f9e88b4f952505c07e04851aabecdcaa422ae404bbae03be73db16513537`

```dockerfile
```

-	Layers:
	-	`sha256:edf8f4fb12b8accda777e53aacd52a6d6c40382416bcca0a16a2f2fadb123225`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 2.9 MB (2940154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c638c78ea4f370a8b0a8c59a01ccd383fd360de6acfdccdcb03d0f22cf064cdd`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.34` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d20f6831c7b989821bb37cddd854ab2314360f8b9b6c2cb9e7af5d20fbeed28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293690934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e1de805ed8942e6e02ac3b855e1e04874be00b321b1467eb097290703dc275`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77d104492e6550053419391a4a2ef805d6d518e21cf2aa9b9b5692d15bbba6e`  
		Last Modified: Tue, 14 May 2024 17:55:36 GMT  
		Size: 142.3 MB (142304135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58880ff2225f3a624ee7240e212ca8ca12e778c2e80a5070e29ed5c6f7eac618`  
		Last Modified: Wed, 15 May 2024 10:31:41 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d3a869ac57a1a43b45622c9329080baeeb0ea0c642c6f248ddea9c20af514d`  
		Last Modified: Wed, 15 May 2024 10:31:40 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a260059e217dabd1f50775f105c5b26c0c3b3152efcea97170f79bb27ac4ac`  
		Last Modified: Wed, 15 May 2024 10:31:45 GMT  
		Size: 121.3 MB (121286552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34` - unknown; unknown

```console
$ docker pull neo4j@sha256:226eb2dfaeb818962ce80d36b6186717e3332ee200c77a5e4b567f4970bc4b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de71375a8cb897988a689cad26bf8caca6e76cd3a9bfac133ad8b2817f6991ca`

```dockerfile
```

-	Layers:
	-	`sha256:8c8633045328b04e559e02208a8a41eab39feb59390d02d769b1a37cedacc142`  
		Last Modified: Wed, 15 May 2024 10:31:41 GMT  
		Size: 2.9 MB (2940372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074bb9725a43dfc55571018038b4328f55a4a67f608206b4b53104537d495493`  
		Last Modified: Wed, 15 May 2024 10:31:40 GMT  
		Size: 18.7 KB (18667 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.34-community`

```console
$ docker pull neo4j@sha256:23076d3d6fbbfeefb719d81e42b1abe2e4a36f5927e61e487a7b100d525a2df5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.34-community` - linux; amd64

```console
$ docker pull neo4j@sha256:e77771f7f88b65a9eb28cbb17b27ea39b857eb2728796addfccbbdabffd4745e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.3 MB (298275685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2ba40a70b6f1d8cc9ec8bb8926ea6c76329a03bedcf5f5e6ea18861a037549`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5f7dbc6ba33486c14292c8a610c7e7ec98d4d89a82ed5648b26c8c603bde9f`  
		Last Modified: Tue, 14 May 2024 19:58:15 GMT  
		Size: 145.5 MB (145504828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b965231debec1bebd153542feafb8f76f9fc37374a2017859aee0f7ae82995`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36bfbefa2dc3211436f6fd298b2b11b99a156eb999877ea273f7699ce41fa4d`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f3d853dea93024e2570592c1fd3456db780ce2601008bd131c0474ac23006e`  
		Last Modified: Tue, 14 May 2024 19:58:15 GMT  
		Size: 121.3 MB (121323616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d2359206639a051903eaa3c36f77a3420bb1af2bec2eb89693d9050d75a19ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2960626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa30f9e88b4f952505c07e04851aabecdcaa422ae404bbae03be73db16513537`

```dockerfile
```

-	Layers:
	-	`sha256:edf8f4fb12b8accda777e53aacd52a6d6c40382416bcca0a16a2f2fadb123225`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 2.9 MB (2940154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c638c78ea4f370a8b0a8c59a01ccd383fd360de6acfdccdcb03d0f22cf064cdd`  
		Last Modified: Tue, 14 May 2024 19:58:13 GMT  
		Size: 20.5 KB (20472 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.34-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3d20f6831c7b989821bb37cddd854ab2314360f8b9b6c2cb9e7af5d20fbeed28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293690934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e1de805ed8942e6e02ac3b855e1e04874be00b321b1467eb097290703dc275`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77d104492e6550053419391a4a2ef805d6d518e21cf2aa9b9b5692d15bbba6e`  
		Last Modified: Tue, 14 May 2024 17:55:36 GMT  
		Size: 142.3 MB (142304135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58880ff2225f3a624ee7240e212ca8ca12e778c2e80a5070e29ed5c6f7eac618`  
		Last Modified: Wed, 15 May 2024 10:31:41 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d3a869ac57a1a43b45622c9329080baeeb0ea0c642c6f248ddea9c20af514d`  
		Last Modified: Wed, 15 May 2024 10:31:40 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a260059e217dabd1f50775f105c5b26c0c3b3152efcea97170f79bb27ac4ac`  
		Last Modified: Wed, 15 May 2024 10:31:45 GMT  
		Size: 121.3 MB (121286552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:226eb2dfaeb818962ce80d36b6186717e3332ee200c77a5e4b567f4970bc4b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2959039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de71375a8cb897988a689cad26bf8caca6e76cd3a9bfac133ad8b2817f6991ca`

```dockerfile
```

-	Layers:
	-	`sha256:8c8633045328b04e559e02208a8a41eab39feb59390d02d769b1a37cedacc142`  
		Last Modified: Wed, 15 May 2024 10:31:41 GMT  
		Size: 2.9 MB (2940372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:074bb9725a43dfc55571018038b4328f55a4a67f608206b4b53104537d495493`  
		Last Modified: Wed, 15 May 2024 10:31:40 GMT  
		Size: 18.7 KB (18667 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.34-enterprise`

```console
$ docker pull neo4j@sha256:a3df9dfedf41209e5276e58385eaf7afdcbe00845be045944fadc8b746e5868b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.34-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:e9b013df9de21be463be2bc3e8752121ade3ec0ff4a0ef24a67591def0ef4474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (402986235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6cdc0cd2af77114c229b19c0d6f5ea00128a6da30c5beb3f4f7b2c51a6a07f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97444438679bb5dfdd20b3f72128d618bcd614b022eb32b4e2815cd2002e531`  
		Last Modified: Tue, 14 May 2024 19:58:32 GMT  
		Size: 145.5 MB (145504897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136602331c5a987e57b5468c5b09b0f5019f18425d1c92e50ca23cd58cadc69f`  
		Last Modified: Tue, 14 May 2024 19:58:28 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5491ca340a907b1322ee166f672faffd148b3a327df16982a4b7ffebcc145c`  
		Last Modified: Tue, 14 May 2024 19:58:28 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fa6d6e8b7528cce5b18b93423cadb1d869bb8f99b0000331fd360f96d15dd9`  
		Last Modified: Tue, 14 May 2024 19:58:34 GMT  
		Size: 226.0 MB (226034097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:a93749d16d19b1dbc715100d141584eee96c2e6d84b9599edfbcb279fd57886f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3089367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f549df1ebce3e5124cf0fc7066ab550f086192eb4b1c790e93e72b9cfeda1f3e`

```dockerfile
```

-	Layers:
	-	`sha256:b93eaf74278057dd1d6d5ee4658274d2eca29739912f9b6e5754037b9def4e29`  
		Last Modified: Tue, 14 May 2024 19:58:28 GMT  
		Size: 3.1 MB (3069464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6719fd7c9b43f16b544acaf9b5325c1436d75443643c9d1e09c62dd038aaae`  
		Last Modified: Tue, 14 May 2024 19:58:28 GMT  
		Size: 19.9 KB (19903 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.34-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:8726e48162da539ad18c30bb38c8167b8592c9b7440100b2e3bac0889d7073a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398406306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cf5e4195ea533b116372fb920b9f644548af64c83e7a6559e252ffe0596dcf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77d104492e6550053419391a4a2ef805d6d518e21cf2aa9b9b5692d15bbba6e`  
		Last Modified: Tue, 14 May 2024 17:55:36 GMT  
		Size: 142.3 MB (142304135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f614706b956a3060a22bf1a5a9b6944c84d5fe5f6eafc1715d9da733f369545`  
		Last Modified: Wed, 15 May 2024 10:33:08 GMT  
		Size: 3.9 KB (3865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be44285449b2b70132d66ffc1eb40a8b0bed6524b39c9dc89a257d548d37be`  
		Last Modified: Wed, 15 May 2024 10:33:08 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2348eb3dbab6c8ea7684fca32ab562c2df9db278567326534b4771d513d133`  
		Last Modified: Wed, 15 May 2024 10:33:13 GMT  
		Size: 226.0 MB (226001929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.34-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0003f60822538181fab1d2708e4ec68677db6a0213b3f4511560a58e7f605c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579b8170a19924b1651d809a12ab8028326019b80b84c6438e752d62429b1691`

```dockerfile
```

-	Layers:
	-	`sha256:f2d030ccd4ab43ad8d8572e3449fbb799602c03e2e7646c6709b82dd28e09047`  
		Last Modified: Wed, 15 May 2024 10:33:08 GMT  
		Size: 3.1 MB (3069678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f74eb8a940f1c44fc0dbf90b706272c9b5e06e002092ee9439e238075cd2808a`  
		Last Modified: Wed, 15 May 2024 10:33:08 GMT  
		Size: 18.1 KB (18094 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:174c24a85061e67e0069b053503f910d3f0cae5cb6c6e0065f4cce0e166140a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:32cbb416370e6395daaf3b95ac131dec564cac65ebd8b27e26c654d65133d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318553085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e97f47ff28f7b87c10b925d19f4d1f9e509a3c1624fbac65cc332134f4b702`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc6187a0fd731729d24f55646f416bc3ac53dae4051e37ba1791907dc353d2`  
		Last Modified: Wed, 29 May 2024 23:02:12 GMT  
		Size: 152.7 MB (152702358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a775e1e93da20042a6e3321941989c270322a52b74ec25f978074bdc93314a`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b4516264bff29a7903cbcc7b72aa493e8d160c6b3d9af10d89a146a22a61a`  
		Last Modified: Wed, 29 May 2024 23:02:10 GMT  
		Size: 126.4 MB (126437727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:b94170a460c625301741d6d27852d18620699c7a2c443d512e6a3bf169a6b5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9267cd82f3eb15ff8c9669ef89cf15d73799cc9efff60bba860a7fc4fa42d9c`

```dockerfile
```

-	Layers:
	-	`sha256:b35af758a1fe96eecb756b8eec0d0f0367708085a3a92585e8a15763fba6f260`  
		Last Modified: Wed, 29 May 2024 23:02:07 GMT  
		Size: 10.3 MB (10309830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a9d2263602f865cbfb8b45a96b74e3be007b4352dc0cda57d2f546e6698e61`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2a36ce746f5048e927fabe90a45dd432d49d9cb6693dfeadae3bd27b28ad6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5c90bab334b69f502a5b54e965a0b55da157fc1810366abac62ae4ec87f50`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c9b59eb62b6cb3e10d4305fa98f4a86ba5be392111c9282db0ffe7308ac9`  
		Last Modified: Thu, 23 May 2024 20:24:09 GMT  
		Size: 126.4 MB (126437764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6291e1f2216d35268dc52906633b25865ffade29c5af3b423e77faddd3a1f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf2b4a260ee6000e9188e12cd7cafbcb9d64d7d91712b4aee26b8ee6f9b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:390d921c1db7a553ad402613206a652869a8e6517b8b984c7a8c5eb3238ef50a`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 10.8 MB (10836022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3fcfe97a8c4888af967e420a8a765dcd3c693c83e618376719f340c3709ecc`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:421eab133ca6a60b5a183ec2dfb87646b2d25ee2298a517f8aa817359b6becc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fbe08247a37171e18ad95cdf8a8937c3acca94c9fcd6916d9b8c5d8e2d78c069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290499980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b130ddf3e7e6965c61633e2435352d1a2c305f612813b585575eacf9f6e4cff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5cc4fd03dd9cf319fae048b3d49130421622ff27ee3ba632337bfea1731055`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 125.2 MB (125175459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d70a08f1f57303b5f1cf1e2a0e59ce34b1551bdeb5e225a2151d9d85dad7b1`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0718ff3010104007c6550a840d74362c5ccc2aa9544fea7edebc5814af39bd4`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 126.4 MB (126437882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a10e02f222fe61862238cc982f8c69c16c477cb51d04af96ed2d2701b827e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5069969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159824afc638e9979fa1981585b789e37f4828553704f42c317647abb2b41be1`

```dockerfile
```

-	Layers:
	-	`sha256:5052c04790fe485b5429e7d9f453f5affe9912b5213b318fc5e40febaf420fd6`  
		Last Modified: Wed, 29 May 2024 23:01:23 GMT  
		Size: 5.0 MB (5048372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff49b89847e506bb54bdec5ca49678572c74dd3dcb808e523b71fc452ec110ad`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 21.6 KB (21597 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b9db8386b33b03e76234054908369bf244df37985902ebe4e64c5cd9ea4f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293253160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104e4e7622d40bcc8deb3f3753c2d0c9997a1396349b3ae49088a8492bccf2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2a243ffd15909cb0b1d5aee2b729d0df3ba7017523afe1a5ffe07b9566e2c`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 126.4 MB (126437852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:43ece681b0d3f145dc0dba3b37195d5ceaa9c89ae624db68db316f7332b2b654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ab0c15bdbe4bc40ccbfcf22ef7ea242f6d9c2878415a0ffe133996a7bf65dc`

```dockerfile
```

-	Layers:
	-	`sha256:d2884a75a8e6ae30ebebd1428fd1674da40d18282eabfb4923980ee6ca3f182d`  
		Last Modified: Thu, 23 May 2024 20:22:04 GMT  
		Size: 5.3 MB (5345660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a6f2dadbe993eddb337437d8c6103ce00dde1033f695f953a5bf1edca90f30`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 21.6 KB (21614 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:96ed8f0263af6df62e4a9c97a0d7d3385a9246552d4f71216a1a5d254d834efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:66726b01c23895a1084489dfd87fa50a91bb581d8baa5e1b7c9d5ffbde7f7c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8e8b67aa823d777e80932e26871a2bf731572e900d060eafac61608751dac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7140eb8418e2f1e4ec777450d0cd2029e40037913c0c75c03264741f799505`  
		Last Modified: Thu, 23 May 2024 19:53:23 GMT  
		Size: 145.1 MB (145095105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca207659e997c876e0bd01b4773794d68c33dad138b06ff52836fe83c26072`  
		Last Modified: Thu, 23 May 2024 19:53:22 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac23d1712489bcaa8f1870cd4521811d0a137b98912a4652ad4456568bd428`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d9b87d62d53ca3fed3c460b5d697a7819bf383c27fd7fc4d76c8956b8ae13`  
		Last Modified: Thu, 23 May 2024 19:53:27 GMT  
		Size: 378.0 MB (377982829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e04faed0382154d75b05d599b50a5a8cd3f9d85b45033e6be9a9d4eff332d46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72284afa4c4d1b75f7fa67f3aa064a2dfd2823f1587cecf2bf725d97b7a53a1c`

```dockerfile
```

-	Layers:
	-	`sha256:300775d4e659043fc37df266505586253aa303f5d54783659d6ca92061cc8e75`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 3.1 MB (3133588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecc313528fb69d381d41eaee78edc007ec3bd7766cab8a61ec040656609e172`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02dbaf8393e1e2278ab62a3f055323a0f3cfc5d3120b9fa9c706f70d632f5b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605dfe6aceb871e8a7fad54dae819a1b3f753ef8a173e743e21fc767915ec300`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a1b4ddaedf474eed62e08e5cb26e9cc60202af6e41601cbec8277ceec547d`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307aa617531d51b5102a0ba95fed2d83edd9f645319e78de5c88513c327e1aa5`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab1fa2dd0b518a33513cca36ea0ff19b8a917a25a56e7133098cb8339cfeae`  
		Last Modified: Thu, 23 May 2024 20:20:52 GMT  
		Size: 377.9 MB (377944374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0d4911eb640a7643d0593bc655cf4ba4247a1f495d3d5a8ebf2e62021f023f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49875f55ee6d72344cb25583ed99d79436ea63c56c2aa2c330fa13d8baaef592`

```dockerfile
```

-	Layers:
	-	`sha256:775f7456d4802dfa3ca3dd8c95dfea9302345a66b2cb148221b9084845181371`  
		Last Modified: Thu, 23 May 2024 20:20:45 GMT  
		Size: 3.1 MB (3133814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55560658428a4b2c8ea5484cc0947e74a230d6fe078e652383a1230330e8151`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:96ed8f0263af6df62e4a9c97a0d7d3385a9246552d4f71216a1a5d254d834efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:66726b01c23895a1084489dfd87fa50a91bb581d8baa5e1b7c9d5ffbde7f7c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8e8b67aa823d777e80932e26871a2bf731572e900d060eafac61608751dac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7140eb8418e2f1e4ec777450d0cd2029e40037913c0c75c03264741f799505`  
		Last Modified: Thu, 23 May 2024 19:53:23 GMT  
		Size: 145.1 MB (145095105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca207659e997c876e0bd01b4773794d68c33dad138b06ff52836fe83c26072`  
		Last Modified: Thu, 23 May 2024 19:53:22 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac23d1712489bcaa8f1870cd4521811d0a137b98912a4652ad4456568bd428`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d9b87d62d53ca3fed3c460b5d697a7819bf383c27fd7fc4d76c8956b8ae13`  
		Last Modified: Thu, 23 May 2024 19:53:27 GMT  
		Size: 378.0 MB (377982829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e04faed0382154d75b05d599b50a5a8cd3f9d85b45033e6be9a9d4eff332d46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72284afa4c4d1b75f7fa67f3aa064a2dfd2823f1587cecf2bf725d97b7a53a1c`

```dockerfile
```

-	Layers:
	-	`sha256:300775d4e659043fc37df266505586253aa303f5d54783659d6ca92061cc8e75`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 3.1 MB (3133588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecc313528fb69d381d41eaee78edc007ec3bd7766cab8a61ec040656609e172`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02dbaf8393e1e2278ab62a3f055323a0f3cfc5d3120b9fa9c706f70d632f5b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605dfe6aceb871e8a7fad54dae819a1b3f753ef8a173e743e21fc767915ec300`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a1b4ddaedf474eed62e08e5cb26e9cc60202af6e41601cbec8277ceec547d`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307aa617531d51b5102a0ba95fed2d83edd9f645319e78de5c88513c327e1aa5`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab1fa2dd0b518a33513cca36ea0ff19b8a917a25a56e7133098cb8339cfeae`  
		Last Modified: Thu, 23 May 2024 20:20:52 GMT  
		Size: 377.9 MB (377944374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0d4911eb640a7643d0593bc655cf4ba4247a1f495d3d5a8ebf2e62021f023f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49875f55ee6d72344cb25583ed99d79436ea63c56c2aa2c330fa13d8baaef592`

```dockerfile
```

-	Layers:
	-	`sha256:775f7456d4802dfa3ca3dd8c95dfea9302345a66b2cb148221b9084845181371`  
		Last Modified: Thu, 23 May 2024 20:20:45 GMT  
		Size: 3.1 MB (3133814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55560658428a4b2c8ea5484cc0947e74a230d6fe078e652383a1230330e8151`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:32e2cc6bdc443a9bc0db086229eea05327e708ecb4d87266831069cb0cb00fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2e558a362958975656595c5e5cb1f6495f43fc0cd9d5fee190377ad99895689a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.2 MB (567159179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9814602a179f230d461f1abb0324b82f01248a57ad9d06e2711462a1452c2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfcd43411737dea6f06e538e1fcf81a7b05bf289e098cc0eb881a1a00f0f61b`  
		Last Modified: Wed, 29 May 2024 23:02:02 GMT  
		Size: 152.7 MB (152701878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fc403fbd6759c9fbbf6f2cb1649bbbe131b1bcc278a2489510690713e38472`  
		Last Modified: Wed, 29 May 2024 23:01:59 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d802a6ba47cc2a4c6727bf0e665be16f412eb5583b513feebf9a46bd2bb55c6`  
		Last Modified: Wed, 29 May 2024 23:02:05 GMT  
		Size: 375.0 MB (375044303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:3b7425a6d84a59fe500924d1f56d3aac3553290e223204f12ffa098c019dded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cd8832e0be39f36aa8660593c86d42e12a7c5fcc07a58361409c9710e2b570`

```dockerfile
```

-	Layers:
	-	`sha256:b8674afb488ddbee727bf25264230293f79ee8f8476c449a4bbf57d5f247b9d7`  
		Last Modified: Wed, 29 May 2024 23:02:00 GMT  
		Size: 10.5 MB (10481793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b594f464f47c2d3f4fe142db2e6e884fb34e9cab7b55be18c4c763b528fd074`  
		Last Modified: Wed, 29 May 2024 23:01:59 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1f9880330569341a38c64ec3541140400028768e7b0e1d6a389cddc2c240e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.7 MB (575732100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a677531841215346abdcb1ac7135052fcdd950df3e669eb567958498ef3e071f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8296248cd807a837a6dc3acb0ce0aeecba90d737c9f1cc67a91b96515e652ff`  
		Last Modified: Thu, 23 May 2024 20:26:20 GMT  
		Size: 375.0 MB (375044344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2b4a996dbec43b37df193662460d1079afc44a0b527e254e3f8f021d5641d56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11028281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46189612470021190d3bf104dd8f33f37f1935c418d35586a56103a51ae3eae`

```dockerfile
```

-	Layers:
	-	`sha256:92ec65cece960b7d57841f32ed0b7ef10f38a28aa7cba6a4854a8b334dcf3d99`  
		Last Modified: Thu, 23 May 2024 20:26:13 GMT  
		Size: 11.0 MB (11007977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342adbb441ff622538ae3927f0c48e1c840739511ef5f29a2e1b0e0bbdd07f32`  
		Last Modified: Thu, 23 May 2024 20:26:12 GMT  
		Size: 20.3 KB (20304 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:40d59c97924d201e55d78e02df7de0ffab60fc9ddb9cc67b76f4107347d3785f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c5b96fe713e4b9655e2e87bcb532cf9ed8f2844e205b4f6cf92d39592e2a7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.1 MB (539106492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbeea5a2b2292e1680ddf32602c8d092f106211520278f727feea0fc2c00a6fb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa282d1d447912112ea82af8315e469d48bf9c8fab8c92078346278d1ca610d`  
		Last Modified: Wed, 29 May 2024 23:01:40 GMT  
		Size: 125.2 MB (125175347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96db6d20d012ffc4596474d7e180f20bbdcc93e5fdcc5ab31e4143fdf4c2be32`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 9.5 KB (9545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f123ac5729d3ca167b4403cc68570dfdf36a4a8999455d488a56276cd726ae`  
		Last Modified: Wed, 29 May 2024 23:01:46 GMT  
		Size: 375.0 MB (375044503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ec9ed2a8fb4cb9a0762655d9b6b1df665b89621055123bb86da65cdf8b9982b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f394fd800b30ae01de41f9c43751677924836e4d53ac8c3803194ada788d34cd`

```dockerfile
```

-	Layers:
	-	`sha256:f7614b5e0f64af0fea72b62fb4ae2444fc559a68d3cc5e570bcd4c892e978db0`  
		Last Modified: Wed, 29 May 2024 23:01:38 GMT  
		Size: 5.2 MB (5220335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d840d67b8fdf084f1e1a970b865a0928e83b9c4d26988598b91f2b3100e195f`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 20.4 KB (20419 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d758b617678b252e51f56d02ea79f0e2d652ecc6599ff561f456cc49a962a7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.9 MB (541859874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930a633e518c25a7e070f6b634a621a22b7c02a63e25abb2476557c0037d6169`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18871374df4282d60741792b044d3274f56b0324c5f3cf1698b2c74d40f70133`  
		Last Modified: Thu, 23 May 2024 20:23:12 GMT  
		Size: 375.0 MB (375044566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7590a61dc4427200797682d8b5ae73e8eededfd36486301a6bd79463d7463549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ed3748b56b01a09823d1f8498f79031bb40c8136d9c08f633164e702dc815`

```dockerfile
```

-	Layers:
	-	`sha256:0fe01a711b7cd3c6ad7a3c46b8afcb7712244791d5ece662bac44e3c570995cb`  
		Last Modified: Thu, 23 May 2024 20:23:03 GMT  
		Size: 5.5 MB (5517615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c35eec85181e213a4cb7c2766b8250d164576294fc367824bd9ec22dbb6d19`  
		Last Modified: Thu, 23 May 2024 20:23:02 GMT  
		Size: 20.4 KB (20429 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:174c24a85061e67e0069b053503f910d3f0cae5cb6c6e0065f4cce0e166140a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:32cbb416370e6395daaf3b95ac131dec564cac65ebd8b27e26c654d65133d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318553085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e97f47ff28f7b87c10b925d19f4d1f9e509a3c1624fbac65cc332134f4b702`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc6187a0fd731729d24f55646f416bc3ac53dae4051e37ba1791907dc353d2`  
		Last Modified: Wed, 29 May 2024 23:02:12 GMT  
		Size: 152.7 MB (152702358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a775e1e93da20042a6e3321941989c270322a52b74ec25f978074bdc93314a`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b4516264bff29a7903cbcc7b72aa493e8d160c6b3d9af10d89a146a22a61a`  
		Last Modified: Wed, 29 May 2024 23:02:10 GMT  
		Size: 126.4 MB (126437727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:b94170a460c625301741d6d27852d18620699c7a2c443d512e6a3bf169a6b5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9267cd82f3eb15ff8c9669ef89cf15d73799cc9efff60bba860a7fc4fa42d9c`

```dockerfile
```

-	Layers:
	-	`sha256:b35af758a1fe96eecb756b8eec0d0f0367708085a3a92585e8a15763fba6f260`  
		Last Modified: Wed, 29 May 2024 23:02:07 GMT  
		Size: 10.3 MB (10309830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a9d2263602f865cbfb8b45a96b74e3be007b4352dc0cda57d2f546e6698e61`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2a36ce746f5048e927fabe90a45dd432d49d9cb6693dfeadae3bd27b28ad6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5c90bab334b69f502a5b54e965a0b55da157fc1810366abac62ae4ec87f50`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c9b59eb62b6cb3e10d4305fa98f4a86ba5be392111c9282db0ffe7308ac9`  
		Last Modified: Thu, 23 May 2024 20:24:09 GMT  
		Size: 126.4 MB (126437764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6291e1f2216d35268dc52906633b25865ffade29c5af3b423e77faddd3a1f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf2b4a260ee6000e9188e12cd7cafbcb9d64d7d91712b4aee26b8ee6f9b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:390d921c1db7a553ad402613206a652869a8e6517b8b984c7a8c5eb3238ef50a`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 10.8 MB (10836022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3fcfe97a8c4888af967e420a8a765dcd3c693c83e618376719f340c3709ecc`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:421eab133ca6a60b5a183ec2dfb87646b2d25ee2298a517f8aa817359b6becc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fbe08247a37171e18ad95cdf8a8937c3acca94c9fcd6916d9b8c5d8e2d78c069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290499980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b130ddf3e7e6965c61633e2435352d1a2c305f612813b585575eacf9f6e4cff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5cc4fd03dd9cf319fae048b3d49130421622ff27ee3ba632337bfea1731055`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 125.2 MB (125175459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d70a08f1f57303b5f1cf1e2a0e59ce34b1551bdeb5e225a2151d9d85dad7b1`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0718ff3010104007c6550a840d74362c5ccc2aa9544fea7edebc5814af39bd4`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 126.4 MB (126437882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a10e02f222fe61862238cc982f8c69c16c477cb51d04af96ed2d2701b827e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5069969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159824afc638e9979fa1981585b789e37f4828553704f42c317647abb2b41be1`

```dockerfile
```

-	Layers:
	-	`sha256:5052c04790fe485b5429e7d9f453f5affe9912b5213b318fc5e40febaf420fd6`  
		Last Modified: Wed, 29 May 2024 23:01:23 GMT  
		Size: 5.0 MB (5048372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff49b89847e506bb54bdec5ca49678572c74dd3dcb808e523b71fc452ec110ad`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 21.6 KB (21597 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b9db8386b33b03e76234054908369bf244df37985902ebe4e64c5cd9ea4f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293253160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104e4e7622d40bcc8deb3f3753c2d0c9997a1396349b3ae49088a8492bccf2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2a243ffd15909cb0b1d5aee2b729d0df3ba7017523afe1a5ffe07b9566e2c`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 126.4 MB (126437852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:43ece681b0d3f145dc0dba3b37195d5ceaa9c89ae624db68db316f7332b2b654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ab0c15bdbe4bc40ccbfcf22ef7ea242f6d9c2878415a0ffe133996a7bf65dc`

```dockerfile
```

-	Layers:
	-	`sha256:d2884a75a8e6ae30ebebd1428fd1674da40d18282eabfb4923980ee6ca3f182d`  
		Last Modified: Thu, 23 May 2024 20:22:04 GMT  
		Size: 5.3 MB (5345660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a6f2dadbe993eddb337437d8c6103ce00dde1033f695f953a5bf1edca90f30`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 21.6 KB (21614 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-bullseye`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-community`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-community` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-community-bullseye`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-community-ubi8`

```console
$ docker pull neo4j@sha256:174c24a85061e67e0069b053503f910d3f0cae5cb6c6e0065f4cce0e166140a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:32cbb416370e6395daaf3b95ac131dec564cac65ebd8b27e26c654d65133d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318553085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e97f47ff28f7b87c10b925d19f4d1f9e509a3c1624fbac65cc332134f4b702`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc6187a0fd731729d24f55646f416bc3ac53dae4051e37ba1791907dc353d2`  
		Last Modified: Wed, 29 May 2024 23:02:12 GMT  
		Size: 152.7 MB (152702358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a775e1e93da20042a6e3321941989c270322a52b74ec25f978074bdc93314a`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b4516264bff29a7903cbcc7b72aa493e8d160c6b3d9af10d89a146a22a61a`  
		Last Modified: Wed, 29 May 2024 23:02:10 GMT  
		Size: 126.4 MB (126437727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:b94170a460c625301741d6d27852d18620699c7a2c443d512e6a3bf169a6b5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9267cd82f3eb15ff8c9669ef89cf15d73799cc9efff60bba860a7fc4fa42d9c`

```dockerfile
```

-	Layers:
	-	`sha256:b35af758a1fe96eecb756b8eec0d0f0367708085a3a92585e8a15763fba6f260`  
		Last Modified: Wed, 29 May 2024 23:02:07 GMT  
		Size: 10.3 MB (10309830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a9d2263602f865cbfb8b45a96b74e3be007b4352dc0cda57d2f546e6698e61`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2a36ce746f5048e927fabe90a45dd432d49d9cb6693dfeadae3bd27b28ad6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5c90bab334b69f502a5b54e965a0b55da157fc1810366abac62ae4ec87f50`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c9b59eb62b6cb3e10d4305fa98f4a86ba5be392111c9282db0ffe7308ac9`  
		Last Modified: Thu, 23 May 2024 20:24:09 GMT  
		Size: 126.4 MB (126437764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6291e1f2216d35268dc52906633b25865ffade29c5af3b423e77faddd3a1f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf2b4a260ee6000e9188e12cd7cafbcb9d64d7d91712b4aee26b8ee6f9b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:390d921c1db7a553ad402613206a652869a8e6517b8b984c7a8c5eb3238ef50a`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 10.8 MB (10836022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3fcfe97a8c4888af967e420a8a765dcd3c693c83e618376719f340c3709ecc`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-community-ubi9`

```console
$ docker pull neo4j@sha256:421eab133ca6a60b5a183ec2dfb87646b2d25ee2298a517f8aa817359b6becc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fbe08247a37171e18ad95cdf8a8937c3acca94c9fcd6916d9b8c5d8e2d78c069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290499980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b130ddf3e7e6965c61633e2435352d1a2c305f612813b585575eacf9f6e4cff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5cc4fd03dd9cf319fae048b3d49130421622ff27ee3ba632337bfea1731055`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 125.2 MB (125175459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d70a08f1f57303b5f1cf1e2a0e59ce34b1551bdeb5e225a2151d9d85dad7b1`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0718ff3010104007c6550a840d74362c5ccc2aa9544fea7edebc5814af39bd4`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 126.4 MB (126437882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a10e02f222fe61862238cc982f8c69c16c477cb51d04af96ed2d2701b827e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5069969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159824afc638e9979fa1981585b789e37f4828553704f42c317647abb2b41be1`

```dockerfile
```

-	Layers:
	-	`sha256:5052c04790fe485b5429e7d9f453f5affe9912b5213b318fc5e40febaf420fd6`  
		Last Modified: Wed, 29 May 2024 23:01:23 GMT  
		Size: 5.0 MB (5048372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff49b89847e506bb54bdec5ca49678572c74dd3dcb808e523b71fc452ec110ad`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 21.6 KB (21597 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b9db8386b33b03e76234054908369bf244df37985902ebe4e64c5cd9ea4f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293253160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104e4e7622d40bcc8deb3f3753c2d0c9997a1396349b3ae49088a8492bccf2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2a243ffd15909cb0b1d5aee2b729d0df3ba7017523afe1a5ffe07b9566e2c`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 126.4 MB (126437852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:43ece681b0d3f145dc0dba3b37195d5ceaa9c89ae624db68db316f7332b2b654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ab0c15bdbe4bc40ccbfcf22ef7ea242f6d9c2878415a0ffe133996a7bf65dc`

```dockerfile
```

-	Layers:
	-	`sha256:d2884a75a8e6ae30ebebd1428fd1674da40d18282eabfb4923980ee6ca3f182d`  
		Last Modified: Thu, 23 May 2024 20:22:04 GMT  
		Size: 5.3 MB (5345660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a6f2dadbe993eddb337437d8c6103ce00dde1033f695f953a5bf1edca90f30`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 21.6 KB (21614 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-enterprise`

```console
$ docker pull neo4j@sha256:96ed8f0263af6df62e4a9c97a0d7d3385a9246552d4f71216a1a5d254d834efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:66726b01c23895a1084489dfd87fa50a91bb581d8baa5e1b7c9d5ffbde7f7c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8e8b67aa823d777e80932e26871a2bf731572e900d060eafac61608751dac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7140eb8418e2f1e4ec777450d0cd2029e40037913c0c75c03264741f799505`  
		Last Modified: Thu, 23 May 2024 19:53:23 GMT  
		Size: 145.1 MB (145095105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca207659e997c876e0bd01b4773794d68c33dad138b06ff52836fe83c26072`  
		Last Modified: Thu, 23 May 2024 19:53:22 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac23d1712489bcaa8f1870cd4521811d0a137b98912a4652ad4456568bd428`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d9b87d62d53ca3fed3c460b5d697a7819bf383c27fd7fc4d76c8956b8ae13`  
		Last Modified: Thu, 23 May 2024 19:53:27 GMT  
		Size: 378.0 MB (377982829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e04faed0382154d75b05d599b50a5a8cd3f9d85b45033e6be9a9d4eff332d46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72284afa4c4d1b75f7fa67f3aa064a2dfd2823f1587cecf2bf725d97b7a53a1c`

```dockerfile
```

-	Layers:
	-	`sha256:300775d4e659043fc37df266505586253aa303f5d54783659d6ca92061cc8e75`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 3.1 MB (3133588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecc313528fb69d381d41eaee78edc007ec3bd7766cab8a61ec040656609e172`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02dbaf8393e1e2278ab62a3f055323a0f3cfc5d3120b9fa9c706f70d632f5b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605dfe6aceb871e8a7fad54dae819a1b3f753ef8a173e743e21fc767915ec300`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a1b4ddaedf474eed62e08e5cb26e9cc60202af6e41601cbec8277ceec547d`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307aa617531d51b5102a0ba95fed2d83edd9f645319e78de5c88513c327e1aa5`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab1fa2dd0b518a33513cca36ea0ff19b8a917a25a56e7133098cb8339cfeae`  
		Last Modified: Thu, 23 May 2024 20:20:52 GMT  
		Size: 377.9 MB (377944374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0d4911eb640a7643d0593bc655cf4ba4247a1f495d3d5a8ebf2e62021f023f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49875f55ee6d72344cb25583ed99d79436ea63c56c2aa2c330fa13d8baaef592`

```dockerfile
```

-	Layers:
	-	`sha256:775f7456d4802dfa3ca3dd8c95dfea9302345a66b2cb148221b9084845181371`  
		Last Modified: Thu, 23 May 2024 20:20:45 GMT  
		Size: 3.1 MB (3133814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55560658428a4b2c8ea5484cc0947e74a230d6fe078e652383a1230330e8151`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:96ed8f0263af6df62e4a9c97a0d7d3385a9246552d4f71216a1a5d254d834efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:66726b01c23895a1084489dfd87fa50a91bb581d8baa5e1b7c9d5ffbde7f7c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8e8b67aa823d777e80932e26871a2bf731572e900d060eafac61608751dac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7140eb8418e2f1e4ec777450d0cd2029e40037913c0c75c03264741f799505`  
		Last Modified: Thu, 23 May 2024 19:53:23 GMT  
		Size: 145.1 MB (145095105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca207659e997c876e0bd01b4773794d68c33dad138b06ff52836fe83c26072`  
		Last Modified: Thu, 23 May 2024 19:53:22 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac23d1712489bcaa8f1870cd4521811d0a137b98912a4652ad4456568bd428`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d9b87d62d53ca3fed3c460b5d697a7819bf383c27fd7fc4d76c8956b8ae13`  
		Last Modified: Thu, 23 May 2024 19:53:27 GMT  
		Size: 378.0 MB (377982829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e04faed0382154d75b05d599b50a5a8cd3f9d85b45033e6be9a9d4eff332d46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72284afa4c4d1b75f7fa67f3aa064a2dfd2823f1587cecf2bf725d97b7a53a1c`

```dockerfile
```

-	Layers:
	-	`sha256:300775d4e659043fc37df266505586253aa303f5d54783659d6ca92061cc8e75`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 3.1 MB (3133588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecc313528fb69d381d41eaee78edc007ec3bd7766cab8a61ec040656609e172`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02dbaf8393e1e2278ab62a3f055323a0f3cfc5d3120b9fa9c706f70d632f5b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605dfe6aceb871e8a7fad54dae819a1b3f753ef8a173e743e21fc767915ec300`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a1b4ddaedf474eed62e08e5cb26e9cc60202af6e41601cbec8277ceec547d`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307aa617531d51b5102a0ba95fed2d83edd9f645319e78de5c88513c327e1aa5`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab1fa2dd0b518a33513cca36ea0ff19b8a917a25a56e7133098cb8339cfeae`  
		Last Modified: Thu, 23 May 2024 20:20:52 GMT  
		Size: 377.9 MB (377944374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0d4911eb640a7643d0593bc655cf4ba4247a1f495d3d5a8ebf2e62021f023f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49875f55ee6d72344cb25583ed99d79436ea63c56c2aa2c330fa13d8baaef592`

```dockerfile
```

-	Layers:
	-	`sha256:775f7456d4802dfa3ca3dd8c95dfea9302345a66b2cb148221b9084845181371`  
		Last Modified: Thu, 23 May 2024 20:20:45 GMT  
		Size: 3.1 MB (3133814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55560658428a4b2c8ea5484cc0947e74a230d6fe078e652383a1230330e8151`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:32e2cc6bdc443a9bc0db086229eea05327e708ecb4d87266831069cb0cb00fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2e558a362958975656595c5e5cb1f6495f43fc0cd9d5fee190377ad99895689a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.2 MB (567159179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9814602a179f230d461f1abb0324b82f01248a57ad9d06e2711462a1452c2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfcd43411737dea6f06e538e1fcf81a7b05bf289e098cc0eb881a1a00f0f61b`  
		Last Modified: Wed, 29 May 2024 23:02:02 GMT  
		Size: 152.7 MB (152701878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fc403fbd6759c9fbbf6f2cb1649bbbe131b1bcc278a2489510690713e38472`  
		Last Modified: Wed, 29 May 2024 23:01:59 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d802a6ba47cc2a4c6727bf0e665be16f412eb5583b513feebf9a46bd2bb55c6`  
		Last Modified: Wed, 29 May 2024 23:02:05 GMT  
		Size: 375.0 MB (375044303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:3b7425a6d84a59fe500924d1f56d3aac3553290e223204f12ffa098c019dded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cd8832e0be39f36aa8660593c86d42e12a7c5fcc07a58361409c9710e2b570`

```dockerfile
```

-	Layers:
	-	`sha256:b8674afb488ddbee727bf25264230293f79ee8f8476c449a4bbf57d5f247b9d7`  
		Last Modified: Wed, 29 May 2024 23:02:00 GMT  
		Size: 10.5 MB (10481793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b594f464f47c2d3f4fe142db2e6e884fb34e9cab7b55be18c4c763b528fd074`  
		Last Modified: Wed, 29 May 2024 23:01:59 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1f9880330569341a38c64ec3541140400028768e7b0e1d6a389cddc2c240e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.7 MB (575732100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a677531841215346abdcb1ac7135052fcdd950df3e669eb567958498ef3e071f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8296248cd807a837a6dc3acb0ce0aeecba90d737c9f1cc67a91b96515e652ff`  
		Last Modified: Thu, 23 May 2024 20:26:20 GMT  
		Size: 375.0 MB (375044344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2b4a996dbec43b37df193662460d1079afc44a0b527e254e3f8f021d5641d56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11028281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46189612470021190d3bf104dd8f33f37f1935c418d35586a56103a51ae3eae`

```dockerfile
```

-	Layers:
	-	`sha256:92ec65cece960b7d57841f32ed0b7ef10f38a28aa7cba6a4854a8b334dcf3d99`  
		Last Modified: Thu, 23 May 2024 20:26:13 GMT  
		Size: 11.0 MB (11007977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342adbb441ff622538ae3927f0c48e1c840739511ef5f29a2e1b0e0bbdd07f32`  
		Last Modified: Thu, 23 May 2024 20:26:12 GMT  
		Size: 20.3 KB (20304 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:40d59c97924d201e55d78e02df7de0ffab60fc9ddb9cc67b76f4107347d3785f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c5b96fe713e4b9655e2e87bcb532cf9ed8f2844e205b4f6cf92d39592e2a7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.1 MB (539106492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbeea5a2b2292e1680ddf32602c8d092f106211520278f727feea0fc2c00a6fb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa282d1d447912112ea82af8315e469d48bf9c8fab8c92078346278d1ca610d`  
		Last Modified: Wed, 29 May 2024 23:01:40 GMT  
		Size: 125.2 MB (125175347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96db6d20d012ffc4596474d7e180f20bbdcc93e5fdcc5ab31e4143fdf4c2be32`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 9.5 KB (9545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f123ac5729d3ca167b4403cc68570dfdf36a4a8999455d488a56276cd726ae`  
		Last Modified: Wed, 29 May 2024 23:01:46 GMT  
		Size: 375.0 MB (375044503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ec9ed2a8fb4cb9a0762655d9b6b1df665b89621055123bb86da65cdf8b9982b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f394fd800b30ae01de41f9c43751677924836e4d53ac8c3803194ada788d34cd`

```dockerfile
```

-	Layers:
	-	`sha256:f7614b5e0f64af0fea72b62fb4ae2444fc559a68d3cc5e570bcd4c892e978db0`  
		Last Modified: Wed, 29 May 2024 23:01:38 GMT  
		Size: 5.2 MB (5220335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d840d67b8fdf084f1e1a970b865a0928e83b9c4d26988598b91f2b3100e195f`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 20.4 KB (20419 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d758b617678b252e51f56d02ea79f0e2d652ecc6599ff561f456cc49a962a7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.9 MB (541859874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930a633e518c25a7e070f6b634a621a22b7c02a63e25abb2476557c0037d6169`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18871374df4282d60741792b044d3274f56b0324c5f3cf1698b2c74d40f70133`  
		Last Modified: Thu, 23 May 2024 20:23:12 GMT  
		Size: 375.0 MB (375044566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7590a61dc4427200797682d8b5ae73e8eededfd36486301a6bd79463d7463549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ed3748b56b01a09823d1f8498f79031bb40c8136d9c08f633164e702dc815`

```dockerfile
```

-	Layers:
	-	`sha256:0fe01a711b7cd3c6ad7a3c46b8afcb7712244791d5ece662bac44e3c570995cb`  
		Last Modified: Thu, 23 May 2024 20:23:03 GMT  
		Size: 5.5 MB (5517615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c35eec85181e213a4cb7c2766b8250d164576294fc367824bd9ec22dbb6d19`  
		Last Modified: Thu, 23 May 2024 20:23:02 GMT  
		Size: 20.4 KB (20429 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-ubi8`

```console
$ docker pull neo4j@sha256:174c24a85061e67e0069b053503f910d3f0cae5cb6c6e0065f4cce0e166140a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:32cbb416370e6395daaf3b95ac131dec564cac65ebd8b27e26c654d65133d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318553085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e97f47ff28f7b87c10b925d19f4d1f9e509a3c1624fbac65cc332134f4b702`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc6187a0fd731729d24f55646f416bc3ac53dae4051e37ba1791907dc353d2`  
		Last Modified: Wed, 29 May 2024 23:02:12 GMT  
		Size: 152.7 MB (152702358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a775e1e93da20042a6e3321941989c270322a52b74ec25f978074bdc93314a`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b4516264bff29a7903cbcc7b72aa493e8d160c6b3d9af10d89a146a22a61a`  
		Last Modified: Wed, 29 May 2024 23:02:10 GMT  
		Size: 126.4 MB (126437727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:b94170a460c625301741d6d27852d18620699c7a2c443d512e6a3bf169a6b5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9267cd82f3eb15ff8c9669ef89cf15d73799cc9efff60bba860a7fc4fa42d9c`

```dockerfile
```

-	Layers:
	-	`sha256:b35af758a1fe96eecb756b8eec0d0f0367708085a3a92585e8a15763fba6f260`  
		Last Modified: Wed, 29 May 2024 23:02:07 GMT  
		Size: 10.3 MB (10309830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a9d2263602f865cbfb8b45a96b74e3be007b4352dc0cda57d2f546e6698e61`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2a36ce746f5048e927fabe90a45dd432d49d9cb6693dfeadae3bd27b28ad6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5c90bab334b69f502a5b54e965a0b55da157fc1810366abac62ae4ec87f50`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c9b59eb62b6cb3e10d4305fa98f4a86ba5be392111c9282db0ffe7308ac9`  
		Last Modified: Thu, 23 May 2024 20:24:09 GMT  
		Size: 126.4 MB (126437764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6291e1f2216d35268dc52906633b25865ffade29c5af3b423e77faddd3a1f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf2b4a260ee6000e9188e12cd7cafbcb9d64d7d91712b4aee26b8ee6f9b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:390d921c1db7a553ad402613206a652869a8e6517b8b984c7a8c5eb3238ef50a`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 10.8 MB (10836022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3fcfe97a8c4888af967e420a8a765dcd3c693c83e618376719f340c3709ecc`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20-ubi9`

```console
$ docker pull neo4j@sha256:421eab133ca6a60b5a183ec2dfb87646b2d25ee2298a517f8aa817359b6becc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fbe08247a37171e18ad95cdf8a8937c3acca94c9fcd6916d9b8c5d8e2d78c069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290499980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b130ddf3e7e6965c61633e2435352d1a2c305f612813b585575eacf9f6e4cff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5cc4fd03dd9cf319fae048b3d49130421622ff27ee3ba632337bfea1731055`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 125.2 MB (125175459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d70a08f1f57303b5f1cf1e2a0e59ce34b1551bdeb5e225a2151d9d85dad7b1`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0718ff3010104007c6550a840d74362c5ccc2aa9544fea7edebc5814af39bd4`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 126.4 MB (126437882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a10e02f222fe61862238cc982f8c69c16c477cb51d04af96ed2d2701b827e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5069969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159824afc638e9979fa1981585b789e37f4828553704f42c317647abb2b41be1`

```dockerfile
```

-	Layers:
	-	`sha256:5052c04790fe485b5429e7d9f453f5affe9912b5213b318fc5e40febaf420fd6`  
		Last Modified: Wed, 29 May 2024 23:01:23 GMT  
		Size: 5.0 MB (5048372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff49b89847e506bb54bdec5ca49678572c74dd3dcb808e523b71fc452ec110ad`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 21.6 KB (21597 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b9db8386b33b03e76234054908369bf244df37985902ebe4e64c5cd9ea4f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293253160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104e4e7622d40bcc8deb3f3753c2d0c9997a1396349b3ae49088a8492bccf2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2a243ffd15909cb0b1d5aee2b729d0df3ba7017523afe1a5ffe07b9566e2c`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 126.4 MB (126437852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:43ece681b0d3f145dc0dba3b37195d5ceaa9c89ae624db68db316f7332b2b654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ab0c15bdbe4bc40ccbfcf22ef7ea242f6d9c2878415a0ffe133996a7bf65dc`

```dockerfile
```

-	Layers:
	-	`sha256:d2884a75a8e6ae30ebebd1428fd1674da40d18282eabfb4923980ee6ca3f182d`  
		Last Modified: Thu, 23 May 2024 20:22:04 GMT  
		Size: 5.3 MB (5345660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a6f2dadbe993eddb337437d8c6103ce00dde1033f695f953a5bf1edca90f30`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 21.6 KB (21614 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-bullseye`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-community`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-community-bullseye`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-community-ubi8`

```console
$ docker pull neo4j@sha256:174c24a85061e67e0069b053503f910d3f0cae5cb6c6e0065f4cce0e166140a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:32cbb416370e6395daaf3b95ac131dec564cac65ebd8b27e26c654d65133d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318553085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e97f47ff28f7b87c10b925d19f4d1f9e509a3c1624fbac65cc332134f4b702`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc6187a0fd731729d24f55646f416bc3ac53dae4051e37ba1791907dc353d2`  
		Last Modified: Wed, 29 May 2024 23:02:12 GMT  
		Size: 152.7 MB (152702358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a775e1e93da20042a6e3321941989c270322a52b74ec25f978074bdc93314a`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b4516264bff29a7903cbcc7b72aa493e8d160c6b3d9af10d89a146a22a61a`  
		Last Modified: Wed, 29 May 2024 23:02:10 GMT  
		Size: 126.4 MB (126437727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:b94170a460c625301741d6d27852d18620699c7a2c443d512e6a3bf169a6b5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9267cd82f3eb15ff8c9669ef89cf15d73799cc9efff60bba860a7fc4fa42d9c`

```dockerfile
```

-	Layers:
	-	`sha256:b35af758a1fe96eecb756b8eec0d0f0367708085a3a92585e8a15763fba6f260`  
		Last Modified: Wed, 29 May 2024 23:02:07 GMT  
		Size: 10.3 MB (10309830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a9d2263602f865cbfb8b45a96b74e3be007b4352dc0cda57d2f546e6698e61`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2a36ce746f5048e927fabe90a45dd432d49d9cb6693dfeadae3bd27b28ad6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5c90bab334b69f502a5b54e965a0b55da157fc1810366abac62ae4ec87f50`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c9b59eb62b6cb3e10d4305fa98f4a86ba5be392111c9282db0ffe7308ac9`  
		Last Modified: Thu, 23 May 2024 20:24:09 GMT  
		Size: 126.4 MB (126437764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6291e1f2216d35268dc52906633b25865ffade29c5af3b423e77faddd3a1f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf2b4a260ee6000e9188e12cd7cafbcb9d64d7d91712b4aee26b8ee6f9b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:390d921c1db7a553ad402613206a652869a8e6517b8b984c7a8c5eb3238ef50a`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 10.8 MB (10836022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3fcfe97a8c4888af967e420a8a765dcd3c693c83e618376719f340c3709ecc`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-community-ubi9`

```console
$ docker pull neo4j@sha256:421eab133ca6a60b5a183ec2dfb87646b2d25ee2298a517f8aa817359b6becc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fbe08247a37171e18ad95cdf8a8937c3acca94c9fcd6916d9b8c5d8e2d78c069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290499980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b130ddf3e7e6965c61633e2435352d1a2c305f612813b585575eacf9f6e4cff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5cc4fd03dd9cf319fae048b3d49130421622ff27ee3ba632337bfea1731055`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 125.2 MB (125175459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d70a08f1f57303b5f1cf1e2a0e59ce34b1551bdeb5e225a2151d9d85dad7b1`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0718ff3010104007c6550a840d74362c5ccc2aa9544fea7edebc5814af39bd4`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 126.4 MB (126437882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a10e02f222fe61862238cc982f8c69c16c477cb51d04af96ed2d2701b827e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5069969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159824afc638e9979fa1981585b789e37f4828553704f42c317647abb2b41be1`

```dockerfile
```

-	Layers:
	-	`sha256:5052c04790fe485b5429e7d9f453f5affe9912b5213b318fc5e40febaf420fd6`  
		Last Modified: Wed, 29 May 2024 23:01:23 GMT  
		Size: 5.0 MB (5048372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff49b89847e506bb54bdec5ca49678572c74dd3dcb808e523b71fc452ec110ad`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 21.6 KB (21597 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b9db8386b33b03e76234054908369bf244df37985902ebe4e64c5cd9ea4f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293253160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104e4e7622d40bcc8deb3f3753c2d0c9997a1396349b3ae49088a8492bccf2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2a243ffd15909cb0b1d5aee2b729d0df3ba7017523afe1a5ffe07b9566e2c`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 126.4 MB (126437852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:43ece681b0d3f145dc0dba3b37195d5ceaa9c89ae624db68db316f7332b2b654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ab0c15bdbe4bc40ccbfcf22ef7ea242f6d9c2878415a0ffe133996a7bf65dc`

```dockerfile
```

-	Layers:
	-	`sha256:d2884a75a8e6ae30ebebd1428fd1674da40d18282eabfb4923980ee6ca3f182d`  
		Last Modified: Thu, 23 May 2024 20:22:04 GMT  
		Size: 5.3 MB (5345660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a6f2dadbe993eddb337437d8c6103ce00dde1033f695f953a5bf1edca90f30`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 21.6 KB (21614 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-enterprise`

```console
$ docker pull neo4j@sha256:96ed8f0263af6df62e4a9c97a0d7d3385a9246552d4f71216a1a5d254d834efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:66726b01c23895a1084489dfd87fa50a91bb581d8baa5e1b7c9d5ffbde7f7c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8e8b67aa823d777e80932e26871a2bf731572e900d060eafac61608751dac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7140eb8418e2f1e4ec777450d0cd2029e40037913c0c75c03264741f799505`  
		Last Modified: Thu, 23 May 2024 19:53:23 GMT  
		Size: 145.1 MB (145095105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca207659e997c876e0bd01b4773794d68c33dad138b06ff52836fe83c26072`  
		Last Modified: Thu, 23 May 2024 19:53:22 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac23d1712489bcaa8f1870cd4521811d0a137b98912a4652ad4456568bd428`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d9b87d62d53ca3fed3c460b5d697a7819bf383c27fd7fc4d76c8956b8ae13`  
		Last Modified: Thu, 23 May 2024 19:53:27 GMT  
		Size: 378.0 MB (377982829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e04faed0382154d75b05d599b50a5a8cd3f9d85b45033e6be9a9d4eff332d46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72284afa4c4d1b75f7fa67f3aa064a2dfd2823f1587cecf2bf725d97b7a53a1c`

```dockerfile
```

-	Layers:
	-	`sha256:300775d4e659043fc37df266505586253aa303f5d54783659d6ca92061cc8e75`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 3.1 MB (3133588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecc313528fb69d381d41eaee78edc007ec3bd7766cab8a61ec040656609e172`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02dbaf8393e1e2278ab62a3f055323a0f3cfc5d3120b9fa9c706f70d632f5b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605dfe6aceb871e8a7fad54dae819a1b3f753ef8a173e743e21fc767915ec300`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a1b4ddaedf474eed62e08e5cb26e9cc60202af6e41601cbec8277ceec547d`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307aa617531d51b5102a0ba95fed2d83edd9f645319e78de5c88513c327e1aa5`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab1fa2dd0b518a33513cca36ea0ff19b8a917a25a56e7133098cb8339cfeae`  
		Last Modified: Thu, 23 May 2024 20:20:52 GMT  
		Size: 377.9 MB (377944374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0d4911eb640a7643d0593bc655cf4ba4247a1f495d3d5a8ebf2e62021f023f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49875f55ee6d72344cb25583ed99d79436ea63c56c2aa2c330fa13d8baaef592`

```dockerfile
```

-	Layers:
	-	`sha256:775f7456d4802dfa3ca3dd8c95dfea9302345a66b2cb148221b9084845181371`  
		Last Modified: Thu, 23 May 2024 20:20:45 GMT  
		Size: 3.1 MB (3133814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55560658428a4b2c8ea5484cc0947e74a230d6fe078e652383a1230330e8151`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:96ed8f0263af6df62e4a9c97a0d7d3385a9246552d4f71216a1a5d254d834efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:66726b01c23895a1084489dfd87fa50a91bb581d8baa5e1b7c9d5ffbde7f7c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8e8b67aa823d777e80932e26871a2bf731572e900d060eafac61608751dac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7140eb8418e2f1e4ec777450d0cd2029e40037913c0c75c03264741f799505`  
		Last Modified: Thu, 23 May 2024 19:53:23 GMT  
		Size: 145.1 MB (145095105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca207659e997c876e0bd01b4773794d68c33dad138b06ff52836fe83c26072`  
		Last Modified: Thu, 23 May 2024 19:53:22 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac23d1712489bcaa8f1870cd4521811d0a137b98912a4652ad4456568bd428`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d9b87d62d53ca3fed3c460b5d697a7819bf383c27fd7fc4d76c8956b8ae13`  
		Last Modified: Thu, 23 May 2024 19:53:27 GMT  
		Size: 378.0 MB (377982829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e04faed0382154d75b05d599b50a5a8cd3f9d85b45033e6be9a9d4eff332d46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72284afa4c4d1b75f7fa67f3aa064a2dfd2823f1587cecf2bf725d97b7a53a1c`

```dockerfile
```

-	Layers:
	-	`sha256:300775d4e659043fc37df266505586253aa303f5d54783659d6ca92061cc8e75`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 3.1 MB (3133588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecc313528fb69d381d41eaee78edc007ec3bd7766cab8a61ec040656609e172`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02dbaf8393e1e2278ab62a3f055323a0f3cfc5d3120b9fa9c706f70d632f5b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605dfe6aceb871e8a7fad54dae819a1b3f753ef8a173e743e21fc767915ec300`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a1b4ddaedf474eed62e08e5cb26e9cc60202af6e41601cbec8277ceec547d`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307aa617531d51b5102a0ba95fed2d83edd9f645319e78de5c88513c327e1aa5`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab1fa2dd0b518a33513cca36ea0ff19b8a917a25a56e7133098cb8339cfeae`  
		Last Modified: Thu, 23 May 2024 20:20:52 GMT  
		Size: 377.9 MB (377944374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0d4911eb640a7643d0593bc655cf4ba4247a1f495d3d5a8ebf2e62021f023f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49875f55ee6d72344cb25583ed99d79436ea63c56c2aa2c330fa13d8baaef592`

```dockerfile
```

-	Layers:
	-	`sha256:775f7456d4802dfa3ca3dd8c95dfea9302345a66b2cb148221b9084845181371`  
		Last Modified: Thu, 23 May 2024 20:20:45 GMT  
		Size: 3.1 MB (3133814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55560658428a4b2c8ea5484cc0947e74a230d6fe078e652383a1230330e8151`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:32e2cc6bdc443a9bc0db086229eea05327e708ecb4d87266831069cb0cb00fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2e558a362958975656595c5e5cb1f6495f43fc0cd9d5fee190377ad99895689a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.2 MB (567159179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9814602a179f230d461f1abb0324b82f01248a57ad9d06e2711462a1452c2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfcd43411737dea6f06e538e1fcf81a7b05bf289e098cc0eb881a1a00f0f61b`  
		Last Modified: Wed, 29 May 2024 23:02:02 GMT  
		Size: 152.7 MB (152701878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fc403fbd6759c9fbbf6f2cb1649bbbe131b1bcc278a2489510690713e38472`  
		Last Modified: Wed, 29 May 2024 23:01:59 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d802a6ba47cc2a4c6727bf0e665be16f412eb5583b513feebf9a46bd2bb55c6`  
		Last Modified: Wed, 29 May 2024 23:02:05 GMT  
		Size: 375.0 MB (375044303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:3b7425a6d84a59fe500924d1f56d3aac3553290e223204f12ffa098c019dded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cd8832e0be39f36aa8660593c86d42e12a7c5fcc07a58361409c9710e2b570`

```dockerfile
```

-	Layers:
	-	`sha256:b8674afb488ddbee727bf25264230293f79ee8f8476c449a4bbf57d5f247b9d7`  
		Last Modified: Wed, 29 May 2024 23:02:00 GMT  
		Size: 10.5 MB (10481793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b594f464f47c2d3f4fe142db2e6e884fb34e9cab7b55be18c4c763b528fd074`  
		Last Modified: Wed, 29 May 2024 23:01:59 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1f9880330569341a38c64ec3541140400028768e7b0e1d6a389cddc2c240e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.7 MB (575732100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a677531841215346abdcb1ac7135052fcdd950df3e669eb567958498ef3e071f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8296248cd807a837a6dc3acb0ce0aeecba90d737c9f1cc67a91b96515e652ff`  
		Last Modified: Thu, 23 May 2024 20:26:20 GMT  
		Size: 375.0 MB (375044344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2b4a996dbec43b37df193662460d1079afc44a0b527e254e3f8f021d5641d56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11028281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46189612470021190d3bf104dd8f33f37f1935c418d35586a56103a51ae3eae`

```dockerfile
```

-	Layers:
	-	`sha256:92ec65cece960b7d57841f32ed0b7ef10f38a28aa7cba6a4854a8b334dcf3d99`  
		Last Modified: Thu, 23 May 2024 20:26:13 GMT  
		Size: 11.0 MB (11007977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342adbb441ff622538ae3927f0c48e1c840739511ef5f29a2e1b0e0bbdd07f32`  
		Last Modified: Thu, 23 May 2024 20:26:12 GMT  
		Size: 20.3 KB (20304 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:40d59c97924d201e55d78e02df7de0ffab60fc9ddb9cc67b76f4107347d3785f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c5b96fe713e4b9655e2e87bcb532cf9ed8f2844e205b4f6cf92d39592e2a7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.1 MB (539106492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbeea5a2b2292e1680ddf32602c8d092f106211520278f727feea0fc2c00a6fb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa282d1d447912112ea82af8315e469d48bf9c8fab8c92078346278d1ca610d`  
		Last Modified: Wed, 29 May 2024 23:01:40 GMT  
		Size: 125.2 MB (125175347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96db6d20d012ffc4596474d7e180f20bbdcc93e5fdcc5ab31e4143fdf4c2be32`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 9.5 KB (9545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f123ac5729d3ca167b4403cc68570dfdf36a4a8999455d488a56276cd726ae`  
		Last Modified: Wed, 29 May 2024 23:01:46 GMT  
		Size: 375.0 MB (375044503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ec9ed2a8fb4cb9a0762655d9b6b1df665b89621055123bb86da65cdf8b9982b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f394fd800b30ae01de41f9c43751677924836e4d53ac8c3803194ada788d34cd`

```dockerfile
```

-	Layers:
	-	`sha256:f7614b5e0f64af0fea72b62fb4ae2444fc559a68d3cc5e570bcd4c892e978db0`  
		Last Modified: Wed, 29 May 2024 23:01:38 GMT  
		Size: 5.2 MB (5220335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d840d67b8fdf084f1e1a970b865a0928e83b9c4d26988598b91f2b3100e195f`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 20.4 KB (20419 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d758b617678b252e51f56d02ea79f0e2d652ecc6599ff561f456cc49a962a7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.9 MB (541859874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930a633e518c25a7e070f6b634a621a22b7c02a63e25abb2476557c0037d6169`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18871374df4282d60741792b044d3274f56b0324c5f3cf1698b2c74d40f70133`  
		Last Modified: Thu, 23 May 2024 20:23:12 GMT  
		Size: 375.0 MB (375044566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7590a61dc4427200797682d8b5ae73e8eededfd36486301a6bd79463d7463549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ed3748b56b01a09823d1f8498f79031bb40c8136d9c08f633164e702dc815`

```dockerfile
```

-	Layers:
	-	`sha256:0fe01a711b7cd3c6ad7a3c46b8afcb7712244791d5ece662bac44e3c570995cb`  
		Last Modified: Thu, 23 May 2024 20:23:03 GMT  
		Size: 5.5 MB (5517615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c35eec85181e213a4cb7c2766b8250d164576294fc367824bd9ec22dbb6d19`  
		Last Modified: Thu, 23 May 2024 20:23:02 GMT  
		Size: 20.4 KB (20429 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-ubi8`

```console
$ docker pull neo4j@sha256:174c24a85061e67e0069b053503f910d3f0cae5cb6c6e0065f4cce0e166140a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:32cbb416370e6395daaf3b95ac131dec564cac65ebd8b27e26c654d65133d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318553085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e97f47ff28f7b87c10b925d19f4d1f9e509a3c1624fbac65cc332134f4b702`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc6187a0fd731729d24f55646f416bc3ac53dae4051e37ba1791907dc353d2`  
		Last Modified: Wed, 29 May 2024 23:02:12 GMT  
		Size: 152.7 MB (152702358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a775e1e93da20042a6e3321941989c270322a52b74ec25f978074bdc93314a`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b4516264bff29a7903cbcc7b72aa493e8d160c6b3d9af10d89a146a22a61a`  
		Last Modified: Wed, 29 May 2024 23:02:10 GMT  
		Size: 126.4 MB (126437727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:b94170a460c625301741d6d27852d18620699c7a2c443d512e6a3bf169a6b5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9267cd82f3eb15ff8c9669ef89cf15d73799cc9efff60bba860a7fc4fa42d9c`

```dockerfile
```

-	Layers:
	-	`sha256:b35af758a1fe96eecb756b8eec0d0f0367708085a3a92585e8a15763fba6f260`  
		Last Modified: Wed, 29 May 2024 23:02:07 GMT  
		Size: 10.3 MB (10309830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a9d2263602f865cbfb8b45a96b74e3be007b4352dc0cda57d2f546e6698e61`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2a36ce746f5048e927fabe90a45dd432d49d9cb6693dfeadae3bd27b28ad6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5c90bab334b69f502a5b54e965a0b55da157fc1810366abac62ae4ec87f50`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c9b59eb62b6cb3e10d4305fa98f4a86ba5be392111c9282db0ffe7308ac9`  
		Last Modified: Thu, 23 May 2024 20:24:09 GMT  
		Size: 126.4 MB (126437764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6291e1f2216d35268dc52906633b25865ffade29c5af3b423e77faddd3a1f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf2b4a260ee6000e9188e12cd7cafbcb9d64d7d91712b4aee26b8ee6f9b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:390d921c1db7a553ad402613206a652869a8e6517b8b984c7a8c5eb3238ef50a`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 10.8 MB (10836022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3fcfe97a8c4888af967e420a8a765dcd3c693c83e618376719f340c3709ecc`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.20.0-ubi9`

```console
$ docker pull neo4j@sha256:421eab133ca6a60b5a183ec2dfb87646b2d25ee2298a517f8aa817359b6becc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.20.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fbe08247a37171e18ad95cdf8a8937c3acca94c9fcd6916d9b8c5d8e2d78c069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290499980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b130ddf3e7e6965c61633e2435352d1a2c305f612813b585575eacf9f6e4cff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5cc4fd03dd9cf319fae048b3d49130421622ff27ee3ba632337bfea1731055`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 125.2 MB (125175459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d70a08f1f57303b5f1cf1e2a0e59ce34b1551bdeb5e225a2151d9d85dad7b1`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0718ff3010104007c6550a840d74362c5ccc2aa9544fea7edebc5814af39bd4`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 126.4 MB (126437882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a10e02f222fe61862238cc982f8c69c16c477cb51d04af96ed2d2701b827e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5069969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159824afc638e9979fa1981585b789e37f4828553704f42c317647abb2b41be1`

```dockerfile
```

-	Layers:
	-	`sha256:5052c04790fe485b5429e7d9f453f5affe9912b5213b318fc5e40febaf420fd6`  
		Last Modified: Wed, 29 May 2024 23:01:23 GMT  
		Size: 5.0 MB (5048372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff49b89847e506bb54bdec5ca49678572c74dd3dcb808e523b71fc452ec110ad`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 21.6 KB (21597 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.20.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b9db8386b33b03e76234054908369bf244df37985902ebe4e64c5cd9ea4f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293253160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104e4e7622d40bcc8deb3f3753c2d0c9997a1396349b3ae49088a8492bccf2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2a243ffd15909cb0b1d5aee2b729d0df3ba7017523afe1a5ffe07b9566e2c`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 126.4 MB (126437852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.20.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:43ece681b0d3f145dc0dba3b37195d5ceaa9c89ae624db68db316f7332b2b654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ab0c15bdbe4bc40ccbfcf22ef7ea242f6d9c2878415a0ffe133996a7bf65dc`

```dockerfile
```

-	Layers:
	-	`sha256:d2884a75a8e6ae30ebebd1428fd1674da40d18282eabfb4923980ee6ca3f182d`  
		Last Modified: Thu, 23 May 2024 20:22:04 GMT  
		Size: 5.3 MB (5345660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a6f2dadbe993eddb337437d8c6103ce00dde1033f695f953a5bf1edca90f30`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 21.6 KB (21614 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:174c24a85061e67e0069b053503f910d3f0cae5cb6c6e0065f4cce0e166140a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:32cbb416370e6395daaf3b95ac131dec564cac65ebd8b27e26c654d65133d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318553085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e97f47ff28f7b87c10b925d19f4d1f9e509a3c1624fbac65cc332134f4b702`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc6187a0fd731729d24f55646f416bc3ac53dae4051e37ba1791907dc353d2`  
		Last Modified: Wed, 29 May 2024 23:02:12 GMT  
		Size: 152.7 MB (152702358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a775e1e93da20042a6e3321941989c270322a52b74ec25f978074bdc93314a`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b4516264bff29a7903cbcc7b72aa493e8d160c6b3d9af10d89a146a22a61a`  
		Last Modified: Wed, 29 May 2024 23:02:10 GMT  
		Size: 126.4 MB (126437727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:b94170a460c625301741d6d27852d18620699c7a2c443d512e6a3bf169a6b5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9267cd82f3eb15ff8c9669ef89cf15d73799cc9efff60bba860a7fc4fa42d9c`

```dockerfile
```

-	Layers:
	-	`sha256:b35af758a1fe96eecb756b8eec0d0f0367708085a3a92585e8a15763fba6f260`  
		Last Modified: Wed, 29 May 2024 23:02:07 GMT  
		Size: 10.3 MB (10309830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a9d2263602f865cbfb8b45a96b74e3be007b4352dc0cda57d2f546e6698e61`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2a36ce746f5048e927fabe90a45dd432d49d9cb6693dfeadae3bd27b28ad6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5c90bab334b69f502a5b54e965a0b55da157fc1810366abac62ae4ec87f50`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c9b59eb62b6cb3e10d4305fa98f4a86ba5be392111c9282db0ffe7308ac9`  
		Last Modified: Thu, 23 May 2024 20:24:09 GMT  
		Size: 126.4 MB (126437764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6291e1f2216d35268dc52906633b25865ffade29c5af3b423e77faddd3a1f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf2b4a260ee6000e9188e12cd7cafbcb9d64d7d91712b4aee26b8ee6f9b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:390d921c1db7a553ad402613206a652869a8e6517b8b984c7a8c5eb3238ef50a`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 10.8 MB (10836022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3fcfe97a8c4888af967e420a8a765dcd3c693c83e618376719f340c3709ecc`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:421eab133ca6a60b5a183ec2dfb87646b2d25ee2298a517f8aa817359b6becc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fbe08247a37171e18ad95cdf8a8937c3acca94c9fcd6916d9b8c5d8e2d78c069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290499980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b130ddf3e7e6965c61633e2435352d1a2c305f612813b585575eacf9f6e4cff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5cc4fd03dd9cf319fae048b3d49130421622ff27ee3ba632337bfea1731055`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 125.2 MB (125175459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d70a08f1f57303b5f1cf1e2a0e59ce34b1551bdeb5e225a2151d9d85dad7b1`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0718ff3010104007c6550a840d74362c5ccc2aa9544fea7edebc5814af39bd4`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 126.4 MB (126437882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a10e02f222fe61862238cc982f8c69c16c477cb51d04af96ed2d2701b827e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5069969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159824afc638e9979fa1981585b789e37f4828553704f42c317647abb2b41be1`

```dockerfile
```

-	Layers:
	-	`sha256:5052c04790fe485b5429e7d9f453f5affe9912b5213b318fc5e40febaf420fd6`  
		Last Modified: Wed, 29 May 2024 23:01:23 GMT  
		Size: 5.0 MB (5048372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff49b89847e506bb54bdec5ca49678572c74dd3dcb808e523b71fc452ec110ad`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 21.6 KB (21597 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b9db8386b33b03e76234054908369bf244df37985902ebe4e64c5cd9ea4f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293253160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104e4e7622d40bcc8deb3f3753c2d0c9997a1396349b3ae49088a8492bccf2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2a243ffd15909cb0b1d5aee2b729d0df3ba7017523afe1a5ffe07b9566e2c`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 126.4 MB (126437852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:43ece681b0d3f145dc0dba3b37195d5ceaa9c89ae624db68db316f7332b2b654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ab0c15bdbe4bc40ccbfcf22ef7ea242f6d9c2878415a0ffe133996a7bf65dc`

```dockerfile
```

-	Layers:
	-	`sha256:d2884a75a8e6ae30ebebd1428fd1674da40d18282eabfb4923980ee6ca3f182d`  
		Last Modified: Thu, 23 May 2024 20:22:04 GMT  
		Size: 5.3 MB (5345660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a6f2dadbe993eddb337437d8c6103ce00dde1033f695f953a5bf1edca90f30`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 21.6 KB (21614 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:96ed8f0263af6df62e4a9c97a0d7d3385a9246552d4f71216a1a5d254d834efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:66726b01c23895a1084489dfd87fa50a91bb581d8baa5e1b7c9d5ffbde7f7c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8e8b67aa823d777e80932e26871a2bf731572e900d060eafac61608751dac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7140eb8418e2f1e4ec777450d0cd2029e40037913c0c75c03264741f799505`  
		Last Modified: Thu, 23 May 2024 19:53:23 GMT  
		Size: 145.1 MB (145095105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca207659e997c876e0bd01b4773794d68c33dad138b06ff52836fe83c26072`  
		Last Modified: Thu, 23 May 2024 19:53:22 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac23d1712489bcaa8f1870cd4521811d0a137b98912a4652ad4456568bd428`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d9b87d62d53ca3fed3c460b5d697a7819bf383c27fd7fc4d76c8956b8ae13`  
		Last Modified: Thu, 23 May 2024 19:53:27 GMT  
		Size: 378.0 MB (377982829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e04faed0382154d75b05d599b50a5a8cd3f9d85b45033e6be9a9d4eff332d46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72284afa4c4d1b75f7fa67f3aa064a2dfd2823f1587cecf2bf725d97b7a53a1c`

```dockerfile
```

-	Layers:
	-	`sha256:300775d4e659043fc37df266505586253aa303f5d54783659d6ca92061cc8e75`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 3.1 MB (3133588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecc313528fb69d381d41eaee78edc007ec3bd7766cab8a61ec040656609e172`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02dbaf8393e1e2278ab62a3f055323a0f3cfc5d3120b9fa9c706f70d632f5b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605dfe6aceb871e8a7fad54dae819a1b3f753ef8a173e743e21fc767915ec300`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a1b4ddaedf474eed62e08e5cb26e9cc60202af6e41601cbec8277ceec547d`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307aa617531d51b5102a0ba95fed2d83edd9f645319e78de5c88513c327e1aa5`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab1fa2dd0b518a33513cca36ea0ff19b8a917a25a56e7133098cb8339cfeae`  
		Last Modified: Thu, 23 May 2024 20:20:52 GMT  
		Size: 377.9 MB (377944374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0d4911eb640a7643d0593bc655cf4ba4247a1f495d3d5a8ebf2e62021f023f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49875f55ee6d72344cb25583ed99d79436ea63c56c2aa2c330fa13d8baaef592`

```dockerfile
```

-	Layers:
	-	`sha256:775f7456d4802dfa3ca3dd8c95dfea9302345a66b2cb148221b9084845181371`  
		Last Modified: Thu, 23 May 2024 20:20:45 GMT  
		Size: 3.1 MB (3133814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55560658428a4b2c8ea5484cc0947e74a230d6fe078e652383a1230330e8151`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:96ed8f0263af6df62e4a9c97a0d7d3385a9246552d4f71216a1a5d254d834efa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:66726b01c23895a1084489dfd87fa50a91bb581d8baa5e1b7c9d5ffbde7f7c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.5 MB (554525283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8e8b67aa823d777e80932e26871a2bf731572e900d060eafac61608751dac`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7140eb8418e2f1e4ec777450d0cd2029e40037913c0c75c03264741f799505`  
		Last Modified: Thu, 23 May 2024 19:53:23 GMT  
		Size: 145.1 MB (145095105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca207659e997c876e0bd01b4773794d68c33dad138b06ff52836fe83c26072`  
		Last Modified: Thu, 23 May 2024 19:53:22 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ac23d1712489bcaa8f1870cd4521811d0a137b98912a4652ad4456568bd428`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d9b87d62d53ca3fed3c460b5d697a7819bf383c27fd7fc4d76c8956b8ae13`  
		Last Modified: Thu, 23 May 2024 19:53:27 GMT  
		Size: 378.0 MB (377982829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:e04faed0382154d75b05d599b50a5a8cd3f9d85b45033e6be9a9d4eff332d46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72284afa4c4d1b75f7fa67f3aa064a2dfd2823f1587cecf2bf725d97b7a53a1c`

```dockerfile
```

-	Layers:
	-	`sha256:300775d4e659043fc37df266505586253aa303f5d54783659d6ca92061cc8e75`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 3.1 MB (3133588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecc313528fb69d381d41eaee78edc007ec3bd7766cab8a61ec040656609e172`  
		Last Modified: Thu, 23 May 2024 19:53:21 GMT  
		Size: 21.9 KB (21896 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:02dbaf8393e1e2278ab62a3f055323a0f3cfc5d3120b9fa9c706f70d632f5b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.9 MB (551937492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605dfe6aceb871e8a7fad54dae819a1b3f753ef8a173e743e21fc767915ec300`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7a1b4ddaedf474eed62e08e5cb26e9cc60202af6e41601cbec8277ceec547d`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307aa617531d51b5102a0ba95fed2d83edd9f645319e78de5c88513c327e1aa5`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab1fa2dd0b518a33513cca36ea0ff19b8a917a25a56e7133098cb8339cfeae`  
		Last Modified: Thu, 23 May 2024 20:20:52 GMT  
		Size: 377.9 MB (377944374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0d4911eb640a7643d0593bc655cf4ba4247a1f495d3d5a8ebf2e62021f023f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49875f55ee6d72344cb25583ed99d79436ea63c56c2aa2c330fa13d8baaef592`

```dockerfile
```

-	Layers:
	-	`sha256:775f7456d4802dfa3ca3dd8c95dfea9302345a66b2cb148221b9084845181371`  
		Last Modified: Thu, 23 May 2024 20:20:45 GMT  
		Size: 3.1 MB (3133814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55560658428a4b2c8ea5484cc0947e74a230d6fe078e652383a1230330e8151`  
		Last Modified: Thu, 23 May 2024 20:20:44 GMT  
		Size: 20.9 KB (20929 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:32e2cc6bdc443a9bc0db086229eea05327e708ecb4d87266831069cb0cb00fc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:2e558a362958975656595c5e5cb1f6495f43fc0cd9d5fee190377ad99895689a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **567.2 MB (567159179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9814602a179f230d461f1abb0324b82f01248a57ad9d06e2711462a1452c2c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfcd43411737dea6f06e538e1fcf81a7b05bf289e098cc0eb881a1a00f0f61b`  
		Last Modified: Wed, 29 May 2024 23:02:02 GMT  
		Size: 152.7 MB (152701878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fc403fbd6759c9fbbf6f2cb1649bbbe131b1bcc278a2489510690713e38472`  
		Last Modified: Wed, 29 May 2024 23:01:59 GMT  
		Size: 9.7 KB (9724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d802a6ba47cc2a4c6727bf0e665be16f412eb5583b513feebf9a46bd2bb55c6`  
		Last Modified: Wed, 29 May 2024 23:02:05 GMT  
		Size: 375.0 MB (375044303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:3b7425a6d84a59fe500924d1f56d3aac3553290e223204f12ffa098c019dded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cd8832e0be39f36aa8660593c86d42e12a7c5fcc07a58361409c9710e2b570`

```dockerfile
```

-	Layers:
	-	`sha256:b8674afb488ddbee727bf25264230293f79ee8f8476c449a4bbf57d5f247b9d7`  
		Last Modified: Wed, 29 May 2024 23:02:00 GMT  
		Size: 10.5 MB (10481793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b594f464f47c2d3f4fe142db2e6e884fb34e9cab7b55be18c4c763b528fd074`  
		Last Modified: Wed, 29 May 2024 23:01:59 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1f9880330569341a38c64ec3541140400028768e7b0e1d6a389cddc2c240e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **575.7 MB (575732100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a677531841215346abdcb1ac7135052fcdd950df3e669eb567958498ef3e071f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8296248cd807a837a6dc3acb0ce0aeecba90d737c9f1cc67a91b96515e652ff`  
		Last Modified: Thu, 23 May 2024 20:26:20 GMT  
		Size: 375.0 MB (375044344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2b4a996dbec43b37df193662460d1079afc44a0b527e254e3f8f021d5641d56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11028281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46189612470021190d3bf104dd8f33f37f1935c418d35586a56103a51ae3eae`

```dockerfile
```

-	Layers:
	-	`sha256:92ec65cece960b7d57841f32ed0b7ef10f38a28aa7cba6a4854a8b334dcf3d99`  
		Last Modified: Thu, 23 May 2024 20:26:13 GMT  
		Size: 11.0 MB (11007977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342adbb441ff622538ae3927f0c48e1c840739511ef5f29a2e1b0e0bbdd07f32`  
		Last Modified: Thu, 23 May 2024 20:26:12 GMT  
		Size: 20.3 KB (20304 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:40d59c97924d201e55d78e02df7de0ffab60fc9ddb9cc67b76f4107347d3785f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c5b96fe713e4b9655e2e87bcb532cf9ed8f2844e205b4f6cf92d39592e2a7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **539.1 MB (539106492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbeea5a2b2292e1680ddf32602c8d092f106211520278f727feea0fc2c00a6fb`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa282d1d447912112ea82af8315e469d48bf9c8fab8c92078346278d1ca610d`  
		Last Modified: Wed, 29 May 2024 23:01:40 GMT  
		Size: 125.2 MB (125175347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96db6d20d012ffc4596474d7e180f20bbdcc93e5fdcc5ab31e4143fdf4c2be32`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 9.5 KB (9545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f123ac5729d3ca167b4403cc68570dfdf36a4a8999455d488a56276cd726ae`  
		Last Modified: Wed, 29 May 2024 23:01:46 GMT  
		Size: 375.0 MB (375044503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:ec9ed2a8fb4cb9a0762655d9b6b1df665b89621055123bb86da65cdf8b9982b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f394fd800b30ae01de41f9c43751677924836e4d53ac8c3803194ada788d34cd`

```dockerfile
```

-	Layers:
	-	`sha256:f7614b5e0f64af0fea72b62fb4ae2444fc559a68d3cc5e570bcd4c892e978db0`  
		Last Modified: Wed, 29 May 2024 23:01:38 GMT  
		Size: 5.2 MB (5220335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d840d67b8fdf084f1e1a970b865a0928e83b9c4d26988598b91f2b3100e195f`  
		Last Modified: Wed, 29 May 2024 23:01:37 GMT  
		Size: 20.4 KB (20419 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d758b617678b252e51f56d02ea79f0e2d652ecc6599ff561f456cc49a962a7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.9 MB (541859874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930a633e518c25a7e070f6b634a621a22b7c02a63e25abb2476557c0037d6169`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18871374df4282d60741792b044d3274f56b0324c5f3cf1698b2c74d40f70133`  
		Last Modified: Thu, 23 May 2024 20:23:12 GMT  
		Size: 375.0 MB (375044566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:7590a61dc4427200797682d8b5ae73e8eededfd36486301a6bd79463d7463549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767ed3748b56b01a09823d1f8498f79031bb40c8136d9c08f633164e702dc815`

```dockerfile
```

-	Layers:
	-	`sha256:0fe01a711b7cd3c6ad7a3c46b8afcb7712244791d5ece662bac44e3c570995cb`  
		Last Modified: Thu, 23 May 2024 20:23:03 GMT  
		Size: 5.5 MB (5517615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c35eec85181e213a4cb7c2766b8250d164576294fc367824bd9ec22dbb6d19`  
		Last Modified: Thu, 23 May 2024 20:23:02 GMT  
		Size: 20.4 KB (20429 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:890907c12da70c04a9e5160ea32de66358ddd8295f18a1c2df66e6492291cee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:402fe025da16d72429ba055afee5bdbe3b7d1e831e105e5fcd6ea67b965d7bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305910085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9548f351e39396ae48fb68fe3b4dbfc2f95768150e50f4ade4f5cb080c4a78f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f89178c139ea023dc2322f0b6c9fff3c82836211b15c3ea1a0f4eed181ffbe`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 145.1 MB (145095079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0146762310cc02f49842d9830b045be8d94b9364eaca471d2e86bd24ca6f6025`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde07d3877b258a2b96d0b6ad63b2890934ac6d50f37a340c07b021643ebc477`  
		Last Modified: Thu, 23 May 2024 20:50:22 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564492095d3cd785c15aa4de86f2c69579f618c947808a1b10206da977ad65d`  
		Last Modified: Thu, 23 May 2024 20:50:25 GMT  
		Size: 129.4 MB (129367663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:22097205384d87fece729882f43ebf4ede63c9e5ac80c8634ca754608daa4cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302ed8c6035301fbda7917bb6a7970c4316624744b8e2a8ee672bae95bd535db`

```dockerfile
```

-	Layers:
	-	`sha256:dc29957faf8d8132bad6630ae594f92ad28b5fcc14a96aabc15505e8f2dda1a6`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 3.0 MB (2962819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3092617ce0f653016311f3dfac77158e70b20d862c334063d2424df25217bd`  
		Last Modified: Thu, 23 May 2024 20:50:23 GMT  
		Size: 24.3 KB (24265 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:91da822ccec48ebd0d6d2dfb0d7d3854c74f3e897dc90b02771a0e7a2b78d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303326692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6688e2b3e8debc31b085364a477e705b576bc1c1f73bca0236908ca9dc7e562e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae3f6df449a6f6309553ee04449bf9aaae43df104c7c9a7ec3cc2a89fe5993`  
		Last Modified: Tue, 14 May 2024 17:53:05 GMT  
		Size: 143.9 MB (143892777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c487a291072c37a5281831e1b729109d3c1424f3e72d521c6f41771b3ec4cca5`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4d3db3c8b15ffe2ccb0b74f93ebf149d75dd67a07d51b1168567aa7d90fd7c`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12185fe18c7593bc4b5fc896da56d63aeb955d99910ad29bd6d31441f80e091d`  
		Last Modified: Thu, 23 May 2024 20:19:36 GMT  
		Size: 129.3 MB (129333571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:a566f2ccedf13482ed9d82bc5fdee74ad643dd4e857ee8696d5baed17f4cbd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2986374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecb0b598f61dc90e82c3fcd49578456bda8e36469882edcc7e7e597a2383de8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4e48085f3f6032dffb19a150c7e3355c66bff7f34741f456d67ba619c017ff`  
		Last Modified: Thu, 23 May 2024 20:19:33 GMT  
		Size: 3.0 MB (2963061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9841772168f26e7cda01c02b78f57f105716a496dbaf6bd9beaea5e0c65f6515`  
		Last Modified: Thu, 23 May 2024 20:19:32 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:174c24a85061e67e0069b053503f910d3f0cae5cb6c6e0065f4cce0e166140a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:32cbb416370e6395daaf3b95ac131dec564cac65ebd8b27e26c654d65133d128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318553085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e97f47ff28f7b87c10b925d19f4d1f9e509a3c1624fbac65cc332134f4b702`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:e76a8d5e39e8ff7fa7e47a8a5ed2db86895d4f0557cea48d94939d051f1657c1 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e5208c6531a6e864b82aebe72b97633f8dbec4240858738c29bb3805ffc229f in /etc/yum.repos.d/ 
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
ADD file:d755e4424cc6cb08d1136e3546f11149e0af8be288bc1476334494b1c143a120 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.1716497715.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5f72c47620e6aa97958da35e810c2c2660c69affedeeda3d93145f71648d5cb3 in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896.1716497715 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="896.1716497715" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T20:59:38" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896.1716497715"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3106617-08c97.repo' '/etc/yum.repos.d/rhel-8.10-compose-0e878.repo'
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
	-	`sha256:bd0cfa3ba2edc49b46d73384d730e68ece0f02d2fc80427c93ae5318aa2f50ba`  
		Last Modified: Tue, 28 May 2024 09:54:17 GMT  
		Size: 39.4 MB (39403242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc6187a0fd731729d24f55646f416bc3ac53dae4051e37ba1791907dc353d2`  
		Last Modified: Wed, 29 May 2024 23:02:12 GMT  
		Size: 152.7 MB (152702358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a775e1e93da20042a6e3321941989c270322a52b74ec25f978074bdc93314a`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 9.7 KB (9726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874b4516264bff29a7903cbcc7b72aa493e8d160c6b3d9af10d89a146a22a61a`  
		Last Modified: Wed, 29 May 2024 23:02:10 GMT  
		Size: 126.4 MB (126437727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:b94170a460c625301741d6d27852d18620699c7a2c443d512e6a3bf169a6b5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9267cd82f3eb15ff8c9669ef89cf15d73799cc9efff60bba860a7fc4fa42d9c`

```dockerfile
```

-	Layers:
	-	`sha256:b35af758a1fe96eecb756b8eec0d0f0367708085a3a92585e8a15763fba6f260`  
		Last Modified: Wed, 29 May 2024 23:02:07 GMT  
		Size: 10.3 MB (10309830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a9d2263602f865cbfb8b45a96b74e3be007b4352dc0cda57d2f546e6698e61`  
		Last Modified: Wed, 29 May 2024 23:02:06 GMT  
		Size: 21.5 KB (21473 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:2a36ce746f5048e927fabe90a45dd432d49d9cb6693dfeadae3bd27b28ad6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb5c90bab334b69f502a5b54e965a0b55da157fc1810366abac62ae4ec87f50`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 14 May 2024 18:16:05 GMT
ADD file:c7aced2d2a3aa5493f8d58fef04235995cabee8d71951e23e24d32ef3469feb1 in / 
# Tue, 14 May 2024 18:16:06 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Tue, 14 May 2024 18:16:06 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Tue, 14 May 2024 18:16:06 GMT
ADD multi:9d0854b3f4f2506b2a90463a22b056026ce8ed50a75cee8dbd4447e0b97889fa in /etc/yum.repos.d/ 
# Tue, 14 May 2024 18:16:06 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.10"
# Tue, 14 May 2024 18:16:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 14 May 2024 18:16:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Tue, 14 May 2024 18:16:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.expose-services=""
# Tue, 14 May 2024 18:16:06 GMT
LABEL io.openshift.tags="minimal rhel8"
# Tue, 14 May 2024 18:16:06 GMT
ENV container oci
# Tue, 14 May 2024 18:16:06 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 18:16:06 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 18:16:08 GMT
RUN rm -rf /var/log/*
# Tue, 14 May 2024 18:16:08 GMT
LABEL release=896
# Tue, 14 May 2024 18:16:08 GMT
ADD file:8dbdd797984c6152317aeeac42811b5b62a446523ffb28517a0bb8abcd758bb3 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.10-896.json 
# Tue, 14 May 2024 18:16:08 GMT
ADD file:6af1ef774b6dc1a29e853e6b50d382bb6d8a8e2cb31f1fc058e7fdc064a0978d in /root/buildinfo/Dockerfile-ubi8-minimal-8.10-896 
# Tue, 14 May 2024 18:16:08 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-14T17:55:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7357243bfe6a2392090af428c41ba6d13fe68590" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.10-896"
# Tue, 14 May 2024 18:16:09 GMT
RUN rm -f '/etc/yum.repos.d/repo-a40a0.repo' '/etc/yum.repos.d/repo-bb379.repo'
# Tue, 14 May 2024 18:16:10 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Tue, 14 May 2024 18:16:12 GMT
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
	-	`sha256:ab78d51305cfafe4bf2a939f88c79a59ace7854610512a0bc6d24f7ea0d1540c`  
		Last Modified: Wed, 22 May 2024 13:49:30 GMT  
		Size: 37.7 MB (37673848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283fa4ea779d791c03816eeb7b600e35eb9027ce9a2d8021d271455925f52a58`  
		Last Modified: Thu, 23 May 2024 07:36:21 GMT  
		Size: 163.0 MB (163004166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62b14ab0abab919bfa80a02c9e27f127431f92e387f027d422149b66b562ce5`  
		Last Modified: Thu, 23 May 2024 20:24:00 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608c9b59eb62b6cb3e10d4305fa98f4a86ba5be392111c9282db0ffe7308ac9`  
		Last Modified: Thu, 23 May 2024 20:24:09 GMT  
		Size: 126.4 MB (126437764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:6291e1f2216d35268dc52906633b25865ffade29c5af3b423e77faddd3a1f62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10857513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdf2b4a260ee6000e9188e12cd7cafbcb9d64d7d91712b4aee26b8ee6f9b3c1`

```dockerfile
```

-	Layers:
	-	`sha256:390d921c1db7a553ad402613206a652869a8e6517b8b984c7a8c5eb3238ef50a`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 10.8 MB (10836022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3fcfe97a8c4888af967e420a8a765dcd3c693c83e618376719f340c3709ecc`  
		Last Modified: Thu, 23 May 2024 20:24:01 GMT  
		Size: 21.5 KB (21491 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:421eab133ca6a60b5a183ec2dfb87646b2d25ee2298a517f8aa817359b6becc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:fbe08247a37171e18ad95cdf8a8937c3acca94c9fcd6916d9b8c5d8e2d78c069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.5 MB (290499980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b130ddf3e7e6965c61633e2435352d1a2c305f612813b585575eacf9f6e4cff`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 23 May 2024 10:12:20 GMT
ADD file:2853019fb5062d9ddbe9a00ce8d69abd9c77dc27a92d0916b1b58324b73c8025 in / 
# Thu, 23 May 2024 10:12:20 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 23 May 2024 10:12:20 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 23 May 2024 10:12:20 GMT
ADD multi:9e111fe87abb88c147eef501698b720ace4a55fea6c2cefb58b36419afd47460 in /etc/yum.repos.d/ 
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
ADD file:18b284325bdf076af4a7ec16bd2e0e88cf3a5867dcb1fbf78c832341428ffc7c in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1716471857.json 
# Thu, 23 May 2024 10:12:20 GMT
ADD file:028809d600161529d0b52d671fd12d867bd33bbfd1a26fd35f139c8a31e26483 in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1716471857 
# Thu, 23 May 2024 10:12:20 GMT
LABEL "release"="949.1716471857" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-23T13:47:36" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1716471857"
# Thu, 23 May 2024 10:12:20 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3103507-55f7b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
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
	-	`sha256:570d5d7d3a6a72fe2fa36c5d2c31cde66a5b88741d1336218422745bd35cf321`  
		Last Modified: Tue, 28 May 2024 15:00:00 GMT  
		Size: 38.9 MB (38877065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5cc4fd03dd9cf319fae048b3d49130421622ff27ee3ba632337bfea1731055`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 125.2 MB (125175459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d70a08f1f57303b5f1cf1e2a0e59ce34b1551bdeb5e225a2151d9d85dad7b1`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0718ff3010104007c6550a840d74362c5ccc2aa9544fea7edebc5814af39bd4`  
		Last Modified: Wed, 29 May 2024 23:01:24 GMT  
		Size: 126.4 MB (126437882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8a10e02f222fe61862238cc982f8c69c16c477cb51d04af96ed2d2701b827e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5069969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159824afc638e9979fa1981585b789e37f4828553704f42c317647abb2b41be1`

```dockerfile
```

-	Layers:
	-	`sha256:5052c04790fe485b5429e7d9f453f5affe9912b5213b318fc5e40febaf420fd6`  
		Last Modified: Wed, 29 May 2024 23:01:23 GMT  
		Size: 5.0 MB (5048372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff49b89847e506bb54bdec5ca49678572c74dd3dcb808e523b71fc452ec110ad`  
		Last Modified: Wed, 29 May 2024 23:01:22 GMT  
		Size: 21.6 KB (21597 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:6b9db8386b33b03e76234054908369bf244df37985902ebe4e64c5cd9ea4f56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.3 MB (293253160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104e4e7622d40bcc8deb3f3753c2d0c9997a1396349b3ae49088a8492bccf2df`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 02 May 2024 15:39:54 GMT
ADD file:64ec164ec6824f7f5315c6b92aa679b834b744e93866622ed6275a74c95044df in / 
# Thu, 02 May 2024 15:39:55 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 02 May 2024 15:39:55 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 02 May 2024 15:39:55 GMT
ADD multi:bba82b2c530381d750ea64baaac8ed3e48c924899e721737bc8d6b93fa43f96d in /etc/yum.repos.d/ 
# Thu, 02 May 2024 15:39:55 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 02 May 2024 15:39:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 02 May 2024 15:39:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 02 May 2024 15:39:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.expose-services=""
# Thu, 02 May 2024 15:39:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 02 May 2024 15:39:55 GMT
ENV container oci
# Thu, 02 May 2024 15:39:55 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 15:39:55 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 15:39:57 GMT
RUN rm -rf /var/log/*
# Thu, 02 May 2024 15:39:57 GMT
ADD file:504fa4e582282d72e34a7b86d423f73d40478fcf621b8bfb86af63ee405088ed in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-949.1714662671.json 
# Thu, 02 May 2024 15:39:57 GMT
ADD file:f8d27e45663c02bc2603f266cf0eb3b9dc8c37b04c0f1f0775bda4758d09ddfb in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-949.1714662671 
# Thu, 02 May 2024 15:39:57 GMT
LABEL "release"="949.1714662671" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-05-02T15:15:48" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4b4efbdd5a311b6a9c56319e756ca58c10a2b4de" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-949.1714662671"
# Thu, 02 May 2024 15:39:58 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3029549-719f4.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 02 May 2024 15:39:59 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 02 May 2024 15:40:01 GMT
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
	-	`sha256:e118b45596900675775a6359d1f05008d9a4a750c50eb18862ce0c097abc0326`  
		Last Modified: Mon, 06 May 2024 14:15:20 GMT  
		Size: 37.1 MB (37090800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333548b48331bfbc9a202257e7b02b4e31acee08751a2c95f77911f89a24e673`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 129.7 MB (129714937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3342b2af1e8a8b5715f6cca65ece2c8190fa99eb01ce226c096b3af6b4db5a12`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2a243ffd15909cb0b1d5aee2b729d0df3ba7017523afe1a5ffe07b9566e2c`  
		Last Modified: Thu, 23 May 2024 20:22:06 GMT  
		Size: 126.4 MB (126437852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:43ece681b0d3f145dc0dba3b37195d5ceaa9c89ae624db68db316f7332b2b654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ab0c15bdbe4bc40ccbfcf22ef7ea242f6d9c2878415a0ffe133996a7bf65dc`

```dockerfile
```

-	Layers:
	-	`sha256:d2884a75a8e6ae30ebebd1428fd1674da40d18282eabfb4923980ee6ca3f182d`  
		Last Modified: Thu, 23 May 2024 20:22:04 GMT  
		Size: 5.3 MB (5345660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a6f2dadbe993eddb337437d8c6103ce00dde1033f695f953a5bf1edca90f30`  
		Last Modified: Thu, 23 May 2024 20:22:03 GMT  
		Size: 21.6 KB (21614 bytes)  
		MIME: application/vnd.in-toto+json
