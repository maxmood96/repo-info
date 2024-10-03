<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.37`](#neo4j4437)
-	[`neo4j:4.4.37-community`](#neo4j4437-community)
-	[`neo4j:4.4.37-enterprise`](#neo4j4437-enterprise)
-	[`neo4j:5`](#neo4j5)
-	[`neo4j:5-bullseye`](#neo4j5-bullseye)
-	[`neo4j:5-community`](#neo4j5-community)
-	[`neo4j:5-community-bullseye`](#neo4j5-community-bullseye)
-	[`neo4j:5-community-ubi9`](#neo4j5-community-ubi9)
-	[`neo4j:5-enterprise`](#neo4j5-enterprise)
-	[`neo4j:5-enterprise-bullseye`](#neo4j5-enterprise-bullseye)
-	[`neo4j:5-enterprise-ubi9`](#neo4j5-enterprise-ubi9)
-	[`neo4j:5-ubi9`](#neo4j5-ubi9)
-	[`neo4j:5.24`](#neo4j524)
-	[`neo4j:5.24-bullseye`](#neo4j524-bullseye)
-	[`neo4j:5.24-community`](#neo4j524-community)
-	[`neo4j:5.24-community-bullseye`](#neo4j524-community-bullseye)
-	[`neo4j:5.24-community-ubi9`](#neo4j524-community-ubi9)
-	[`neo4j:5.24-enterprise`](#neo4j524-enterprise)
-	[`neo4j:5.24-enterprise-bullseye`](#neo4j524-enterprise-bullseye)
-	[`neo4j:5.24-enterprise-ubi9`](#neo4j524-enterprise-ubi9)
-	[`neo4j:5.24-ubi9`](#neo4j524-ubi9)
-	[`neo4j:5.24.1`](#neo4j5241)
-	[`neo4j:5.24.1-bullseye`](#neo4j5241-bullseye)
-	[`neo4j:5.24.1-community`](#neo4j5241-community)
-	[`neo4j:5.24.1-community-bullseye`](#neo4j5241-community-bullseye)
-	[`neo4j:5.24.1-community-ubi9`](#neo4j5241-community-ubi9)
-	[`neo4j:5.24.1-enterprise`](#neo4j5241-enterprise)
-	[`neo4j:5.24.1-enterprise-bullseye`](#neo4j5241-enterprise-bullseye)
-	[`neo4j:5.24.1-enterprise-ubi9`](#neo4j5241-enterprise-ubi9)
-	[`neo4j:5.24.1-ubi9`](#neo4j5241-ubi9)
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
$ docker pull neo4j@sha256:fb19dd9fcc831b2c48027cd4854cdde19bc0a6895df007b0034e7da270e25545
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:3168ac6cf2311794958763c86b011575747ecaa2b6981d5ff67845d665aa3199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303072769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2d3b5cb4cbfcc41bef7bd447e93ece3f1491985331df156d2ae4b6c55c827a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc3dd69242c7921cc0144a016d1a5174daa96a5b4e10548faff5f9c54bd9498`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 145.5 MB (145549847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aae421918ec2514815900a1d216ae68d4dbc7b4ec3741815c6a8d41aa7ec3e`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55a0f9054515adb9a9142a7f93fad5e282809a704f076e0d441eeb43d668f0c`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c074c5037df8a115de5d5962e6691965deb32ee6b94303825434c2207e20b187`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 126.1 MB (126080930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f9b83aeea2ccfa510edf31741e51919948bea4e8509333604f647a9356a0892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88decb5567890b41ebe1a9fdbee6f7e2e619c5542d028ee07e963b201e47bdb`

```dockerfile
```

-	Layers:
	-	`sha256:972c0a9dfd500f2db70606d93f22cb9ffd4f5c9fc506e246a01a7db3b149aabc`  
		Last Modified: Wed, 02 Oct 2024 02:59:18 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b2a8853f2562752f05b19b72cc28ca2a0842f82ce9ade86e2b51de34c5572c`  
		Last Modified: Wed, 02 Oct 2024 02:59:18 GMT  
		Size: 19.6 KB (19596 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0115637e077ee5a279da383f1374b0cc1264834e457c925f0839bf09ebe11962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298487630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522d7e64901713bd09e9cd2981eb6bdae1935432ff3a79ae43166216c9452c3e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30149fff09dc33f83b6ab4318fbe4dd4f83df2dc3e54bf33b92b83879e58b67b`  
		Last Modified: Wed, 02 Oct 2024 02:12:34 GMT  
		Size: 142.4 MB (142354841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e2af0ab1fcf0531cbcce35f9d72e52bd6b2ccf158da1efac892465554f390`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b968945b04843bc77c445aebd56986b7792d49b4dad5647622077ab4549f8a`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa8910a5cd1eac983e21273d0c521dcf54e7ae353cd18939d6996bf87f4e951`  
		Last Modified: Wed, 02 Oct 2024 03:23:49 GMT  
		Size: 126.0 MB (126044210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:0055941a30e7ca12bd407564e525aa9e7ff32aecebf07f3fafc3e27917d16c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ebcceb1ea8983978a89e44a48d6da054e58ff67c554e1ba71b46b386a7cfd2`

```dockerfile
```

-	Layers:
	-	`sha256:e378e49ed68a2b3dad6cf4e1b38f88af8871e59a678c2a4ef158d65feb4c4c8d`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58927597aa019c049070eaec8df4ceceda74acc3da387d8f046f6fb33e95bdba`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:fb19dd9fcc831b2c48027cd4854cdde19bc0a6895df007b0034e7da270e25545
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3168ac6cf2311794958763c86b011575747ecaa2b6981d5ff67845d665aa3199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303072769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2d3b5cb4cbfcc41bef7bd447e93ece3f1491985331df156d2ae4b6c55c827a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc3dd69242c7921cc0144a016d1a5174daa96a5b4e10548faff5f9c54bd9498`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 145.5 MB (145549847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aae421918ec2514815900a1d216ae68d4dbc7b4ec3741815c6a8d41aa7ec3e`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55a0f9054515adb9a9142a7f93fad5e282809a704f076e0d441eeb43d668f0c`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c074c5037df8a115de5d5962e6691965deb32ee6b94303825434c2207e20b187`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 126.1 MB (126080930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f9b83aeea2ccfa510edf31741e51919948bea4e8509333604f647a9356a0892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88decb5567890b41ebe1a9fdbee6f7e2e619c5542d028ee07e963b201e47bdb`

```dockerfile
```

-	Layers:
	-	`sha256:972c0a9dfd500f2db70606d93f22cb9ffd4f5c9fc506e246a01a7db3b149aabc`  
		Last Modified: Wed, 02 Oct 2024 02:59:18 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b2a8853f2562752f05b19b72cc28ca2a0842f82ce9ade86e2b51de34c5572c`  
		Last Modified: Wed, 02 Oct 2024 02:59:18 GMT  
		Size: 19.6 KB (19596 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0115637e077ee5a279da383f1374b0cc1264834e457c925f0839bf09ebe11962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298487630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522d7e64901713bd09e9cd2981eb6bdae1935432ff3a79ae43166216c9452c3e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30149fff09dc33f83b6ab4318fbe4dd4f83df2dc3e54bf33b92b83879e58b67b`  
		Last Modified: Wed, 02 Oct 2024 02:12:34 GMT  
		Size: 142.4 MB (142354841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e2af0ab1fcf0531cbcce35f9d72e52bd6b2ccf158da1efac892465554f390`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b968945b04843bc77c445aebd56986b7792d49b4dad5647622077ab4549f8a`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa8910a5cd1eac983e21273d0c521dcf54e7ae353cd18939d6996bf87f4e951`  
		Last Modified: Wed, 02 Oct 2024 03:23:49 GMT  
		Size: 126.0 MB (126044210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0055941a30e7ca12bd407564e525aa9e7ff32aecebf07f3fafc3e27917d16c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ebcceb1ea8983978a89e44a48d6da054e58ff67c554e1ba71b46b386a7cfd2`

```dockerfile
```

-	Layers:
	-	`sha256:e378e49ed68a2b3dad6cf4e1b38f88af8871e59a678c2a4ef158d65feb4c4c8d`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58927597aa019c049070eaec8df4ceceda74acc3da387d8f046f6fb33e95bdba`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:cbfbff62c9d091c5932ee194d727eb7893aa0d5069410525babab94798cb963c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fa89cde86228f2398fc3c687e53d92a47b236ec95f746348389c34cb2ec3571c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407242338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7084ccb3e64abdde99380261c8c0ffcf6977e75ba23a0e812709ade77617c0c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cce711def6761647f11a49a3248a338024ef42471387ec25cb0c3ec1d5239a6 NEO4J_TARBALL=neo4j-enterprise-4.4.37-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc3dd69242c7921cc0144a016d1a5174daa96a5b4e10548faff5f9c54bd9498`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 145.5 MB (145549847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aae421918ec2514815900a1d216ae68d4dbc7b4ec3741815c6a8d41aa7ec3e`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7400e1f25dea355da0a5de93549eac5b69170423b034e603919cf7632fc1ae45`  
		Last Modified: Wed, 02 Oct 2024 02:59:30 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f2b21cd2a05b661c3bd1a192fbcf6f6be8968e31659b4fbee0dadb570fcfaa`  
		Last Modified: Wed, 02 Oct 2024 02:59:33 GMT  
		Size: 230.3 MB (230250500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e9354bb21436d817395bec40f38d9d5dd5061e48c08c29890911eb57d24dc774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6a318be959b87833219a3b771b779cc177819d5c8f2d0eabdf2be968bcaf32`

```dockerfile
```

-	Layers:
	-	`sha256:580958298fa71ed5488703cc353d05c6644568d05621642b7e244ddeeb1cfd13`  
		Last Modified: Wed, 02 Oct 2024 02:59:30 GMT  
		Size: 3.3 MB (3302201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320364e54891a5efcb2a0fecb53dd2243109bff9a9ce5e1c6b6e18843f76b2b0`  
		Last Modified: Wed, 02 Oct 2024 02:59:30 GMT  
		Size: 19.0 KB (19027 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1623dfaeed6a65a0a59434388a295b38bbd12eac8ea27c247a70d50c0cfe2603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402658432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3314339dc1bbd8a3c1f3d027dc7ec7ac78a4af1c061ad23320531cf6fcf7ceb9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cce711def6761647f11a49a3248a338024ef42471387ec25cb0c3ec1d5239a6 NEO4J_TARBALL=neo4j-enterprise-4.4.37-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30149fff09dc33f83b6ab4318fbe4dd4f83df2dc3e54bf33b92b83879e58b67b`  
		Last Modified: Wed, 02 Oct 2024 02:12:34 GMT  
		Size: 142.4 MB (142354841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b296ca3b64f4745a48b267cc07f32a1c372feb54497f5e4e1142f5755f2ac72`  
		Last Modified: Wed, 02 Oct 2024 03:24:52 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66ed96190f12bffe4ec1d041b2fda99626c65611d7527eb0bdf32dd6e45719b`  
		Last Modified: Wed, 02 Oct 2024 03:24:51 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da682f50e4ed1eb2ba5b44d08dc22e21f4fe12347bca850d737ef1df7a6c875a`  
		Last Modified: Wed, 02 Oct 2024 03:24:57 GMT  
		Size: 230.2 MB (230215014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ddd1c51ca4265853d80dc3e6258f0788b6cbd1e17e439001a4e31a00dd85d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f993ae52c59a5f59341737ddb9850512c989d6bdc2b1c0f2307cfc60aa0477`

```dockerfile
```

-	Layers:
	-	`sha256:77e00f9f1730ee87f91e75e1c0ccb7bf2671954f3334dba6453a36f5dde9870a`  
		Last Modified: Wed, 02 Oct 2024 03:24:52 GMT  
		Size: 3.3 MB (3302440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c2f3627510023f7c722ab89fd305e37f4c6294b0d9eecef78a7a8dc73d0a0b`  
		Last Modified: Wed, 02 Oct 2024 03:24:51 GMT  
		Size: 19.1 KB (19136 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.37`

```console
$ docker pull neo4j@sha256:fb19dd9fcc831b2c48027cd4854cdde19bc0a6895df007b0034e7da270e25545
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.37` - linux; amd64

```console
$ docker pull neo4j@sha256:3168ac6cf2311794958763c86b011575747ecaa2b6981d5ff67845d665aa3199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303072769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2d3b5cb4cbfcc41bef7bd447e93ece3f1491985331df156d2ae4b6c55c827a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc3dd69242c7921cc0144a016d1a5174daa96a5b4e10548faff5f9c54bd9498`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 145.5 MB (145549847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aae421918ec2514815900a1d216ae68d4dbc7b4ec3741815c6a8d41aa7ec3e`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55a0f9054515adb9a9142a7f93fad5e282809a704f076e0d441eeb43d668f0c`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c074c5037df8a115de5d5962e6691965deb32ee6b94303825434c2207e20b187`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 126.1 MB (126080930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f9b83aeea2ccfa510edf31741e51919948bea4e8509333604f647a9356a0892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88decb5567890b41ebe1a9fdbee6f7e2e619c5542d028ee07e963b201e47bdb`

```dockerfile
```

-	Layers:
	-	`sha256:972c0a9dfd500f2db70606d93f22cb9ffd4f5c9fc506e246a01a7db3b149aabc`  
		Last Modified: Wed, 02 Oct 2024 02:59:18 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b2a8853f2562752f05b19b72cc28ca2a0842f82ce9ade86e2b51de34c5572c`  
		Last Modified: Wed, 02 Oct 2024 02:59:18 GMT  
		Size: 19.6 KB (19596 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.37` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0115637e077ee5a279da383f1374b0cc1264834e457c925f0839bf09ebe11962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298487630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522d7e64901713bd09e9cd2981eb6bdae1935432ff3a79ae43166216c9452c3e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30149fff09dc33f83b6ab4318fbe4dd4f83df2dc3e54bf33b92b83879e58b67b`  
		Last Modified: Wed, 02 Oct 2024 02:12:34 GMT  
		Size: 142.4 MB (142354841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e2af0ab1fcf0531cbcce35f9d72e52bd6b2ccf158da1efac892465554f390`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b968945b04843bc77c445aebd56986b7792d49b4dad5647622077ab4549f8a`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa8910a5cd1eac983e21273d0c521dcf54e7ae353cd18939d6996bf87f4e951`  
		Last Modified: Wed, 02 Oct 2024 03:23:49 GMT  
		Size: 126.0 MB (126044210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37` - unknown; unknown

```console
$ docker pull neo4j@sha256:0055941a30e7ca12bd407564e525aa9e7ff32aecebf07f3fafc3e27917d16c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ebcceb1ea8983978a89e44a48d6da054e58ff67c554e1ba71b46b386a7cfd2`

```dockerfile
```

-	Layers:
	-	`sha256:e378e49ed68a2b3dad6cf4e1b38f88af8871e59a678c2a4ef158d65feb4c4c8d`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58927597aa019c049070eaec8df4ceceda74acc3da387d8f046f6fb33e95bdba`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.37-community`

```console
$ docker pull neo4j@sha256:fb19dd9fcc831b2c48027cd4854cdde19bc0a6895df007b0034e7da270e25545
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.37-community` - linux; amd64

```console
$ docker pull neo4j@sha256:3168ac6cf2311794958763c86b011575747ecaa2b6981d5ff67845d665aa3199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303072769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2d3b5cb4cbfcc41bef7bd447e93ece3f1491985331df156d2ae4b6c55c827a`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc3dd69242c7921cc0144a016d1a5174daa96a5b4e10548faff5f9c54bd9498`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 145.5 MB (145549847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aae421918ec2514815900a1d216ae68d4dbc7b4ec3741815c6a8d41aa7ec3e`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55a0f9054515adb9a9142a7f93fad5e282809a704f076e0d441eeb43d668f0c`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c074c5037df8a115de5d5962e6691965deb32ee6b94303825434c2207e20b187`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 126.1 MB (126080930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:1f9b83aeea2ccfa510edf31741e51919948bea4e8509333604f647a9356a0892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88decb5567890b41ebe1a9fdbee6f7e2e619c5542d028ee07e963b201e47bdb`

```dockerfile
```

-	Layers:
	-	`sha256:972c0a9dfd500f2db70606d93f22cb9ffd4f5c9fc506e246a01a7db3b149aabc`  
		Last Modified: Wed, 02 Oct 2024 02:59:18 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b2a8853f2562752f05b19b72cc28ca2a0842f82ce9ade86e2b51de34c5572c`  
		Last Modified: Wed, 02 Oct 2024 02:59:18 GMT  
		Size: 19.6 KB (19596 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.37-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0115637e077ee5a279da383f1374b0cc1264834e457c925f0839bf09ebe11962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298487630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522d7e64901713bd09e9cd2981eb6bdae1935432ff3a79ae43166216c9452c3e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=1df748bf54206d4cbf2c9e19bab9c43120df054f466469c93099afd41c3f2cd8 NEO4J_TARBALL=neo4j-community-4.4.37-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30149fff09dc33f83b6ab4318fbe4dd4f83df2dc3e54bf33b92b83879e58b67b`  
		Last Modified: Wed, 02 Oct 2024 02:12:34 GMT  
		Size: 142.4 MB (142354841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e2af0ab1fcf0531cbcce35f9d72e52bd6b2ccf158da1efac892465554f390`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b968945b04843bc77c445aebd56986b7792d49b4dad5647622077ab4549f8a`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa8910a5cd1eac983e21273d0c521dcf54e7ae353cd18939d6996bf87f4e951`  
		Last Modified: Wed, 02 Oct 2024 03:23:49 GMT  
		Size: 126.0 MB (126044210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0055941a30e7ca12bd407564e525aa9e7ff32aecebf07f3fafc3e27917d16c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ebcceb1ea8983978a89e44a48d6da054e58ff67c554e1ba71b46b386a7cfd2`

```dockerfile
```

-	Layers:
	-	`sha256:e378e49ed68a2b3dad6cf4e1b38f88af8871e59a678c2a4ef158d65feb4c4c8d`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58927597aa019c049070eaec8df4ceceda74acc3da387d8f046f6fb33e95bdba`  
		Last Modified: Wed, 02 Oct 2024 03:23:46 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.37-enterprise`

```console
$ docker pull neo4j@sha256:cbfbff62c9d091c5932ee194d727eb7893aa0d5069410525babab94798cb963c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.37-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:fa89cde86228f2398fc3c687e53d92a47b236ec95f746348389c34cb2ec3571c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407242338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7084ccb3e64abdde99380261c8c0ffcf6977e75ba23a0e812709ade77617c0c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cce711def6761647f11a49a3248a338024ef42471387ec25cb0c3ec1d5239a6 NEO4J_TARBALL=neo4j-enterprise-4.4.37-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc3dd69242c7921cc0144a016d1a5174daa96a5b4e10548faff5f9c54bd9498`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 145.5 MB (145549847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aae421918ec2514815900a1d216ae68d4dbc7b4ec3741815c6a8d41aa7ec3e`  
		Last Modified: Wed, 02 Oct 2024 02:59:17 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7400e1f25dea355da0a5de93549eac5b69170423b034e603919cf7632fc1ae45`  
		Last Modified: Wed, 02 Oct 2024 02:59:30 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f2b21cd2a05b661c3bd1a192fbcf6f6be8968e31659b4fbee0dadb570fcfaa`  
		Last Modified: Wed, 02 Oct 2024 02:59:33 GMT  
		Size: 230.3 MB (230250500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:e9354bb21436d817395bec40f38d9d5dd5061e48c08c29890911eb57d24dc774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6a318be959b87833219a3b771b779cc177819d5c8f2d0eabdf2be968bcaf32`

```dockerfile
```

-	Layers:
	-	`sha256:580958298fa71ed5488703cc353d05c6644568d05621642b7e244ddeeb1cfd13`  
		Last Modified: Wed, 02 Oct 2024 02:59:30 GMT  
		Size: 3.3 MB (3302201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320364e54891a5efcb2a0fecb53dd2243109bff9a9ce5e1c6b6e18843f76b2b0`  
		Last Modified: Wed, 02 Oct 2024 02:59:30 GMT  
		Size: 19.0 KB (19027 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.37-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:1623dfaeed6a65a0a59434388a295b38bbd12eac8ea27c247a70d50c0cfe2603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402658432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3314339dc1bbd8a3c1f3d027dc7ec7ac78a4af1c061ad23320531cf6fcf7ceb9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 03 Sep 2024 13:35:21 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 13:35:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Sep 2024 13:35:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cce711def6761647f11a49a3248a338024ef42471387ec25cb0c3ec1d5239a6 NEO4J_TARBALL=neo4j-enterprise-4.4.37-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Tue, 03 Sep 2024 13:35:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.37-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Tue, 03 Sep 2024 13:35:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 13:35:21 GMT
WORKDIR /var/lib/neo4j
# Tue, 03 Sep 2024 13:35:21 GMT
VOLUME [/data /logs]
# Tue, 03 Sep 2024 13:35:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Tue, 03 Sep 2024 13:35:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Tue, 03 Sep 2024 13:35:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30149fff09dc33f83b6ab4318fbe4dd4f83df2dc3e54bf33b92b83879e58b67b`  
		Last Modified: Wed, 02 Oct 2024 02:12:34 GMT  
		Size: 142.4 MB (142354841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b296ca3b64f4745a48b267cc07f32a1c372feb54497f5e4e1142f5755f2ac72`  
		Last Modified: Wed, 02 Oct 2024 03:24:52 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66ed96190f12bffe4ec1d041b2fda99626c65611d7527eb0bdf32dd6e45719b`  
		Last Modified: Wed, 02 Oct 2024 03:24:51 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da682f50e4ed1eb2ba5b44d08dc22e21f4fe12347bca850d737ef1df7a6c875a`  
		Last Modified: Wed, 02 Oct 2024 03:24:57 GMT  
		Size: 230.2 MB (230215014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3ddd1c51ca4265853d80dc3e6258f0788b6cbd1e17e439001a4e31a00dd85d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f993ae52c59a5f59341737ddb9850512c989d6bdc2b1c0f2307cfc60aa0477`

```dockerfile
```

-	Layers:
	-	`sha256:77e00f9f1730ee87f91e75e1c0ccb7bf2671954f3334dba6453a36f5dde9870a`  
		Last Modified: Wed, 02 Oct 2024 03:24:52 GMT  
		Size: 3.3 MB (3302440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c2f3627510023f7c722ab89fd305e37f4c6294b0d9eecef78a7a8dc73d0a0b`  
		Last Modified: Wed, 02 Oct 2024 03:24:51 GMT  
		Size: 19.1 KB (19136 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:1c7b2197f0fcb5d9ed6456804121667262b3cd0cee8f9e6889d17e265c0b3cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:58665334ba82501643877e06327de5406c3f079706e84e6017556828a7774925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2c1adfcb59b9b5dd03aad4ef62fd50776902fa038c7e74b59b3f4546ac5b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d935cee01c732d4722d7a7727d92848dbd8229a2c30591c16c6c7b00418277`  
		Last Modified: Wed, 02 Oct 2024 02:59:22 GMT  
		Size: 145.2 MB (145166528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c34f444a07358def36a5ae4b90f14c15cacfa0b7e854ec13852b09b7cfd1b0f`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3a5a8ff936a268696d467125a422ea978319807026ef6bc5be10789ca063e`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ade805ded6479b4db6e8171c44d657b9861f25ca1e42a38d14a802c0b5aa5e`  
		Last Modified: Wed, 02 Oct 2024 02:59:23 GMT  
		Size: 127.3 MB (127275142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:7b10c70da51727d23af98b1d0514c52cefbcba9deb68cf13db23d79db8e94c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9701f91d801823895f343ce9993fe2f066c8308b45153b437160ffc5c49e551`

```dockerfile
```

-	Layers:
	-	`sha256:7fe14d30fc4b595a17c2f57793ff8957f211b2b726bec7c13f11df81c8fc5af1`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b33e418c793b6cf45a23d2729151bc3646be6127891e651edd8307122b80f9c`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13dcb70f7bdfd061ee08230885ccbdf1ac446f5a0ddad0d5e7c16c9e93cf3cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91034df5644d0684bec8328c2780afa24c79fda52d6c8ff58f1e1a6fa4916d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac86c75abfa1438961120af68547a82316efc45175dd99bd0991973d91602`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da34dbbe75bd1251df5ec2c1e6b4c3b6c98c93335576651d7f951e7ee8d452a`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b326abc798852973a1c0c17d9e74846d6855ebd6e0e667779c7122cb6cfd7d6`  
		Last Modified: Wed, 02 Oct 2024 03:21:05 GMT  
		Size: 127.2 MB (127242634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a18ea06a4e2784097670ff7059fad93c4003c68e5b3a53889fa336faa86e792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868989d9a63f365a3bc5b3b2791179d136ec3a4af5dd9d514172dda858460177`

```dockerfile
```

-	Layers:
	-	`sha256:b1fbaa5abc0d38d06f7acf7533f911d82194a5c12f21a7df274521907cfd6193`  
		Last Modified: Wed, 02 Oct 2024 03:21:03 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424dfd47453071312aac8f8b67e972719901aad42db58e9aa532449d7178a5ae`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:1c7b2197f0fcb5d9ed6456804121667262b3cd0cee8f9e6889d17e265c0b3cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58665334ba82501643877e06327de5406c3f079706e84e6017556828a7774925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2c1adfcb59b9b5dd03aad4ef62fd50776902fa038c7e74b59b3f4546ac5b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d935cee01c732d4722d7a7727d92848dbd8229a2c30591c16c6c7b00418277`  
		Last Modified: Wed, 02 Oct 2024 02:59:22 GMT  
		Size: 145.2 MB (145166528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c34f444a07358def36a5ae4b90f14c15cacfa0b7e854ec13852b09b7cfd1b0f`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3a5a8ff936a268696d467125a422ea978319807026ef6bc5be10789ca063e`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ade805ded6479b4db6e8171c44d657b9861f25ca1e42a38d14a802c0b5aa5e`  
		Last Modified: Wed, 02 Oct 2024 02:59:23 GMT  
		Size: 127.3 MB (127275142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7b10c70da51727d23af98b1d0514c52cefbcba9deb68cf13db23d79db8e94c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9701f91d801823895f343ce9993fe2f066c8308b45153b437160ffc5c49e551`

```dockerfile
```

-	Layers:
	-	`sha256:7fe14d30fc4b595a17c2f57793ff8957f211b2b726bec7c13f11df81c8fc5af1`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b33e418c793b6cf45a23d2729151bc3646be6127891e651edd8307122b80f9c`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13dcb70f7bdfd061ee08230885ccbdf1ac446f5a0ddad0d5e7c16c9e93cf3cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91034df5644d0684bec8328c2780afa24c79fda52d6c8ff58f1e1a6fa4916d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac86c75abfa1438961120af68547a82316efc45175dd99bd0991973d91602`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da34dbbe75bd1251df5ec2c1e6b4c3b6c98c93335576651d7f951e7ee8d452a`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b326abc798852973a1c0c17d9e74846d6855ebd6e0e667779c7122cb6cfd7d6`  
		Last Modified: Wed, 02 Oct 2024 03:21:05 GMT  
		Size: 127.2 MB (127242634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a18ea06a4e2784097670ff7059fad93c4003c68e5b3a53889fa336faa86e792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868989d9a63f365a3bc5b3b2791179d136ec3a4af5dd9d514172dda858460177`

```dockerfile
```

-	Layers:
	-	`sha256:b1fbaa5abc0d38d06f7acf7533f911d82194a5c12f21a7df274521907cfd6193`  
		Last Modified: Wed, 02 Oct 2024 03:21:03 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424dfd47453071312aac8f8b67e972719901aad42db58e9aa532449d7178a5ae`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:1c7b2197f0fcb5d9ed6456804121667262b3cd0cee8f9e6889d17e265c0b3cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:58665334ba82501643877e06327de5406c3f079706e84e6017556828a7774925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2c1adfcb59b9b5dd03aad4ef62fd50776902fa038c7e74b59b3f4546ac5b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d935cee01c732d4722d7a7727d92848dbd8229a2c30591c16c6c7b00418277`  
		Last Modified: Wed, 02 Oct 2024 02:59:22 GMT  
		Size: 145.2 MB (145166528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c34f444a07358def36a5ae4b90f14c15cacfa0b7e854ec13852b09b7cfd1b0f`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3a5a8ff936a268696d467125a422ea978319807026ef6bc5be10789ca063e`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ade805ded6479b4db6e8171c44d657b9861f25ca1e42a38d14a802c0b5aa5e`  
		Last Modified: Wed, 02 Oct 2024 02:59:23 GMT  
		Size: 127.3 MB (127275142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:7b10c70da51727d23af98b1d0514c52cefbcba9deb68cf13db23d79db8e94c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9701f91d801823895f343ce9993fe2f066c8308b45153b437160ffc5c49e551`

```dockerfile
```

-	Layers:
	-	`sha256:7fe14d30fc4b595a17c2f57793ff8957f211b2b726bec7c13f11df81c8fc5af1`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b33e418c793b6cf45a23d2729151bc3646be6127891e651edd8307122b80f9c`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13dcb70f7bdfd061ee08230885ccbdf1ac446f5a0ddad0d5e7c16c9e93cf3cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91034df5644d0684bec8328c2780afa24c79fda52d6c8ff58f1e1a6fa4916d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac86c75abfa1438961120af68547a82316efc45175dd99bd0991973d91602`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da34dbbe75bd1251df5ec2c1e6b4c3b6c98c93335576651d7f951e7ee8d452a`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b326abc798852973a1c0c17d9e74846d6855ebd6e0e667779c7122cb6cfd7d6`  
		Last Modified: Wed, 02 Oct 2024 03:21:05 GMT  
		Size: 127.2 MB (127242634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a18ea06a4e2784097670ff7059fad93c4003c68e5b3a53889fa336faa86e792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868989d9a63f365a3bc5b3b2791179d136ec3a4af5dd9d514172dda858460177`

```dockerfile
```

-	Layers:
	-	`sha256:b1fbaa5abc0d38d06f7acf7533f911d82194a5c12f21a7df274521907cfd6193`  
		Last Modified: Wed, 02 Oct 2024 03:21:03 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424dfd47453071312aac8f8b67e972719901aad42db58e9aa532449d7178a5ae`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:1c7b2197f0fcb5d9ed6456804121667262b3cd0cee8f9e6889d17e265c0b3cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58665334ba82501643877e06327de5406c3f079706e84e6017556828a7774925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2c1adfcb59b9b5dd03aad4ef62fd50776902fa038c7e74b59b3f4546ac5b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d935cee01c732d4722d7a7727d92848dbd8229a2c30591c16c6c7b00418277`  
		Last Modified: Wed, 02 Oct 2024 02:59:22 GMT  
		Size: 145.2 MB (145166528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c34f444a07358def36a5ae4b90f14c15cacfa0b7e854ec13852b09b7cfd1b0f`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3a5a8ff936a268696d467125a422ea978319807026ef6bc5be10789ca063e`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ade805ded6479b4db6e8171c44d657b9861f25ca1e42a38d14a802c0b5aa5e`  
		Last Modified: Wed, 02 Oct 2024 02:59:23 GMT  
		Size: 127.3 MB (127275142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7b10c70da51727d23af98b1d0514c52cefbcba9deb68cf13db23d79db8e94c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9701f91d801823895f343ce9993fe2f066c8308b45153b437160ffc5c49e551`

```dockerfile
```

-	Layers:
	-	`sha256:7fe14d30fc4b595a17c2f57793ff8957f211b2b726bec7c13f11df81c8fc5af1`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b33e418c793b6cf45a23d2729151bc3646be6127891e651edd8307122b80f9c`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13dcb70f7bdfd061ee08230885ccbdf1ac446f5a0ddad0d5e7c16c9e93cf3cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91034df5644d0684bec8328c2780afa24c79fda52d6c8ff58f1e1a6fa4916d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac86c75abfa1438961120af68547a82316efc45175dd99bd0991973d91602`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da34dbbe75bd1251df5ec2c1e6b4c3b6c98c93335576651d7f951e7ee8d452a`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b326abc798852973a1c0c17d9e74846d6855ebd6e0e667779c7122cb6cfd7d6`  
		Last Modified: Wed, 02 Oct 2024 03:21:05 GMT  
		Size: 127.2 MB (127242634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a18ea06a4e2784097670ff7059fad93c4003c68e5b3a53889fa336faa86e792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868989d9a63f365a3bc5b3b2791179d136ec3a4af5dd9d514172dda858460177`

```dockerfile
```

-	Layers:
	-	`sha256:b1fbaa5abc0d38d06f7acf7533f911d82194a5c12f21a7df274521907cfd6193`  
		Last Modified: Wed, 02 Oct 2024 03:21:03 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424dfd47453071312aac8f8b67e972719901aad42db58e9aa532449d7178a5ae`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:c77cd5d0d7930ecb4580f2ddb19e7423f6ba1435a3a3faa4165e5e05945f27b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0098560ed9a805f66cb221afeacc75786af6853dfde846f4803b8b414917059a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288881588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb77b9a32219305cb8b70b0595648e2303428f12a9d6cefe9159d2c63a8005f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d83d28c3ec134ab55df59638494812485d08170e15afd59ab5c97b1a7d8a8f`  
		Last Modified: Tue, 24 Sep 2024 01:00:40 GMT  
		Size: 125.4 MB (125421564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870f203580c59bfdcc2ffdb4f700745fda689be118fe7ada23459d8de3adf89a`  
		Last Modified: Tue, 24 Sep 2024 01:00:29 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744de09bc8f096be6c252b419afba26bddf9aa48c1c1f24cba1b0d390140afa`  
		Last Modified: Tue, 24 Sep 2024 01:00:31 GMT  
		Size: 124.3 MB (124348666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e981219ef42811e3a6c660fbff9e0ee2eb3c97bdbaff75ef6228f90c16b20f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71d74c4f7dbbf4aeff5c0f8efda90b46f16ef4d0a14d10d4626fcc9d485c4a`

```dockerfile
```

-	Layers:
	-	`sha256:6b4509003f57a092d99ec6d78a85374ec2f36f4e558a841f1c92c201bb6f72a9`  
		Last Modified: Tue, 24 Sep 2024 01:00:29 GMT  
		Size: 21.5 KB (21541 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b434eff505440dcc5f1300b7d9593b92bede39ddf5671c45957c149f377b284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287152268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100909fbb1b910412e47364cdd30cdc03111552e43af49fc93b1b95b20098a0c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3b708771449b1058f44f70932e1fa3868e1876107200b42fa17ab54d8ac089`  
		Last Modified: Tue, 24 Sep 2024 01:12:58 GMT  
		Size: 125.5 MB (125458540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d44a2f712becd634bcbe851a9ebdf018848d6c2e32bf8b2b0ba37b7c95cff`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46aa237c5a48019c4e9f67746ca7c30e2980798b04e4277c2d5ba80c70db7b9`  
		Last Modified: Tue, 24 Sep 2024 01:12:59 GMT  
		Size: 124.3 MB (124348656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:cf28fc857e6f49c6f7093163c5c3213d8c223c802a65431b92a7bd21ea95deb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd1ba6e0ec09093d45a1034696b3986742ef28383629290966b124d58efb73`

```dockerfile
```

-	Layers:
	-	`sha256:c9b24924c6f572004d9933f2d27a0a279594cea367b25b993f6e9adc5338a6a3`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 5.2 MB (5236424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9ffcfef31d3564087854428f3f9bbd7bf021fc5ed241f9164419d84f66dc54`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:20eb19e3d60f9f07c12c89eac8d8722e393be7e45c6d7e56004a2c493b8e2032
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:75474ba2e65bb99d3db5af62793bfa59d93e029a9b5af0228dc40199a3b356ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996d41a3868b10d956a98cc462c07d3fe1caec76400deba09068f5173b2415b7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1673cb44d5ff17b2b047fb5e1b3d90664aa7974f1c88ee4b3cff5899f1295b3`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 145.2 MB (145166509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00efd9813924815509302df1a98bae91516f68ead8ce6fdeb73ee82e876cba30`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a960959b94579c301984c7c79f7cadf4feb48f868f44aac2a518ce69e07f6e1d`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8218a43e0f72f5dd96cbf2a18155ba5720886c86bb783cf43e72769c05d109ce`  
		Last Modified: Wed, 02 Oct 2024 02:59:49 GMT  
		Size: 410.5 MB (410499185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3834913397e1d8b9723b0809332b285176f6b07e625f0b9bd17028bd56889160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748035d3340215f2d2adaa62767322130a30f6feb7df762d6e93bfb3b66fdcba`

```dockerfile
```

-	Layers:
	-	`sha256:2a919e97d07e444dc8ef297a50a01fa3064bc4ec20f82a4ec9653c3461937c2b`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07470de5ea31e0b89bb89e444b8be15011204b4028a3e591ca376a20da23e538`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 21.0 KB (21020 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d22431c9e6bf24550d5247206c30f3c18088e044468a114b8dbf9ddcc7e9d034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9160a03f2de508875f42891f871df91ee97f10b8c3e705150c404c144f417e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464555d7c1fa8910a4a9406e6e6c756235875214eb559a0c388509a758e36755`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38f14431d475169e0738488b259c4e8963782a82ae18614ae84b14e0f17c81`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b4b9f5e759fcc5fc268f3b21012594db25ab21e86224b7752c2406045a875f`  
		Last Modified: Wed, 02 Oct 2024 03:22:42 GMT  
		Size: 410.5 MB (410461075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3647952a054bc223149f2e5b40f9bf80a938a9a587e4310e0da75418c4e5d467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88e2135a47cf6fa1018d51b183225fb15f44249a51d832d24dc436690ef4e72`

```dockerfile
```

-	Layers:
	-	`sha256:74a11e5c2cda1795b8b911af24b2e12c45f3afe1fd3eb47da4e8d1ec721d0ade`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da34dff3f2bc8e6954ef51fcacb54093fe632fee32601daffe0474e30a873f0a`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 21.2 KB (21201 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:20eb19e3d60f9f07c12c89eac8d8722e393be7e45c6d7e56004a2c493b8e2032
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:75474ba2e65bb99d3db5af62793bfa59d93e029a9b5af0228dc40199a3b356ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996d41a3868b10d956a98cc462c07d3fe1caec76400deba09068f5173b2415b7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1673cb44d5ff17b2b047fb5e1b3d90664aa7974f1c88ee4b3cff5899f1295b3`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 145.2 MB (145166509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00efd9813924815509302df1a98bae91516f68ead8ce6fdeb73ee82e876cba30`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a960959b94579c301984c7c79f7cadf4feb48f868f44aac2a518ce69e07f6e1d`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8218a43e0f72f5dd96cbf2a18155ba5720886c86bb783cf43e72769c05d109ce`  
		Last Modified: Wed, 02 Oct 2024 02:59:49 GMT  
		Size: 410.5 MB (410499185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3834913397e1d8b9723b0809332b285176f6b07e625f0b9bd17028bd56889160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748035d3340215f2d2adaa62767322130a30f6feb7df762d6e93bfb3b66fdcba`

```dockerfile
```

-	Layers:
	-	`sha256:2a919e97d07e444dc8ef297a50a01fa3064bc4ec20f82a4ec9653c3461937c2b`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07470de5ea31e0b89bb89e444b8be15011204b4028a3e591ca376a20da23e538`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 21.0 KB (21020 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d22431c9e6bf24550d5247206c30f3c18088e044468a114b8dbf9ddcc7e9d034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9160a03f2de508875f42891f871df91ee97f10b8c3e705150c404c144f417e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464555d7c1fa8910a4a9406e6e6c756235875214eb559a0c388509a758e36755`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38f14431d475169e0738488b259c4e8963782a82ae18614ae84b14e0f17c81`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b4b9f5e759fcc5fc268f3b21012594db25ab21e86224b7752c2406045a875f`  
		Last Modified: Wed, 02 Oct 2024 03:22:42 GMT  
		Size: 410.5 MB (410461075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3647952a054bc223149f2e5b40f9bf80a938a9a587e4310e0da75418c4e5d467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88e2135a47cf6fa1018d51b183225fb15f44249a51d832d24dc436690ef4e72`

```dockerfile
```

-	Layers:
	-	`sha256:74a11e5c2cda1795b8b911af24b2e12c45f3afe1fd3eb47da4e8d1ec721d0ade`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da34dff3f2bc8e6954ef51fcacb54093fe632fee32601daffe0474e30a873f0a`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 21.2 KB (21201 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f59e1c59f081b7ce91f88566f8eb7f6e68b5e7dab182c718cab3a0234c41e865
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:00de8405641c3906ac0870b927cf918c65ef95c891be0b93d9e931e8c7fac235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572100400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb15e28d84d25c2da9a5232ab5345e4674c667ee1ff4cc78fc5982d3c214ccc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ddfd76485f79816a994af03e07f81ee0c26d4c555265dc88e431ebbb6fee20`  
		Last Modified: Tue, 24 Sep 2024 01:01:05 GMT  
		Size: 125.4 MB (125421178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b59dbfef883969f961184a0d8560874ebb1a97f145ea42a515f7c7b0eb7bdae`  
		Last Modified: Tue, 24 Sep 2024 01:01:01 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba43c06803d528425ab4076d700fa88099832f6ea43e74b6f3b4fe22310a70`  
		Last Modified: Tue, 24 Sep 2024 01:01:11 GMT  
		Size: 407.6 MB (407567866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0888dc285bb2dc044a5f4afcf39f75536886fac737576e67540677413ed546d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833fe7cd0b2aab3c01ebee2c497ecaa3e0cc85a792cfa58b45b7b72904de2b57`

```dockerfile
```

-	Layers:
	-	`sha256:5bde44f1792bcfb4f97422ea6906284d9a2e0d72af82131ae16d8328f3192b0d`  
		Last Modified: Tue, 24 Sep 2024 01:01:01 GMT  
		Size: 20.4 KB (20363 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d81ca8cc0509d3aff0ea4a20d49d3846607a1a1ff1def2e51ec278541be84808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.4 MB (570371572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4ec1334d7ef63e23205a70a572f6d5a7d5b6e4b3bf29dd5ae13a4e2bbbdd34`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3b708771449b1058f44f70932e1fa3868e1876107200b42fa17ab54d8ac089`  
		Last Modified: Tue, 24 Sep 2024 01:12:58 GMT  
		Size: 125.5 MB (125458540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d44a2f712becd634bcbe851a9ebdf018848d6c2e32bf8b2b0ba37b7c95cff`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4345f5d20350eb93081102690fe65aa682534dab079fc921857e60ba42559243`  
		Last Modified: Tue, 24 Sep 2024 01:14:03 GMT  
		Size: 407.6 MB (407567960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:28cc26443537185525d9dfbc931bbe1f296050ce2225312a92a0c8e9c875ec48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9024a6d2dd8890aa63c2a6d9859d5ee22edd5309239caef9d338e4479a0a9420`

```dockerfile
```

-	Layers:
	-	`sha256:5cfbe26c48cfa6bd9510f45a86d9c17fd152e76fcd881f6e3e109cb2b9314a50`  
		Last Modified: Tue, 24 Sep 2024 01:13:55 GMT  
		Size: 5.5 MB (5517469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a16b7ec254cf43803685ccb33216dd7c8d65ebd34eb5ad4854819dc3e6210712`  
		Last Modified: Tue, 24 Sep 2024 01:13:54 GMT  
		Size: 20.9 KB (20890 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:c77cd5d0d7930ecb4580f2ddb19e7423f6ba1435a3a3faa4165e5e05945f27b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0098560ed9a805f66cb221afeacc75786af6853dfde846f4803b8b414917059a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288881588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb77b9a32219305cb8b70b0595648e2303428f12a9d6cefe9159d2c63a8005f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d83d28c3ec134ab55df59638494812485d08170e15afd59ab5c97b1a7d8a8f`  
		Last Modified: Tue, 24 Sep 2024 01:00:40 GMT  
		Size: 125.4 MB (125421564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870f203580c59bfdcc2ffdb4f700745fda689be118fe7ada23459d8de3adf89a`  
		Last Modified: Tue, 24 Sep 2024 01:00:29 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744de09bc8f096be6c252b419afba26bddf9aa48c1c1f24cba1b0d390140afa`  
		Last Modified: Tue, 24 Sep 2024 01:00:31 GMT  
		Size: 124.3 MB (124348666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e981219ef42811e3a6c660fbff9e0ee2eb3c97bdbaff75ef6228f90c16b20f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71d74c4f7dbbf4aeff5c0f8efda90b46f16ef4d0a14d10d4626fcc9d485c4a`

```dockerfile
```

-	Layers:
	-	`sha256:6b4509003f57a092d99ec6d78a85374ec2f36f4e558a841f1c92c201bb6f72a9`  
		Last Modified: Tue, 24 Sep 2024 01:00:29 GMT  
		Size: 21.5 KB (21541 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b434eff505440dcc5f1300b7d9593b92bede39ddf5671c45957c149f377b284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287152268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100909fbb1b910412e47364cdd30cdc03111552e43af49fc93b1b95b20098a0c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3b708771449b1058f44f70932e1fa3868e1876107200b42fa17ab54d8ac089`  
		Last Modified: Tue, 24 Sep 2024 01:12:58 GMT  
		Size: 125.5 MB (125458540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d44a2f712becd634bcbe851a9ebdf018848d6c2e32bf8b2b0ba37b7c95cff`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46aa237c5a48019c4e9f67746ca7c30e2980798b04e4277c2d5ba80c70db7b9`  
		Last Modified: Tue, 24 Sep 2024 01:12:59 GMT  
		Size: 124.3 MB (124348656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:cf28fc857e6f49c6f7093163c5c3213d8c223c802a65431b92a7bd21ea95deb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd1ba6e0ec09093d45a1034696b3986742ef28383629290966b124d58efb73`

```dockerfile
```

-	Layers:
	-	`sha256:c9b24924c6f572004d9933f2d27a0a279594cea367b25b993f6e9adc5338a6a3`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 5.2 MB (5236424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9ffcfef31d3564087854428f3f9bbd7bf021fc5ed241f9164419d84f66dc54`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.24`

**does not exist** (yet?)

## `neo4j:5.24-bullseye`

**does not exist** (yet?)

## `neo4j:5.24-community`

**does not exist** (yet?)

## `neo4j:5.24-community-bullseye`

**does not exist** (yet?)

## `neo4j:5.24-community-ubi9`

**does not exist** (yet?)

## `neo4j:5.24-enterprise`

**does not exist** (yet?)

## `neo4j:5.24-enterprise-bullseye`

**does not exist** (yet?)

## `neo4j:5.24-enterprise-ubi9`

**does not exist** (yet?)

## `neo4j:5.24-ubi9`

**does not exist** (yet?)

## `neo4j:5.24.1`

**does not exist** (yet?)

## `neo4j:5.24.1-bullseye`

**does not exist** (yet?)

## `neo4j:5.24.1-community`

**does not exist** (yet?)

## `neo4j:5.24.1-community-bullseye`

**does not exist** (yet?)

## `neo4j:5.24.1-community-ubi9`

**does not exist** (yet?)

## `neo4j:5.24.1-enterprise`

**does not exist** (yet?)

## `neo4j:5.24.1-enterprise-bullseye`

**does not exist** (yet?)

## `neo4j:5.24.1-enterprise-ubi9`

**does not exist** (yet?)

## `neo4j:5.24.1-ubi9`

**does not exist** (yet?)

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:1c7b2197f0fcb5d9ed6456804121667262b3cd0cee8f9e6889d17e265c0b3cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58665334ba82501643877e06327de5406c3f079706e84e6017556828a7774925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2c1adfcb59b9b5dd03aad4ef62fd50776902fa038c7e74b59b3f4546ac5b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d935cee01c732d4722d7a7727d92848dbd8229a2c30591c16c6c7b00418277`  
		Last Modified: Wed, 02 Oct 2024 02:59:22 GMT  
		Size: 145.2 MB (145166528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c34f444a07358def36a5ae4b90f14c15cacfa0b7e854ec13852b09b7cfd1b0f`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3a5a8ff936a268696d467125a422ea978319807026ef6bc5be10789ca063e`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ade805ded6479b4db6e8171c44d657b9861f25ca1e42a38d14a802c0b5aa5e`  
		Last Modified: Wed, 02 Oct 2024 02:59:23 GMT  
		Size: 127.3 MB (127275142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7b10c70da51727d23af98b1d0514c52cefbcba9deb68cf13db23d79db8e94c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9701f91d801823895f343ce9993fe2f066c8308b45153b437160ffc5c49e551`

```dockerfile
```

-	Layers:
	-	`sha256:7fe14d30fc4b595a17c2f57793ff8957f211b2b726bec7c13f11df81c8fc5af1`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b33e418c793b6cf45a23d2729151bc3646be6127891e651edd8307122b80f9c`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13dcb70f7bdfd061ee08230885ccbdf1ac446f5a0ddad0d5e7c16c9e93cf3cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91034df5644d0684bec8328c2780afa24c79fda52d6c8ff58f1e1a6fa4916d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac86c75abfa1438961120af68547a82316efc45175dd99bd0991973d91602`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da34dbbe75bd1251df5ec2c1e6b4c3b6c98c93335576651d7f951e7ee8d452a`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b326abc798852973a1c0c17d9e74846d6855ebd6e0e667779c7122cb6cfd7d6`  
		Last Modified: Wed, 02 Oct 2024 03:21:05 GMT  
		Size: 127.2 MB (127242634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a18ea06a4e2784097670ff7059fad93c4003c68e5b3a53889fa336faa86e792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868989d9a63f365a3bc5b3b2791179d136ec3a4af5dd9d514172dda858460177`

```dockerfile
```

-	Layers:
	-	`sha256:b1fbaa5abc0d38d06f7acf7533f911d82194a5c12f21a7df274521907cfd6193`  
		Last Modified: Wed, 02 Oct 2024 03:21:03 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424dfd47453071312aac8f8b67e972719901aad42db58e9aa532449d7178a5ae`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:1c7b2197f0fcb5d9ed6456804121667262b3cd0cee8f9e6889d17e265c0b3cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:58665334ba82501643877e06327de5406c3f079706e84e6017556828a7774925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2c1adfcb59b9b5dd03aad4ef62fd50776902fa038c7e74b59b3f4546ac5b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d935cee01c732d4722d7a7727d92848dbd8229a2c30591c16c6c7b00418277`  
		Last Modified: Wed, 02 Oct 2024 02:59:22 GMT  
		Size: 145.2 MB (145166528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c34f444a07358def36a5ae4b90f14c15cacfa0b7e854ec13852b09b7cfd1b0f`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3a5a8ff936a268696d467125a422ea978319807026ef6bc5be10789ca063e`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ade805ded6479b4db6e8171c44d657b9861f25ca1e42a38d14a802c0b5aa5e`  
		Last Modified: Wed, 02 Oct 2024 02:59:23 GMT  
		Size: 127.3 MB (127275142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:7b10c70da51727d23af98b1d0514c52cefbcba9deb68cf13db23d79db8e94c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9701f91d801823895f343ce9993fe2f066c8308b45153b437160ffc5c49e551`

```dockerfile
```

-	Layers:
	-	`sha256:7fe14d30fc4b595a17c2f57793ff8957f211b2b726bec7c13f11df81c8fc5af1`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b33e418c793b6cf45a23d2729151bc3646be6127891e651edd8307122b80f9c`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13dcb70f7bdfd061ee08230885ccbdf1ac446f5a0ddad0d5e7c16c9e93cf3cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91034df5644d0684bec8328c2780afa24c79fda52d6c8ff58f1e1a6fa4916d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac86c75abfa1438961120af68547a82316efc45175dd99bd0991973d91602`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da34dbbe75bd1251df5ec2c1e6b4c3b6c98c93335576651d7f951e7ee8d452a`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b326abc798852973a1c0c17d9e74846d6855ebd6e0e667779c7122cb6cfd7d6`  
		Last Modified: Wed, 02 Oct 2024 03:21:05 GMT  
		Size: 127.2 MB (127242634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a18ea06a4e2784097670ff7059fad93c4003c68e5b3a53889fa336faa86e792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868989d9a63f365a3bc5b3b2791179d136ec3a4af5dd9d514172dda858460177`

```dockerfile
```

-	Layers:
	-	`sha256:b1fbaa5abc0d38d06f7acf7533f911d82194a5c12f21a7df274521907cfd6193`  
		Last Modified: Wed, 02 Oct 2024 03:21:03 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424dfd47453071312aac8f8b67e972719901aad42db58e9aa532449d7178a5ae`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:1c7b2197f0fcb5d9ed6456804121667262b3cd0cee8f9e6889d17e265c0b3cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58665334ba82501643877e06327de5406c3f079706e84e6017556828a7774925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2c1adfcb59b9b5dd03aad4ef62fd50776902fa038c7e74b59b3f4546ac5b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d935cee01c732d4722d7a7727d92848dbd8229a2c30591c16c6c7b00418277`  
		Last Modified: Wed, 02 Oct 2024 02:59:22 GMT  
		Size: 145.2 MB (145166528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c34f444a07358def36a5ae4b90f14c15cacfa0b7e854ec13852b09b7cfd1b0f`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3a5a8ff936a268696d467125a422ea978319807026ef6bc5be10789ca063e`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ade805ded6479b4db6e8171c44d657b9861f25ca1e42a38d14a802c0b5aa5e`  
		Last Modified: Wed, 02 Oct 2024 02:59:23 GMT  
		Size: 127.3 MB (127275142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:7b10c70da51727d23af98b1d0514c52cefbcba9deb68cf13db23d79db8e94c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9701f91d801823895f343ce9993fe2f066c8308b45153b437160ffc5c49e551`

```dockerfile
```

-	Layers:
	-	`sha256:7fe14d30fc4b595a17c2f57793ff8957f211b2b726bec7c13f11df81c8fc5af1`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b33e418c793b6cf45a23d2729151bc3646be6127891e651edd8307122b80f9c`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13dcb70f7bdfd061ee08230885ccbdf1ac446f5a0ddad0d5e7c16c9e93cf3cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91034df5644d0684bec8328c2780afa24c79fda52d6c8ff58f1e1a6fa4916d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac86c75abfa1438961120af68547a82316efc45175dd99bd0991973d91602`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da34dbbe75bd1251df5ec2c1e6b4c3b6c98c93335576651d7f951e7ee8d452a`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b326abc798852973a1c0c17d9e74846d6855ebd6e0e667779c7122cb6cfd7d6`  
		Last Modified: Wed, 02 Oct 2024 03:21:05 GMT  
		Size: 127.2 MB (127242634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a18ea06a4e2784097670ff7059fad93c4003c68e5b3a53889fa336faa86e792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868989d9a63f365a3bc5b3b2791179d136ec3a4af5dd9d514172dda858460177`

```dockerfile
```

-	Layers:
	-	`sha256:b1fbaa5abc0d38d06f7acf7533f911d82194a5c12f21a7df274521907cfd6193`  
		Last Modified: Wed, 02 Oct 2024 03:21:03 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424dfd47453071312aac8f8b67e972719901aad42db58e9aa532449d7178a5ae`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:c77cd5d0d7930ecb4580f2ddb19e7423f6ba1435a3a3faa4165e5e05945f27b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0098560ed9a805f66cb221afeacc75786af6853dfde846f4803b8b414917059a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288881588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb77b9a32219305cb8b70b0595648e2303428f12a9d6cefe9159d2c63a8005f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d83d28c3ec134ab55df59638494812485d08170e15afd59ab5c97b1a7d8a8f`  
		Last Modified: Tue, 24 Sep 2024 01:00:40 GMT  
		Size: 125.4 MB (125421564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870f203580c59bfdcc2ffdb4f700745fda689be118fe7ada23459d8de3adf89a`  
		Last Modified: Tue, 24 Sep 2024 01:00:29 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744de09bc8f096be6c252b419afba26bddf9aa48c1c1f24cba1b0d390140afa`  
		Last Modified: Tue, 24 Sep 2024 01:00:31 GMT  
		Size: 124.3 MB (124348666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e981219ef42811e3a6c660fbff9e0ee2eb3c97bdbaff75ef6228f90c16b20f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71d74c4f7dbbf4aeff5c0f8efda90b46f16ef4d0a14d10d4626fcc9d485c4a`

```dockerfile
```

-	Layers:
	-	`sha256:6b4509003f57a092d99ec6d78a85374ec2f36f4e558a841f1c92c201bb6f72a9`  
		Last Modified: Tue, 24 Sep 2024 01:00:29 GMT  
		Size: 21.5 KB (21541 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b434eff505440dcc5f1300b7d9593b92bede39ddf5671c45957c149f377b284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287152268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100909fbb1b910412e47364cdd30cdc03111552e43af49fc93b1b95b20098a0c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3b708771449b1058f44f70932e1fa3868e1876107200b42fa17ab54d8ac089`  
		Last Modified: Tue, 24 Sep 2024 01:12:58 GMT  
		Size: 125.5 MB (125458540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d44a2f712becd634bcbe851a9ebdf018848d6c2e32bf8b2b0ba37b7c95cff`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46aa237c5a48019c4e9f67746ca7c30e2980798b04e4277c2d5ba80c70db7b9`  
		Last Modified: Tue, 24 Sep 2024 01:12:59 GMT  
		Size: 124.3 MB (124348656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:cf28fc857e6f49c6f7093163c5c3213d8c223c802a65431b92a7bd21ea95deb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd1ba6e0ec09093d45a1034696b3986742ef28383629290966b124d58efb73`

```dockerfile
```

-	Layers:
	-	`sha256:c9b24924c6f572004d9933f2d27a0a279594cea367b25b993f6e9adc5338a6a3`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 5.2 MB (5236424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9ffcfef31d3564087854428f3f9bbd7bf021fc5ed241f9164419d84f66dc54`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:20eb19e3d60f9f07c12c89eac8d8722e393be7e45c6d7e56004a2c493b8e2032
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:75474ba2e65bb99d3db5af62793bfa59d93e029a9b5af0228dc40199a3b356ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996d41a3868b10d956a98cc462c07d3fe1caec76400deba09068f5173b2415b7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1673cb44d5ff17b2b047fb5e1b3d90664aa7974f1c88ee4b3cff5899f1295b3`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 145.2 MB (145166509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00efd9813924815509302df1a98bae91516f68ead8ce6fdeb73ee82e876cba30`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a960959b94579c301984c7c79f7cadf4feb48f868f44aac2a518ce69e07f6e1d`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8218a43e0f72f5dd96cbf2a18155ba5720886c86bb783cf43e72769c05d109ce`  
		Last Modified: Wed, 02 Oct 2024 02:59:49 GMT  
		Size: 410.5 MB (410499185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3834913397e1d8b9723b0809332b285176f6b07e625f0b9bd17028bd56889160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748035d3340215f2d2adaa62767322130a30f6feb7df762d6e93bfb3b66fdcba`

```dockerfile
```

-	Layers:
	-	`sha256:2a919e97d07e444dc8ef297a50a01fa3064bc4ec20f82a4ec9653c3461937c2b`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07470de5ea31e0b89bb89e444b8be15011204b4028a3e591ca376a20da23e538`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 21.0 KB (21020 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d22431c9e6bf24550d5247206c30f3c18088e044468a114b8dbf9ddcc7e9d034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9160a03f2de508875f42891f871df91ee97f10b8c3e705150c404c144f417e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464555d7c1fa8910a4a9406e6e6c756235875214eb559a0c388509a758e36755`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38f14431d475169e0738488b259c4e8963782a82ae18614ae84b14e0f17c81`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b4b9f5e759fcc5fc268f3b21012594db25ab21e86224b7752c2406045a875f`  
		Last Modified: Wed, 02 Oct 2024 03:22:42 GMT  
		Size: 410.5 MB (410461075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:3647952a054bc223149f2e5b40f9bf80a938a9a587e4310e0da75418c4e5d467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88e2135a47cf6fa1018d51b183225fb15f44249a51d832d24dc436690ef4e72`

```dockerfile
```

-	Layers:
	-	`sha256:74a11e5c2cda1795b8b911af24b2e12c45f3afe1fd3eb47da4e8d1ec721d0ade`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da34dff3f2bc8e6954ef51fcacb54093fe632fee32601daffe0474e30a873f0a`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 21.2 KB (21201 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:20eb19e3d60f9f07c12c89eac8d8722e393be7e45c6d7e56004a2c493b8e2032
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:75474ba2e65bb99d3db5af62793bfa59d93e029a9b5af0228dc40199a3b356ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996d41a3868b10d956a98cc462c07d3fe1caec76400deba09068f5173b2415b7`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1673cb44d5ff17b2b047fb5e1b3d90664aa7974f1c88ee4b3cff5899f1295b3`  
		Last Modified: Wed, 02 Oct 2024 02:59:46 GMT  
		Size: 145.2 MB (145166509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00efd9813924815509302df1a98bae91516f68ead8ce6fdeb73ee82e876cba30`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a960959b94579c301984c7c79f7cadf4feb48f868f44aac2a518ce69e07f6e1d`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8218a43e0f72f5dd96cbf2a18155ba5720886c86bb783cf43e72769c05d109ce`  
		Last Modified: Wed, 02 Oct 2024 02:59:49 GMT  
		Size: 410.5 MB (410499185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3834913397e1d8b9723b0809332b285176f6b07e625f0b9bd17028bd56889160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748035d3340215f2d2adaa62767322130a30f6feb7df762d6e93bfb3b66fdcba`

```dockerfile
```

-	Layers:
	-	`sha256:2a919e97d07e444dc8ef297a50a01fa3064bc4ec20f82a4ec9653c3461937c2b`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07470de5ea31e0b89bb89e444b8be15011204b4028a3e591ca376a20da23e538`  
		Last Modified: Wed, 02 Oct 2024 02:59:43 GMT  
		Size: 21.0 KB (21020 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d22431c9e6bf24550d5247206c30f3c18088e044468a114b8dbf9ddcc7e9d034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9160a03f2de508875f42891f871df91ee97f10b8c3e705150c404c144f417e`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464555d7c1fa8910a4a9406e6e6c756235875214eb559a0c388509a758e36755`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 3.9 KB (3864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38f14431d475169e0738488b259c4e8963782a82ae18614ae84b14e0f17c81`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b4b9f5e759fcc5fc268f3b21012594db25ab21e86224b7752c2406045a875f`  
		Last Modified: Wed, 02 Oct 2024 03:22:42 GMT  
		Size: 410.5 MB (410461075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3647952a054bc223149f2e5b40f9bf80a938a9a587e4310e0da75418c4e5d467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88e2135a47cf6fa1018d51b183225fb15f44249a51d832d24dc436690ef4e72`

```dockerfile
```

-	Layers:
	-	`sha256:74a11e5c2cda1795b8b911af24b2e12c45f3afe1fd3eb47da4e8d1ec721d0ade`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da34dff3f2bc8e6954ef51fcacb54093fe632fee32601daffe0474e30a873f0a`  
		Last Modified: Wed, 02 Oct 2024 03:22:33 GMT  
		Size: 21.2 KB (21201 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f59e1c59f081b7ce91f88566f8eb7f6e68b5e7dab182c718cab3a0234c41e865
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:00de8405641c3906ac0870b927cf918c65ef95c891be0b93d9e931e8c7fac235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **572.1 MB (572100400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb15e28d84d25c2da9a5232ab5345e4674c667ee1ff4cc78fc5982d3c214ccc`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ddfd76485f79816a994af03e07f81ee0c26d4c555265dc88e431ebbb6fee20`  
		Last Modified: Tue, 24 Sep 2024 01:01:05 GMT  
		Size: 125.4 MB (125421178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b59dbfef883969f961184a0d8560874ebb1a97f145ea42a515f7c7b0eb7bdae`  
		Last Modified: Tue, 24 Sep 2024 01:01:01 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba43c06803d528425ab4076d700fa88099832f6ea43e74b6f3b4fe22310a70`  
		Last Modified: Tue, 24 Sep 2024 01:01:11 GMT  
		Size: 407.6 MB (407567866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:0888dc285bb2dc044a5f4afcf39f75536886fac737576e67540677413ed546d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833fe7cd0b2aab3c01ebee2c497ecaa3e0cc85a792cfa58b45b7b72904de2b57`

```dockerfile
```

-	Layers:
	-	`sha256:5bde44f1792bcfb4f97422ea6906284d9a2e0d72af82131ae16d8328f3192b0d`  
		Last Modified: Tue, 24 Sep 2024 01:01:01 GMT  
		Size: 20.4 KB (20363 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d81ca8cc0509d3aff0ea4a20d49d3846607a1a1ff1def2e51ec278541be84808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.4 MB (570371572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4ec1334d7ef63e23205a70a572f6d5a7d5b6e4b3bf29dd5ae13a4e2bbbdd34`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=9311d86cfe0ace3e5f1463dd92db13117d1aae54358113a291e2ca254faec3d9 NEO4J_TARBALL=neo4j-enterprise-5.23.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3b708771449b1058f44f70932e1fa3868e1876107200b42fa17ab54d8ac089`  
		Last Modified: Tue, 24 Sep 2024 01:12:58 GMT  
		Size: 125.5 MB (125458540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d44a2f712becd634bcbe851a9ebdf018848d6c2e32bf8b2b0ba37b7c95cff`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4345f5d20350eb93081102690fe65aa682534dab079fc921857e60ba42559243`  
		Last Modified: Tue, 24 Sep 2024 01:14:03 GMT  
		Size: 407.6 MB (407567960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:28cc26443537185525d9dfbc931bbe1f296050ce2225312a92a0c8e9c875ec48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9024a6d2dd8890aa63c2a6d9859d5ee22edd5309239caef9d338e4479a0a9420`

```dockerfile
```

-	Layers:
	-	`sha256:5cfbe26c48cfa6bd9510f45a86d9c17fd152e76fcd881f6e3e109cb2b9314a50`  
		Last Modified: Tue, 24 Sep 2024 01:13:55 GMT  
		Size: 5.5 MB (5517469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a16b7ec254cf43803685ccb33216dd7c8d65ebd34eb5ad4854819dc3e6210712`  
		Last Modified: Tue, 24 Sep 2024 01:13:54 GMT  
		Size: 20.9 KB (20890 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:1c7b2197f0fcb5d9ed6456804121667262b3cd0cee8f9e6889d17e265c0b3cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:58665334ba82501643877e06327de5406c3f079706e84e6017556828a7774925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c2c1adfcb59b9b5dd03aad4ef62fd50776902fa038c7e74b59b3f4546ac5b6`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d935cee01c732d4722d7a7727d92848dbd8229a2c30591c16c6c7b00418277`  
		Last Modified: Wed, 02 Oct 2024 02:59:22 GMT  
		Size: 145.2 MB (145166528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c34f444a07358def36a5ae4b90f14c15cacfa0b7e854ec13852b09b7cfd1b0f`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 3.8 KB (3848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3a5a8ff936a268696d467125a422ea978319807026ef6bc5be10789ca063e`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ade805ded6479b4db6e8171c44d657b9861f25ca1e42a38d14a802c0b5aa5e`  
		Last Modified: Wed, 02 Oct 2024 02:59:23 GMT  
		Size: 127.3 MB (127275142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:7b10c70da51727d23af98b1d0514c52cefbcba9deb68cf13db23d79db8e94c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9701f91d801823895f343ce9993fe2f066c8308b45153b437160ffc5c49e551`

```dockerfile
```

-	Layers:
	-	`sha256:7fe14d30fc4b595a17c2f57793ff8957f211b2b726bec7c13f11df81c8fc5af1`  
		Last Modified: Wed, 02 Oct 2024 02:59:20 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b33e418c793b6cf45a23d2729151bc3646be6127891e651edd8307122b80f9c`  
		Last Modified: Wed, 02 Oct 2024 02:59:19 GMT  
		Size: 23.4 KB (23389 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:13dcb70f7bdfd061ee08230885ccbdf1ac446f5a0ddad0d5e7c16c9e93cf3cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a91034df5644d0684bec8328c2780afa24c79fda52d6c8ff58f1e1a6fa4916d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 11:51:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && sed -i 's/Package Type:.*/Package Type: docker bullseye/' $NEO4J_HOME/packaging_info     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && chmod -R 755 "${NEO4J_HOME}/bin"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb27d49f52d849d785878ad27fb2291a6437cbd955a2286a8d0fd7688179644`  
		Last Modified: Wed, 02 Oct 2024 02:21:28 GMT  
		Size: 144.0 MB (143959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72ac86c75abfa1438961120af68547a82316efc45175dd99bd0991973d91602`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da34dbbe75bd1251df5ec2c1e6b4c3b6c98c93335576651d7f951e7ee8d452a`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b326abc798852973a1c0c17d9e74846d6855ebd6e0e667779c7122cb6cfd7d6`  
		Last Modified: Wed, 02 Oct 2024 03:21:05 GMT  
		Size: 127.2 MB (127242634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:0a18ea06a4e2784097670ff7059fad93c4003c68e5b3a53889fa336faa86e792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868989d9a63f365a3bc5b3b2791179d136ec3a4af5dd9d514172dda858460177`

```dockerfile
```

-	Layers:
	-	`sha256:b1fbaa5abc0d38d06f7acf7533f911d82194a5c12f21a7df274521907cfd6193`  
		Last Modified: Wed, 02 Oct 2024 03:21:03 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:424dfd47453071312aac8f8b67e972719901aad42db58e9aa532449d7178a5ae`  
		Last Modified: Wed, 02 Oct 2024 03:21:02 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:c77cd5d0d7930ecb4580f2ddb19e7423f6ba1435a3a3faa4165e5e05945f27b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:0098560ed9a805f66cb221afeacc75786af6853dfde846f4803b8b414917059a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288881588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb77b9a32219305cb8b70b0595648e2303428f12a9d6cefe9159d2c63a8005f`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:f7962bcea8426558f5511299e708fc6b7f7c85bd2c87cf668f4ad792bf3679df in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b61dc232d84be84b398c4a9d319ce263c1e698a1f3e41122b4989b26ae411742 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:3763314761ee75f4c50d08cca38184a1368ca6d78d98ed9b3df4d4a28ce9a60f in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:4d5d1cbd7ece41ce278c26338e01e2b82e1861b820ca052da9f3e0b16815358f`  
		Last Modified: Fri, 20 Sep 2024 03:47:53 GMT  
		Size: 39.1 MB (39101700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d83d28c3ec134ab55df59638494812485d08170e15afd59ab5c97b1a7d8a8f`  
		Last Modified: Tue, 24 Sep 2024 01:00:40 GMT  
		Size: 125.4 MB (125421564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870f203580c59bfdcc2ffdb4f700745fda689be118fe7ada23459d8de3adf89a`  
		Last Modified: Tue, 24 Sep 2024 01:00:29 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744de09bc8f096be6c252b419afba26bddf9aa48c1c1f24cba1b0d390140afa`  
		Last Modified: Tue, 24 Sep 2024 01:00:31 GMT  
		Size: 124.3 MB (124348666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4e981219ef42811e3a6c660fbff9e0ee2eb3c97bdbaff75ef6228f90c16b20f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 KB (21541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac71d74c4f7dbbf4aeff5c0f8efda90b46f16ef4d0a14d10d4626fcc9d485c4a`

```dockerfile
```

-	Layers:
	-	`sha256:6b4509003f57a092d99ec6d78a85374ec2f36f4e558a841f1c92c201bb6f72a9`  
		Last Modified: Tue, 24 Sep 2024 01:00:29 GMT  
		Size: 21.5 KB (21541 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b434eff505440dcc5f1300b7d9593b92bede39ddf5671c45957c149f377b284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287152268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100909fbb1b910412e47364cdd30cdc03111552e43af49fc93b1b95b20098a0c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:b8ad50f3d6859f84ef1f5a65e6525025d882089a4bfbfe1c1a6dcec413b08335 in / 
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:5b1f650e1376d79fa3a65df4a154ea5166def95154b52c1c1097dfd8fc7d58eb in /tmp/tls-ca-bundle.pem 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD multi:d851b7f6b461892ebd008971ee8858113becab621ea011cd6ca3834693892de0 in /etc/yum.repos.d/ 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.4"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 22 Aug 2024 11:51:04 GMT
ENV container oci
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["/bin/bash"]
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -rf /var/log/*
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:1b5dd590117e3105bf4bc7bf3d14e32e15284033314e5016a8b6a569d1309f13 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.4-1227.1726694542.json 
# Thu, 22 Aug 2024 11:51:04 GMT
ADD file:7d839fd792e21cdd37858c3a5300c195beb3df94eded547fbd1508ef81f3a0ce in /root/buildinfo/Dockerfile-ubi9-minimal-9.4-1227.1726694542 
# Thu, 22 Aug 2024 11:51:04 GMT
LABEL "release"="1227.1726694542" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-09-18T21:23:26" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="94baa7760359088a42ad33dc22d329a5ee2c7209" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.4-1227.1726694542"
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f '/etc/yum.repos.d/odcs-3496922-3d51b.repo' '/etc/yum.repos.d/rhel-9.4-compose-34ae9.repo'
# Thu, 22 Aug 2024 11:51:04 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 22 Aug 2024 11:51:04 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Thu, 22 Aug 2024 11:51:04 GMT
RUN set -eux;     arch="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${arch}" in         'x86_64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tini_sha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tini_url="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tini_sha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17-openjdk-headless         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tini_url} -O /usr/bin/tini;     wget -q ${tini_url}.asc -O tini.asc;     echo "${tini_sha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" /tini.asc /su-exec;     microdnf remove -y git* perl* make gcc glibc-headers glibc-devel libxcrypt-devel;     microdnf clean all # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV NEO4J_SHA256=ba71776c80ff5882524e6a535c942776249cffdcd0036baf9e1a1a257722285f NEO4J_TARBALL=neo4j-community-5.23.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j LANG=C.UTF-8
# Thu, 22 Aug 2024 11:51:04 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
# Thu, 22 Aug 2024 11:51:04 GMT
COPY ./local-package/* /startup/ # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.23.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     sed -i 's/Package Type:.*/Package Type: docker ubi9/' $NEO4J_HOME/packaging_info;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report;     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     chmod -R 755 "${NEO4J_HOME}/bin";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs # buildkit
# Thu, 22 Aug 2024 11:51:04 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 11:51:04 GMT
WORKDIR /var/lib/neo4j
# Thu, 22 Aug 2024 11:51:04 GMT
VOLUME [/data /logs]
# Thu, 22 Aug 2024 11:51:04 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Thu, 22 Aug 2024 11:51:04 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Thu, 22 Aug 2024 11:51:04 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:b7ea02e7115a7f896de4b38813636b60adf943ded0dc88824bbe396f76e618a0`  
		Last Modified: Fri, 20 Sep 2024 03:47:54 GMT  
		Size: 37.3 MB (37335414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3b708771449b1058f44f70932e1fa3868e1876107200b42fa17ab54d8ac089`  
		Last Modified: Tue, 24 Sep 2024 01:12:58 GMT  
		Size: 125.5 MB (125458540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01d44a2f712becd634bcbe851a9ebdf018848d6c2e32bf8b2b0ba37b7c95cff`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46aa237c5a48019c4e9f67746ca7c30e2980798b04e4277c2d5ba80c70db7b9`  
		Last Modified: Tue, 24 Sep 2024 01:12:59 GMT  
		Size: 124.3 MB (124348656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:cf28fc857e6f49c6f7093163c5c3213d8c223c802a65431b92a7bd21ea95deb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bd1ba6e0ec09093d45a1034696b3986742ef28383629290966b124d58efb73`

```dockerfile
```

-	Layers:
	-	`sha256:c9b24924c6f572004d9933f2d27a0a279594cea367b25b993f6e9adc5338a6a3`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 5.2 MB (5236424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9ffcfef31d3564087854428f3f9bbd7bf021fc5ed241f9164419d84f66dc54`  
		Last Modified: Tue, 24 Sep 2024 01:12:56 GMT  
		Size: 22.1 KB (22116 bytes)  
		MIME: application/vnd.in-toto+json
