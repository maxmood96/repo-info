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
-	[`neo4j:5.23`](#neo4j523)
-	[`neo4j:5.23-bullseye`](#neo4j523-bullseye)
-	[`neo4j:5.23-community`](#neo4j523-community)
-	[`neo4j:5.23-community-bullseye`](#neo4j523-community-bullseye)
-	[`neo4j:5.23-community-ubi9`](#neo4j523-community-ubi9)
-	[`neo4j:5.23-enterprise`](#neo4j523-enterprise)
-	[`neo4j:5.23-enterprise-bullseye`](#neo4j523-enterprise-bullseye)
-	[`neo4j:5.23-enterprise-ubi9`](#neo4j523-enterprise-ubi9)
-	[`neo4j:5.23-ubi9`](#neo4j523-ubi9)
-	[`neo4j:5.23.0`](#neo4j5230)
-	[`neo4j:5.23.0-bullseye`](#neo4j5230-bullseye)
-	[`neo4j:5.23.0-community`](#neo4j5230-community)
-	[`neo4j:5.23.0-community-bullseye`](#neo4j5230-community-bullseye)
-	[`neo4j:5.23.0-community-ubi9`](#neo4j5230-community-ubi9)
-	[`neo4j:5.23.0-enterprise`](#neo4j5230-enterprise)
-	[`neo4j:5.23.0-enterprise-bullseye`](#neo4j5230-enterprise-bullseye)
-	[`neo4j:5.23.0-enterprise-ubi9`](#neo4j5230-enterprise-ubi9)
-	[`neo4j:5.23.0-ubi9`](#neo4j5230-ubi9)
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
$ docker pull neo4j@sha256:f142e06c307835acd829d7dbe65a1be7cf15a91b33f535c21ac56bdbe901def6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:241711d42d6fdc4badd0966f0f375407f1fd62961b94ba37f4ac21f235a8d86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303072916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768777fe20ae2a4da5d60f5972f35613ffec2beb63b35de64b9ce4456e4a4609`
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
	-	`sha256:b3a93066566b4c6a6504b05e3ec0da5bc1c8a3674ff11b4be03ada21cfdf2346`  
		Last Modified: Fri, 27 Sep 2024 06:02:39 GMT  
		Size: 145.6 MB (145550043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17011573b77377e986b4b80bd5585722bb5546664aba0f54306c46e78c0f2754`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aceec55dfce1db5652c02f466083085c5278b5b5a9858b3bdef28724e29a62`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef2ee01639496ce3308ed2e761b20d53252a8055237373ec97349a5e9eb7765`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 126.1 MB (126080885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:a102eab7d3dc5591998ce67c6cf7118d477b1bdf45a6926fb9c715fb9dacba9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fef344886677a3869aa62ae52f8163fdce627c7e2940c8ca5afc5a526ce7292`

```dockerfile
```

-	Layers:
	-	`sha256:e778b4f7ba38ab16d939c1dd7f07b76c9ee44e13e5e0d35efd1c4c2e0d47717d`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58efcf091d22785a805469f1e749954b43b737d1670994e2d46fd87958008dc`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 19.6 KB (19591 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:152990af3eb41e45f8474b491a33de12d4c45568f833fdc7588348395d8c0be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298487722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b200a246fd120aabbaa8b497f4ce77e2fde2630bdbc373c99f66dda675b319`
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
	-	`sha256:f9ca088f405538d234c7d9cbac7f408847c3d31d8b3ae7208157c2f1abbf2e30`  
		Last Modified: Fri, 27 Sep 2024 10:27:10 GMT  
		Size: 142.4 MB (142354816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e449d04dae62cf513540948f8a62fcf8d992d5fb5d68bd0178a9b5036ad746fb`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab25ace0b2c001ae6778b9020506f019ed87a50583eb6679fccd8b734e4fd6`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede361f920bcc62deb16bc4848eda04e49215e599e8d07e2dce05b47d360071e`  
		Last Modified: Fri, 27 Sep 2024 15:24:25 GMT  
		Size: 126.0 MB (126044327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:ac10f881ed8bffe352a2f66d96b2b5eb290be934b96bad8066c99027474be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaed74ca7e791bcb8c230529e3a090daa68dbd4efe1a94f3bc3c8413214a9b27`

```dockerfile
```

-	Layers:
	-	`sha256:c2bab5d5f39631b459a1aeb289664b47acb3b446769bd3d597acb129c40bd7cc`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537d9fc0ffaa45f609403feb18e0ddd0987569edaba6f8e8aae5440dd6cdc0e2`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 20.1 KB (20143 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:f142e06c307835acd829d7dbe65a1be7cf15a91b33f535c21ac56bdbe901def6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:241711d42d6fdc4badd0966f0f375407f1fd62961b94ba37f4ac21f235a8d86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303072916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768777fe20ae2a4da5d60f5972f35613ffec2beb63b35de64b9ce4456e4a4609`
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
	-	`sha256:b3a93066566b4c6a6504b05e3ec0da5bc1c8a3674ff11b4be03ada21cfdf2346`  
		Last Modified: Fri, 27 Sep 2024 06:02:39 GMT  
		Size: 145.6 MB (145550043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17011573b77377e986b4b80bd5585722bb5546664aba0f54306c46e78c0f2754`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aceec55dfce1db5652c02f466083085c5278b5b5a9858b3bdef28724e29a62`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef2ee01639496ce3308ed2e761b20d53252a8055237373ec97349a5e9eb7765`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 126.1 MB (126080885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a102eab7d3dc5591998ce67c6cf7118d477b1bdf45a6926fb9c715fb9dacba9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fef344886677a3869aa62ae52f8163fdce627c7e2940c8ca5afc5a526ce7292`

```dockerfile
```

-	Layers:
	-	`sha256:e778b4f7ba38ab16d939c1dd7f07b76c9ee44e13e5e0d35efd1c4c2e0d47717d`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58efcf091d22785a805469f1e749954b43b737d1670994e2d46fd87958008dc`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 19.6 KB (19591 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:152990af3eb41e45f8474b491a33de12d4c45568f833fdc7588348395d8c0be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298487722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b200a246fd120aabbaa8b497f4ce77e2fde2630bdbc373c99f66dda675b319`
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
	-	`sha256:f9ca088f405538d234c7d9cbac7f408847c3d31d8b3ae7208157c2f1abbf2e30`  
		Last Modified: Fri, 27 Sep 2024 10:27:10 GMT  
		Size: 142.4 MB (142354816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e449d04dae62cf513540948f8a62fcf8d992d5fb5d68bd0178a9b5036ad746fb`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab25ace0b2c001ae6778b9020506f019ed87a50583eb6679fccd8b734e4fd6`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede361f920bcc62deb16bc4848eda04e49215e599e8d07e2dce05b47d360071e`  
		Last Modified: Fri, 27 Sep 2024 15:24:25 GMT  
		Size: 126.0 MB (126044327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:ac10f881ed8bffe352a2f66d96b2b5eb290be934b96bad8066c99027474be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaed74ca7e791bcb8c230529e3a090daa68dbd4efe1a94f3bc3c8413214a9b27`

```dockerfile
```

-	Layers:
	-	`sha256:c2bab5d5f39631b459a1aeb289664b47acb3b446769bd3d597acb129c40bd7cc`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537d9fc0ffaa45f609403feb18e0ddd0987569edaba6f8e8aae5440dd6cdc0e2`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 20.1 KB (20143 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:da9e8510ad470e5ee265d7e05ccaf6f5f816f68d9ea9614ee010a777cb001dde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c3ebb6aea21124f821800e873192bac3d19d7a3bb39190d0bc2fd1b9933f7703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407242376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649e76e89fa6450e7000eee7f8ca86496ead4ab7ee1b5241a7cf302c5cb52668`
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
	-	`sha256:267963e9f553f61adc49fe96dfc8d58c9e61d838d6cbc758cc71760d3a19afef`  
		Last Modified: Fri, 27 Sep 2024 06:02:51 GMT  
		Size: 145.6 MB (145550044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fa716f2bdbb9b24b5384c635febd38ceedd082c0b3e422d8a58f1de4d3e746`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9c1a06cf08bd91a16535fc2c5a262a6f783ef3bb3d3a359019540c8472584f`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaac97a106c0a02ae3677bac3c7e1a9c99a01f39679ac9cf466babfd761be9b`  
		Last Modified: Fri, 27 Sep 2024 06:02:57 GMT  
		Size: 230.3 MB (230250340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:1dc579e251d43d4b13cfae45e98ffdcfabed79a0ebdd1588ef4b77b69c22249e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da957e64347ade8b2f7bc00a07c81c2c447d1a398d3ddb573aa613a329012868`

```dockerfile
```

-	Layers:
	-	`sha256:103f16aa960151921452c225d806255802244fe2b814f0d7e0fbea1d2544b78e`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 3.3 MB (3302201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad2d53a79fb5d3b8282e08acbf728adae45d0a8f5b4e537e4ff1a82c096a987`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d4a6efebf1aa4037f315ea82b5d1850d4aa1c26364a074cfe3ba43308d02496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402658277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefdde75676782585d47b013c5715aa34156f9fcdfd5cd4d6df6fddeb7ff5602`
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
	-	`sha256:f9ca088f405538d234c7d9cbac7f408847c3d31d8b3ae7208157c2f1abbf2e30`  
		Last Modified: Fri, 27 Sep 2024 10:27:10 GMT  
		Size: 142.4 MB (142354816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac9b515d99c59489c0a491fb3482568604a2d17054b2c4649411c59ab90b13c`  
		Last Modified: Fri, 27 Sep 2024 15:26:42 GMT  
		Size: 3.9 KB (3876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd48d44ddf1ed480d0013d7e2f4d47ce399b3d693e8195e6ff69d54075d3637c`  
		Last Modified: Fri, 27 Sep 2024 15:26:42 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb179e973508d978bd641cff7e84ea295652a1b0c6550f52c11967ccdaaad46d`  
		Last Modified: Fri, 27 Sep 2024 15:26:47 GMT  
		Size: 230.2 MB (230214874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:dbd80c5f97beb0641f3197a5f86d1cd92e41778fbf6a76e1cf624132d11b4dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a86e05a5591e5f118a49ac9d592be509fa91a792fd209ab4692e22db32d7810`

```dockerfile
```

-	Layers:
	-	`sha256:503b22ed5bf001a2cfdcab2476bf2a7a98881c5a98671a8cc95fc1663616e091`  
		Last Modified: Fri, 27 Sep 2024 15:26:42 GMT  
		Size: 3.3 MB (3302440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbd5173b45cbe97a2f49c8a579c85364df4e4169c3c7d250652251a6fdf4682`  
		Last Modified: Fri, 27 Sep 2024 15:26:42 GMT  
		Size: 19.6 KB (19551 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.37`

```console
$ docker pull neo4j@sha256:f142e06c307835acd829d7dbe65a1be7cf15a91b33f535c21ac56bdbe901def6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.37` - linux; amd64

```console
$ docker pull neo4j@sha256:241711d42d6fdc4badd0966f0f375407f1fd62961b94ba37f4ac21f235a8d86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303072916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768777fe20ae2a4da5d60f5972f35613ffec2beb63b35de64b9ce4456e4a4609`
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
	-	`sha256:b3a93066566b4c6a6504b05e3ec0da5bc1c8a3674ff11b4be03ada21cfdf2346`  
		Last Modified: Fri, 27 Sep 2024 06:02:39 GMT  
		Size: 145.6 MB (145550043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17011573b77377e986b4b80bd5585722bb5546664aba0f54306c46e78c0f2754`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aceec55dfce1db5652c02f466083085c5278b5b5a9858b3bdef28724e29a62`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef2ee01639496ce3308ed2e761b20d53252a8055237373ec97349a5e9eb7765`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 126.1 MB (126080885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37` - unknown; unknown

```console
$ docker pull neo4j@sha256:a102eab7d3dc5591998ce67c6cf7118d477b1bdf45a6926fb9c715fb9dacba9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fef344886677a3869aa62ae52f8163fdce627c7e2940c8ca5afc5a526ce7292`

```dockerfile
```

-	Layers:
	-	`sha256:e778b4f7ba38ab16d939c1dd7f07b76c9ee44e13e5e0d35efd1c4c2e0d47717d`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58efcf091d22785a805469f1e749954b43b737d1670994e2d46fd87958008dc`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 19.6 KB (19591 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.37` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:152990af3eb41e45f8474b491a33de12d4c45568f833fdc7588348395d8c0be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298487722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b200a246fd120aabbaa8b497f4ce77e2fde2630bdbc373c99f66dda675b319`
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
	-	`sha256:f9ca088f405538d234c7d9cbac7f408847c3d31d8b3ae7208157c2f1abbf2e30`  
		Last Modified: Fri, 27 Sep 2024 10:27:10 GMT  
		Size: 142.4 MB (142354816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e449d04dae62cf513540948f8a62fcf8d992d5fb5d68bd0178a9b5036ad746fb`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab25ace0b2c001ae6778b9020506f019ed87a50583eb6679fccd8b734e4fd6`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede361f920bcc62deb16bc4848eda04e49215e599e8d07e2dce05b47d360071e`  
		Last Modified: Fri, 27 Sep 2024 15:24:25 GMT  
		Size: 126.0 MB (126044327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37` - unknown; unknown

```console
$ docker pull neo4j@sha256:ac10f881ed8bffe352a2f66d96b2b5eb290be934b96bad8066c99027474be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaed74ca7e791bcb8c230529e3a090daa68dbd4efe1a94f3bc3c8413214a9b27`

```dockerfile
```

-	Layers:
	-	`sha256:c2bab5d5f39631b459a1aeb289664b47acb3b446769bd3d597acb129c40bd7cc`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537d9fc0ffaa45f609403feb18e0ddd0987569edaba6f8e8aae5440dd6cdc0e2`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 20.1 KB (20143 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.37-community`

```console
$ docker pull neo4j@sha256:f142e06c307835acd829d7dbe65a1be7cf15a91b33f535c21ac56bdbe901def6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.37-community` - linux; amd64

```console
$ docker pull neo4j@sha256:241711d42d6fdc4badd0966f0f375407f1fd62961b94ba37f4ac21f235a8d86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303072916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768777fe20ae2a4da5d60f5972f35613ffec2beb63b35de64b9ce4456e4a4609`
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
	-	`sha256:b3a93066566b4c6a6504b05e3ec0da5bc1c8a3674ff11b4be03ada21cfdf2346`  
		Last Modified: Fri, 27 Sep 2024 06:02:39 GMT  
		Size: 145.6 MB (145550043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17011573b77377e986b4b80bd5585722bb5546664aba0f54306c46e78c0f2754`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aceec55dfce1db5652c02f466083085c5278b5b5a9858b3bdef28724e29a62`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef2ee01639496ce3308ed2e761b20d53252a8055237373ec97349a5e9eb7765`  
		Last Modified: Fri, 27 Sep 2024 06:02:44 GMT  
		Size: 126.1 MB (126080885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:a102eab7d3dc5591998ce67c6cf7118d477b1bdf45a6926fb9c715fb9dacba9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3182529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fef344886677a3869aa62ae52f8163fdce627c7e2940c8ca5afc5a526ce7292`

```dockerfile
```

-	Layers:
	-	`sha256:e778b4f7ba38ab16d939c1dd7f07b76c9ee44e13e5e0d35efd1c4c2e0d47717d`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 3.2 MB (3162938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c58efcf091d22785a805469f1e749954b43b737d1670994e2d46fd87958008dc`  
		Last Modified: Fri, 27 Sep 2024 06:02:35 GMT  
		Size: 19.6 KB (19591 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.37-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:152990af3eb41e45f8474b491a33de12d4c45568f833fdc7588348395d8c0be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298487722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b200a246fd120aabbaa8b497f4ce77e2fde2630bdbc373c99f66dda675b319`
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
	-	`sha256:f9ca088f405538d234c7d9cbac7f408847c3d31d8b3ae7208157c2f1abbf2e30`  
		Last Modified: Fri, 27 Sep 2024 10:27:10 GMT  
		Size: 142.4 MB (142354816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e449d04dae62cf513540948f8a62fcf8d992d5fb5d68bd0178a9b5036ad746fb`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab25ace0b2c001ae6778b9020506f019ed87a50583eb6679fccd8b734e4fd6`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede361f920bcc62deb16bc4848eda04e49215e599e8d07e2dce05b47d360071e`  
		Last Modified: Fri, 27 Sep 2024 15:24:25 GMT  
		Size: 126.0 MB (126044327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:ac10f881ed8bffe352a2f66d96b2b5eb290be934b96bad8066c99027474be1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3183344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaed74ca7e791bcb8c230529e3a090daa68dbd4efe1a94f3bc3c8413214a9b27`

```dockerfile
```

-	Layers:
	-	`sha256:c2bab5d5f39631b459a1aeb289664b47acb3b446769bd3d597acb129c40bd7cc`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 3.2 MB (3163201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537d9fc0ffaa45f609403feb18e0ddd0987569edaba6f8e8aae5440dd6cdc0e2`  
		Last Modified: Fri, 27 Sep 2024 15:24:21 GMT  
		Size: 20.1 KB (20143 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.37-enterprise`

```console
$ docker pull neo4j@sha256:da9e8510ad470e5ee265d7e05ccaf6f5f816f68d9ea9614ee010a777cb001dde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.37-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:c3ebb6aea21124f821800e873192bac3d19d7a3bb39190d0bc2fd1b9933f7703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407242376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649e76e89fa6450e7000eee7f8ca86496ead4ab7ee1b5241a7cf302c5cb52668`
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
	-	`sha256:267963e9f553f61adc49fe96dfc8d58c9e61d838d6cbc758cc71760d3a19afef`  
		Last Modified: Fri, 27 Sep 2024 06:02:51 GMT  
		Size: 145.6 MB (145550044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fa716f2bdbb9b24b5384c635febd38ceedd082c0b3e422d8a58f1de4d3e746`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9c1a06cf08bd91a16535fc2c5a262a6f783ef3bb3d3a359019540c8472584f`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaac97a106c0a02ae3677bac3c7e1a9c99a01f39679ac9cf466babfd761be9b`  
		Last Modified: Fri, 27 Sep 2024 06:02:57 GMT  
		Size: 230.3 MB (230250340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:1dc579e251d43d4b13cfae45e98ffdcfabed79a0ebdd1588ef4b77b69c22249e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da957e64347ade8b2f7bc00a07c81c2c447d1a398d3ddb573aa613a329012868`

```dockerfile
```

-	Layers:
	-	`sha256:103f16aa960151921452c225d806255802244fe2b814f0d7e0fbea1d2544b78e`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 3.3 MB (3302201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad2d53a79fb5d3b8282e08acbf728adae45d0a8f5b4e537e4ff1a82c096a987`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 19.0 KB (19020 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4.37-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d4a6efebf1aa4037f315ea82b5d1850d4aa1c26364a074cfe3ba43308d02496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402658277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefdde75676782585d47b013c5715aa34156f9fcdfd5cd4d6df6fddeb7ff5602`
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
	-	`sha256:f9ca088f405538d234c7d9cbac7f408847c3d31d8b3ae7208157c2f1abbf2e30`  
		Last Modified: Fri, 27 Sep 2024 10:27:10 GMT  
		Size: 142.4 MB (142354816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac9b515d99c59489c0a491fb3482568604a2d17054b2c4649411c59ab90b13c`  
		Last Modified: Fri, 27 Sep 2024 15:26:42 GMT  
		Size: 3.9 KB (3876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd48d44ddf1ed480d0013d7e2f4d47ce399b3d693e8195e6ff69d54075d3637c`  
		Last Modified: Fri, 27 Sep 2024 15:26:42 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb179e973508d978bd641cff7e84ea295652a1b0c6550f52c11967ccdaaad46d`  
		Last Modified: Fri, 27 Sep 2024 15:26:47 GMT  
		Size: 230.2 MB (230214874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4.37-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:dbd80c5f97beb0641f3197a5f86d1cd92e41778fbf6a76e1cf624132d11b4dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3321991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a86e05a5591e5f118a49ac9d592be509fa91a792fd209ab4692e22db32d7810`

```dockerfile
```

-	Layers:
	-	`sha256:503b22ed5bf001a2cfdcab2476bf2a7a98881c5a98671a8cc95fc1663616e091`  
		Last Modified: Fri, 27 Sep 2024 15:26:42 GMT  
		Size: 3.3 MB (3302440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbd5173b45cbe97a2f49c8a579c85364df4e4169c3c7d250652251a6fdf4682`  
		Last Modified: Fri, 27 Sep 2024 15:26:42 GMT  
		Size: 19.6 KB (19551 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
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
$ docker pull neo4j@sha256:1e4798f5ad5581aee1a9e1407cb91a6b4c72b2c985e9e793019ab952834b9c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b5f91ecd702916f4cd7ae68a473600891a8a617bc1360bfb9cd57357e7b54fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9f0a0977ccf4f0a2ddcb5aa58692e46c3b3240266b94f540562b8ec7c71cec`
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
	-	`sha256:84e4e6b77bd9385a9a6f9a642144dd54ed07d54a4696a0521bf4efa25af637cd`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d433d9752e230bad32526fda01c334afb12cf495644179797e3c264ce20c8e8`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bacec138231cd594efc40dcad0ff5080d2d1f77c561adfa7cee6a7d3fcdb96`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74bf75996dbe9037f327f6cb03c56d4e1d43bfe4bee81cac29f6f3088cbb19`  
		Last Modified: Fri, 27 Sep 2024 06:02:49 GMT  
		Size: 410.5 MB (410499150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0518d1f857e5be99a53d90a68c728fe64c5193f4f258a7e59a720f4bf2e1b0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa92b3f1b3106604eb0bb28adeffc97ec804078cf92d11c233bd7a71ab616d04`

```dockerfile
```

-	Layers:
	-	`sha256:3296896f2d33b7629c04227fac0b219d69ff6fdba423372f4d3ff37fb1f280ad`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b29c140ca030e493c6020079aba224449dabfa9c0470c0cdc7470c84ea3178`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:69b51038d44f0f0342647a31ee5c8c0070367a1db0a179173b5432cacacbd13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a1d373b70fa75a2d37d76175581ad7f34c3717d3d5d2ec1fea8d194484245`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba146b90e0a392c265f63b58cc86ddc8ee46d5bba6a044c07f05122acab38bd7`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45695b8a9267c8834a7862ca600d7d1e0d1093777a99cfaebe459ec8aa695b67`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5f12ba6c5018de35ec6920a8ad06130ffbb1c10cd54856831d7d8701ad425`  
		Last Modified: Fri, 27 Sep 2024 15:23:22 GMT  
		Size: 410.5 MB (410461015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:040dba030ce3b6e7f8c96afc16763dd8f6b991eab9f79d488507a349ceb32ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e14288d8309236aa027c7febc1f3762ef7403c92e8a20f41424083bdea1ff1`

```dockerfile
```

-	Layers:
	-	`sha256:f3b99aeddd8d5ff4eb01e8646a356b1be27fa76dd7c635eb3ebf0048960faa4e`  
		Last Modified: Fri, 27 Sep 2024 15:23:13 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0053c396c032ad4a973385688ded9e778b8569ba381879a94b34f76bb1ea2b4`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:1e4798f5ad5581aee1a9e1407cb91a6b4c72b2c985e9e793019ab952834b9c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b5f91ecd702916f4cd7ae68a473600891a8a617bc1360bfb9cd57357e7b54fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9f0a0977ccf4f0a2ddcb5aa58692e46c3b3240266b94f540562b8ec7c71cec`
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
	-	`sha256:84e4e6b77bd9385a9a6f9a642144dd54ed07d54a4696a0521bf4efa25af637cd`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d433d9752e230bad32526fda01c334afb12cf495644179797e3c264ce20c8e8`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bacec138231cd594efc40dcad0ff5080d2d1f77c561adfa7cee6a7d3fcdb96`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74bf75996dbe9037f327f6cb03c56d4e1d43bfe4bee81cac29f6f3088cbb19`  
		Last Modified: Fri, 27 Sep 2024 06:02:49 GMT  
		Size: 410.5 MB (410499150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0518d1f857e5be99a53d90a68c728fe64c5193f4f258a7e59a720f4bf2e1b0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa92b3f1b3106604eb0bb28adeffc97ec804078cf92d11c233bd7a71ab616d04`

```dockerfile
```

-	Layers:
	-	`sha256:3296896f2d33b7629c04227fac0b219d69ff6fdba423372f4d3ff37fb1f280ad`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b29c140ca030e493c6020079aba224449dabfa9c0470c0cdc7470c84ea3178`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:69b51038d44f0f0342647a31ee5c8c0070367a1db0a179173b5432cacacbd13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a1d373b70fa75a2d37d76175581ad7f34c3717d3d5d2ec1fea8d194484245`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba146b90e0a392c265f63b58cc86ddc8ee46d5bba6a044c07f05122acab38bd7`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45695b8a9267c8834a7862ca600d7d1e0d1093777a99cfaebe459ec8aa695b67`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5f12ba6c5018de35ec6920a8ad06130ffbb1c10cd54856831d7d8701ad425`  
		Last Modified: Fri, 27 Sep 2024 15:23:22 GMT  
		Size: 410.5 MB (410461015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:040dba030ce3b6e7f8c96afc16763dd8f6b991eab9f79d488507a349ceb32ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e14288d8309236aa027c7febc1f3762ef7403c92e8a20f41424083bdea1ff1`

```dockerfile
```

-	Layers:
	-	`sha256:f3b99aeddd8d5ff4eb01e8646a356b1be27fa76dd7c635eb3ebf0048960faa4e`  
		Last Modified: Fri, 27 Sep 2024 15:23:13 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0053c396c032ad4a973385688ded9e778b8569ba381879a94b34f76bb1ea2b4`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 21.6 KB (21616 bytes)  
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

## `neo4j:5.23`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-bullseye`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-community`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-community` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-community-bullseye`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-community-ubi9`

```console
$ docker pull neo4j@sha256:c77cd5d0d7930ecb4580f2ddb19e7423f6ba1435a3a3faa4165e5e05945f27b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-community-ubi9` - linux; amd64

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

### `neo4j:5.23-community-ubi9` - unknown; unknown

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

### `neo4j:5.23-community-ubi9` - linux; arm64 variant v8

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

### `neo4j:5.23-community-ubi9` - unknown; unknown

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

## `neo4j:5.23-enterprise`

```console
$ docker pull neo4j@sha256:1e4798f5ad5581aee1a9e1407cb91a6b4c72b2c985e9e793019ab952834b9c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b5f91ecd702916f4cd7ae68a473600891a8a617bc1360bfb9cd57357e7b54fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9f0a0977ccf4f0a2ddcb5aa58692e46c3b3240266b94f540562b8ec7c71cec`
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
	-	`sha256:84e4e6b77bd9385a9a6f9a642144dd54ed07d54a4696a0521bf4efa25af637cd`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d433d9752e230bad32526fda01c334afb12cf495644179797e3c264ce20c8e8`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bacec138231cd594efc40dcad0ff5080d2d1f77c561adfa7cee6a7d3fcdb96`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74bf75996dbe9037f327f6cb03c56d4e1d43bfe4bee81cac29f6f3088cbb19`  
		Last Modified: Fri, 27 Sep 2024 06:02:49 GMT  
		Size: 410.5 MB (410499150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0518d1f857e5be99a53d90a68c728fe64c5193f4f258a7e59a720f4bf2e1b0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa92b3f1b3106604eb0bb28adeffc97ec804078cf92d11c233bd7a71ab616d04`

```dockerfile
```

-	Layers:
	-	`sha256:3296896f2d33b7629c04227fac0b219d69ff6fdba423372f4d3ff37fb1f280ad`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b29c140ca030e493c6020079aba224449dabfa9c0470c0cdc7470c84ea3178`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:69b51038d44f0f0342647a31ee5c8c0070367a1db0a179173b5432cacacbd13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a1d373b70fa75a2d37d76175581ad7f34c3717d3d5d2ec1fea8d194484245`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba146b90e0a392c265f63b58cc86ddc8ee46d5bba6a044c07f05122acab38bd7`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45695b8a9267c8834a7862ca600d7d1e0d1093777a99cfaebe459ec8aa695b67`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5f12ba6c5018de35ec6920a8ad06130ffbb1c10cd54856831d7d8701ad425`  
		Last Modified: Fri, 27 Sep 2024 15:23:22 GMT  
		Size: 410.5 MB (410461015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:040dba030ce3b6e7f8c96afc16763dd8f6b991eab9f79d488507a349ceb32ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e14288d8309236aa027c7febc1f3762ef7403c92e8a20f41424083bdea1ff1`

```dockerfile
```

-	Layers:
	-	`sha256:f3b99aeddd8d5ff4eb01e8646a356b1be27fa76dd7c635eb3ebf0048960faa4e`  
		Last Modified: Fri, 27 Sep 2024 15:23:13 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0053c396c032ad4a973385688ded9e778b8569ba381879a94b34f76bb1ea2b4`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:1e4798f5ad5581aee1a9e1407cb91a6b4c72b2c985e9e793019ab952834b9c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b5f91ecd702916f4cd7ae68a473600891a8a617bc1360bfb9cd57357e7b54fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9f0a0977ccf4f0a2ddcb5aa58692e46c3b3240266b94f540562b8ec7c71cec`
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
	-	`sha256:84e4e6b77bd9385a9a6f9a642144dd54ed07d54a4696a0521bf4efa25af637cd`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d433d9752e230bad32526fda01c334afb12cf495644179797e3c264ce20c8e8`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bacec138231cd594efc40dcad0ff5080d2d1f77c561adfa7cee6a7d3fcdb96`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74bf75996dbe9037f327f6cb03c56d4e1d43bfe4bee81cac29f6f3088cbb19`  
		Last Modified: Fri, 27 Sep 2024 06:02:49 GMT  
		Size: 410.5 MB (410499150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0518d1f857e5be99a53d90a68c728fe64c5193f4f258a7e59a720f4bf2e1b0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa92b3f1b3106604eb0bb28adeffc97ec804078cf92d11c233bd7a71ab616d04`

```dockerfile
```

-	Layers:
	-	`sha256:3296896f2d33b7629c04227fac0b219d69ff6fdba423372f4d3ff37fb1f280ad`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b29c140ca030e493c6020079aba224449dabfa9c0470c0cdc7470c84ea3178`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:69b51038d44f0f0342647a31ee5c8c0070367a1db0a179173b5432cacacbd13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a1d373b70fa75a2d37d76175581ad7f34c3717d3d5d2ec1fea8d194484245`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba146b90e0a392c265f63b58cc86ddc8ee46d5bba6a044c07f05122acab38bd7`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45695b8a9267c8834a7862ca600d7d1e0d1093777a99cfaebe459ec8aa695b67`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5f12ba6c5018de35ec6920a8ad06130ffbb1c10cd54856831d7d8701ad425`  
		Last Modified: Fri, 27 Sep 2024 15:23:22 GMT  
		Size: 410.5 MB (410461015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:040dba030ce3b6e7f8c96afc16763dd8f6b991eab9f79d488507a349ceb32ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e14288d8309236aa027c7febc1f3762ef7403c92e8a20f41424083bdea1ff1`

```dockerfile
```

-	Layers:
	-	`sha256:f3b99aeddd8d5ff4eb01e8646a356b1be27fa76dd7c635eb3ebf0048960faa4e`  
		Last Modified: Fri, 27 Sep 2024 15:23:13 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0053c396c032ad4a973385688ded9e778b8569ba381879a94b34f76bb1ea2b4`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f59e1c59f081b7ce91f88566f8eb7f6e68b5e7dab182c718cab3a0234c41e865
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-enterprise-ubi9` - linux; amd64

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

### `neo4j:5.23-enterprise-ubi9` - unknown; unknown

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

### `neo4j:5.23-enterprise-ubi9` - linux; arm64 variant v8

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

### `neo4j:5.23-enterprise-ubi9` - unknown; unknown

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

## `neo4j:5.23-ubi9`

```console
$ docker pull neo4j@sha256:c77cd5d0d7930ecb4580f2ddb19e7423f6ba1435a3a3faa4165e5e05945f27b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23-ubi9` - linux; amd64

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

### `neo4j:5.23-ubi9` - unknown; unknown

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

### `neo4j:5.23-ubi9` - linux; arm64 variant v8

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

### `neo4j:5.23-ubi9` - unknown; unknown

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

## `neo4j:5.23.0`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-bullseye`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-community`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-community-bullseye`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-community-ubi9`

```console
$ docker pull neo4j@sha256:c77cd5d0d7930ecb4580f2ddb19e7423f6ba1435a3a3faa4165e5e05945f27b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-community-ubi9` - linux; amd64

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

### `neo4j:5.23.0-community-ubi9` - unknown; unknown

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

### `neo4j:5.23.0-community-ubi9` - linux; arm64 variant v8

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

### `neo4j:5.23.0-community-ubi9` - unknown; unknown

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

## `neo4j:5.23.0-enterprise`

```console
$ docker pull neo4j@sha256:1e4798f5ad5581aee1a9e1407cb91a6b4c72b2c985e9e793019ab952834b9c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b5f91ecd702916f4cd7ae68a473600891a8a617bc1360bfb9cd57357e7b54fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9f0a0977ccf4f0a2ddcb5aa58692e46c3b3240266b94f540562b8ec7c71cec`
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
	-	`sha256:84e4e6b77bd9385a9a6f9a642144dd54ed07d54a4696a0521bf4efa25af637cd`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d433d9752e230bad32526fda01c334afb12cf495644179797e3c264ce20c8e8`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bacec138231cd594efc40dcad0ff5080d2d1f77c561adfa7cee6a7d3fcdb96`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74bf75996dbe9037f327f6cb03c56d4e1d43bfe4bee81cac29f6f3088cbb19`  
		Last Modified: Fri, 27 Sep 2024 06:02:49 GMT  
		Size: 410.5 MB (410499150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0518d1f857e5be99a53d90a68c728fe64c5193f4f258a7e59a720f4bf2e1b0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa92b3f1b3106604eb0bb28adeffc97ec804078cf92d11c233bd7a71ab616d04`

```dockerfile
```

-	Layers:
	-	`sha256:3296896f2d33b7629c04227fac0b219d69ff6fdba423372f4d3ff37fb1f280ad`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b29c140ca030e493c6020079aba224449dabfa9c0470c0cdc7470c84ea3178`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:69b51038d44f0f0342647a31ee5c8c0070367a1db0a179173b5432cacacbd13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a1d373b70fa75a2d37d76175581ad7f34c3717d3d5d2ec1fea8d194484245`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba146b90e0a392c265f63b58cc86ddc8ee46d5bba6a044c07f05122acab38bd7`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45695b8a9267c8834a7862ca600d7d1e0d1093777a99cfaebe459ec8aa695b67`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5f12ba6c5018de35ec6920a8ad06130ffbb1c10cd54856831d7d8701ad425`  
		Last Modified: Fri, 27 Sep 2024 15:23:22 GMT  
		Size: 410.5 MB (410461015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:040dba030ce3b6e7f8c96afc16763dd8f6b991eab9f79d488507a349ceb32ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e14288d8309236aa027c7febc1f3762ef7403c92e8a20f41424083bdea1ff1`

```dockerfile
```

-	Layers:
	-	`sha256:f3b99aeddd8d5ff4eb01e8646a356b1be27fa76dd7c635eb3ebf0048960faa4e`  
		Last Modified: Fri, 27 Sep 2024 15:23:13 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0053c396c032ad4a973385688ded9e778b8569ba381879a94b34f76bb1ea2b4`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:1e4798f5ad5581aee1a9e1407cb91a6b4c72b2c985e9e793019ab952834b9c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b5f91ecd702916f4cd7ae68a473600891a8a617bc1360bfb9cd57357e7b54fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9f0a0977ccf4f0a2ddcb5aa58692e46c3b3240266b94f540562b8ec7c71cec`
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
	-	`sha256:84e4e6b77bd9385a9a6f9a642144dd54ed07d54a4696a0521bf4efa25af637cd`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d433d9752e230bad32526fda01c334afb12cf495644179797e3c264ce20c8e8`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bacec138231cd594efc40dcad0ff5080d2d1f77c561adfa7cee6a7d3fcdb96`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74bf75996dbe9037f327f6cb03c56d4e1d43bfe4bee81cac29f6f3088cbb19`  
		Last Modified: Fri, 27 Sep 2024 06:02:49 GMT  
		Size: 410.5 MB (410499150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0518d1f857e5be99a53d90a68c728fe64c5193f4f258a7e59a720f4bf2e1b0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa92b3f1b3106604eb0bb28adeffc97ec804078cf92d11c233bd7a71ab616d04`

```dockerfile
```

-	Layers:
	-	`sha256:3296896f2d33b7629c04227fac0b219d69ff6fdba423372f4d3ff37fb1f280ad`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b29c140ca030e493c6020079aba224449dabfa9c0470c0cdc7470c84ea3178`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.23.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:69b51038d44f0f0342647a31ee5c8c0070367a1db0a179173b5432cacacbd13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a1d373b70fa75a2d37d76175581ad7f34c3717d3d5d2ec1fea8d194484245`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba146b90e0a392c265f63b58cc86ddc8ee46d5bba6a044c07f05122acab38bd7`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45695b8a9267c8834a7862ca600d7d1e0d1093777a99cfaebe459ec8aa695b67`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5f12ba6c5018de35ec6920a8ad06130ffbb1c10cd54856831d7d8701ad425`  
		Last Modified: Fri, 27 Sep 2024 15:23:22 GMT  
		Size: 410.5 MB (410461015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.23.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:040dba030ce3b6e7f8c96afc16763dd8f6b991eab9f79d488507a349ceb32ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e14288d8309236aa027c7febc1f3762ef7403c92e8a20f41424083bdea1ff1`

```dockerfile
```

-	Layers:
	-	`sha256:f3b99aeddd8d5ff4eb01e8646a356b1be27fa76dd7c635eb3ebf0048960faa4e`  
		Last Modified: Fri, 27 Sep 2024 15:23:13 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0053c396c032ad4a973385688ded9e778b8569ba381879a94b34f76bb1ea2b4`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.23.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f59e1c59f081b7ce91f88566f8eb7f6e68b5e7dab182c718cab3a0234c41e865
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-enterprise-ubi9` - linux; amd64

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

### `neo4j:5.23.0-enterprise-ubi9` - unknown; unknown

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

### `neo4j:5.23.0-enterprise-ubi9` - linux; arm64 variant v8

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

### `neo4j:5.23.0-enterprise-ubi9` - unknown; unknown

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

## `neo4j:5.23.0-ubi9`

```console
$ docker pull neo4j@sha256:c77cd5d0d7930ecb4580f2ddb19e7423f6ba1435a3a3faa4165e5e05945f27b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.23.0-ubi9` - linux; amd64

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

### `neo4j:5.23.0-ubi9` - unknown; unknown

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

### `neo4j:5.23.0-ubi9` - linux; arm64 variant v8

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

### `neo4j:5.23.0-ubi9` - unknown; unknown

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

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
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
$ docker pull neo4j@sha256:1e4798f5ad5581aee1a9e1407cb91a6b4c72b2c985e9e793019ab952834b9c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:b5f91ecd702916f4cd7ae68a473600891a8a617bc1360bfb9cd57357e7b54fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9f0a0977ccf4f0a2ddcb5aa58692e46c3b3240266b94f540562b8ec7c71cec`
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
	-	`sha256:84e4e6b77bd9385a9a6f9a642144dd54ed07d54a4696a0521bf4efa25af637cd`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d433d9752e230bad32526fda01c334afb12cf495644179797e3c264ce20c8e8`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bacec138231cd594efc40dcad0ff5080d2d1f77c561adfa7cee6a7d3fcdb96`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74bf75996dbe9037f327f6cb03c56d4e1d43bfe4bee81cac29f6f3088cbb19`  
		Last Modified: Fri, 27 Sep 2024 06:02:49 GMT  
		Size: 410.5 MB (410499150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:0518d1f857e5be99a53d90a68c728fe64c5193f4f258a7e59a720f4bf2e1b0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa92b3f1b3106604eb0bb28adeffc97ec804078cf92d11c233bd7a71ab616d04`

```dockerfile
```

-	Layers:
	-	`sha256:3296896f2d33b7629c04227fac0b219d69ff6fdba423372f4d3ff37fb1f280ad`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b29c140ca030e493c6020079aba224449dabfa9c0470c0cdc7470c84ea3178`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:69b51038d44f0f0342647a31ee5c8c0070367a1db0a179173b5432cacacbd13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a1d373b70fa75a2d37d76175581ad7f34c3717d3d5d2ec1fea8d194484245`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba146b90e0a392c265f63b58cc86ddc8ee46d5bba6a044c07f05122acab38bd7`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45695b8a9267c8834a7862ca600d7d1e0d1093777a99cfaebe459ec8aa695b67`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5f12ba6c5018de35ec6920a8ad06130ffbb1c10cd54856831d7d8701ad425`  
		Last Modified: Fri, 27 Sep 2024 15:23:22 GMT  
		Size: 410.5 MB (410461015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:040dba030ce3b6e7f8c96afc16763dd8f6b991eab9f79d488507a349ceb32ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e14288d8309236aa027c7febc1f3762ef7403c92e8a20f41424083bdea1ff1`

```dockerfile
```

-	Layers:
	-	`sha256:f3b99aeddd8d5ff4eb01e8646a356b1be27fa76dd7c635eb3ebf0048960faa4e`  
		Last Modified: Fri, 27 Sep 2024 15:23:13 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0053c396c032ad4a973385688ded9e778b8569ba381879a94b34f76bb1ea2b4`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 21.6 KB (21616 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:1e4798f5ad5581aee1a9e1407cb91a6b4c72b2c985e9e793019ab952834b9c04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b5f91ecd702916f4cd7ae68a473600891a8a617bc1360bfb9cd57357e7b54fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.1 MB (587107776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9f0a0977ccf4f0a2ddcb5aa58692e46c3b3240266b94f540562b8ec7c71cec`
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
	-	`sha256:84e4e6b77bd9385a9a6f9a642144dd54ed07d54a4696a0521bf4efa25af637cd`  
		Last Modified: Fri, 27 Sep 2024 06:02:45 GMT  
		Size: 145.2 MB (145166537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d433d9752e230bad32526fda01c334afb12cf495644179797e3c264ce20c8e8`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bacec138231cd594efc40dcad0ff5080d2d1f77c561adfa7cee6a7d3fcdb96`  
		Last Modified: Fri, 27 Sep 2024 06:02:42 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f74bf75996dbe9037f327f6cb03c56d4e1d43bfe4bee81cac29f6f3088cbb19`  
		Last Modified: Fri, 27 Sep 2024 06:02:49 GMT  
		Size: 410.5 MB (410499150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:0518d1f857e5be99a53d90a68c728fe64c5193f4f258a7e59a720f4bf2e1b0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3479993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa92b3f1b3106604eb0bb28adeffc97ec804078cf92d11c233bd7a71ab616d04`

```dockerfile
```

-	Layers:
	-	`sha256:3296896f2d33b7629c04227fac0b219d69ff6fdba423372f4d3ff37fb1f280ad`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 3.5 MB (3458980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b29c140ca030e493c6020079aba224449dabfa9c0470c0cdc7470c84ea3178`  
		Last Modified: Fri, 27 Sep 2024 06:02:43 GMT  
		Size: 21.0 KB (21013 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:69b51038d44f0f0342647a31ee5c8c0070367a1db0a179173b5432cacacbd13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **584.5 MB (584509174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307a1d373b70fa75a2d37d76175581ad7f34c3717d3d5d2ec1fea8d194484245`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba146b90e0a392c265f63b58cc86ddc8ee46d5bba6a044c07f05122acab38bd7`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 3.9 KB (3874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45695b8a9267c8834a7862ca600d7d1e0d1093777a99cfaebe459ec8aa695b67`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c5f12ba6c5018de35ec6920a8ad06130ffbb1c10cd54856831d7d8701ad425`  
		Last Modified: Fri, 27 Sep 2024 15:23:22 GMT  
		Size: 410.5 MB (410461015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:040dba030ce3b6e7f8c96afc16763dd8f6b991eab9f79d488507a349ceb32ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e14288d8309236aa027c7febc1f3762ef7403c92e8a20f41424083bdea1ff1`

```dockerfile
```

-	Layers:
	-	`sha256:f3b99aeddd8d5ff4eb01e8646a356b1be27fa76dd7c635eb3ebf0048960faa4e`  
		Last Modified: Fri, 27 Sep 2024 15:23:13 GMT  
		Size: 3.5 MB (3458672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0053c396c032ad4a973385688ded9e778b8569ba381879a94b34f76bb1ea2b4`  
		Last Modified: Fri, 27 Sep 2024 15:23:12 GMT  
		Size: 21.6 KB (21616 bytes)  
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
$ docker pull neo4j@sha256:69b9c02f73ec8335ca747e413ba29ea20aa1002a9b02c3d163793dc8c8dcffc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:e9d0e2d53d8d297c8c2be1f4237631d6c144639c4193f01e6a3090f3b63ce1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303883653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fe8107e327b41f863349008d697ac317c3c93366be9936363467dc3fa513ad`
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
	-	`sha256:25bf8144eae6630c4d46992c6b0bc335cc21f379feb09c219212a2e745bc3070`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 145.2 MB (145166558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060e63e7e44ef5c4537dae2d610abb02cc1bf7f3066b8403ae23a2383ed861e0`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76524e091c3240ee6140c1cb2bab6070dda7f26de5278719f82fcdbd1820b8a`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f94784028f3e7f2326b0ce490b4bd4873f6bac6d4ab25a36fbeb350835b5d2`  
		Last Modified: Fri, 27 Sep 2024 06:02:33 GMT  
		Size: 127.3 MB (127275004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:196728f2f8f85d2af4aaaa50d8979374964a5e2f62d94eb56f5cd1330beaa29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2864aa98f79999e8bd29d0d09061c6b1cfc944641f2285208cafcc00b5bf7659`

```dockerfile
```

-	Layers:
	-	`sha256:e27120df413aeb9db6f6407591dcf6848c64d646f05d5c745f3874aa585e7873`  
		Last Modified: Fri, 27 Sep 2024 06:02:31 GMT  
		Size: 3.2 MB (3179081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4927b29623f4b32ac3fda28dc53d34330e31bfde4b3c8321ac3ac0ac23767b2`  
		Last Modified: Fri, 27 Sep 2024 06:02:30 GMT  
		Size: 23.4 KB (23384 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c77f7c32aee60832b4d9f601b732c20eb8ae6c2fde43ebbc8c3beaa32f249c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301290633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dfab2e68ae97b458bac906f0b20d561d38a9b580253946a3351df4b89133c`
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
	-	`sha256:2317319673a9df5ed3b42eaf75a011f1481479f5a93ba9691c4531e69611903e`  
		Last Modified: Fri, 27 Sep 2024 10:35:08 GMT  
		Size: 144.0 MB (143959471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed310a72e2e4e0804c4a1c25658ebecfe0dfcdd34edbd2d0856303225d805870`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea93bedaa391daec653adf9e62ee0816600c56b3d6ffe6ca208921247db6c69`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96894ba80a2dc0aafd08517b2deb07c8b53615925a19facbc7d956617aa762fd`  
		Last Modified: Fri, 27 Sep 2024 15:21:40 GMT  
		Size: 127.2 MB (127242482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:d10d78c5f3fc8f426efdfe4f93acd56c9faad5a2cb4f594ccd983480fffcbf01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3202950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37fcb28c3a00268bd195cc3338343d40744a4d956a173affecde1b5b2dfda4`

```dockerfile
```

-	Layers:
	-	`sha256:8f63e811ca84a485a52cbb8429dc47174c514771a45418dd721b051dfd50f428`  
		Last Modified: Fri, 27 Sep 2024 15:21:37 GMT  
		Size: 3.2 MB (3178869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531764d225069803a797761f589879c1abdd81f71ccb6e7d5c10d055ae2c4675`  
		Last Modified: Fri, 27 Sep 2024 15:21:36 GMT  
		Size: 24.1 KB (24081 bytes)  
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
