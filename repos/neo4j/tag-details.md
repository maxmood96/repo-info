<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.32`](#neo4j4432)
-	[`neo4j:4.4.32-community`](#neo4j4432-community)
-	[`neo4j:4.4.32-enterprise`](#neo4j4432-enterprise)
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
-	[`neo4j:5.18`](#neo4j518)
-	[`neo4j:5.18-bullseye`](#neo4j518-bullseye)
-	[`neo4j:5.18-community`](#neo4j518-community)
-	[`neo4j:5.18-community-bullseye`](#neo4j518-community-bullseye)
-	[`neo4j:5.18-community-ubi8`](#neo4j518-community-ubi8)
-	[`neo4j:5.18-community-ubi9`](#neo4j518-community-ubi9)
-	[`neo4j:5.18-enterprise`](#neo4j518-enterprise)
-	[`neo4j:5.18-enterprise-bullseye`](#neo4j518-enterprise-bullseye)
-	[`neo4j:5.18-enterprise-ubi8`](#neo4j518-enterprise-ubi8)
-	[`neo4j:5.18-enterprise-ubi9`](#neo4j518-enterprise-ubi9)
-	[`neo4j:5.18-ubi8`](#neo4j518-ubi8)
-	[`neo4j:5.18-ubi9`](#neo4j518-ubi9)
-	[`neo4j:5.18.1`](#neo4j5181)
-	[`neo4j:5.18.1-bullseye`](#neo4j5181-bullseye)
-	[`neo4j:5.18.1-community`](#neo4j5181-community)
-	[`neo4j:5.18.1-community-bullseye`](#neo4j5181-community-bullseye)
-	[`neo4j:5.18.1-community-ubi8`](#neo4j5181-community-ubi8)
-	[`neo4j:5.18.1-community-ubi9`](#neo4j5181-community-ubi9)
-	[`neo4j:5.18.1-enterprise`](#neo4j5181-enterprise)
-	[`neo4j:5.18.1-enterprise-bullseye`](#neo4j5181-enterprise-bullseye)
-	[`neo4j:5.18.1-enterprise-ubi8`](#neo4j5181-enterprise-ubi8)
-	[`neo4j:5.18.1-enterprise-ubi9`](#neo4j5181-enterprise-ubi9)
-	[`neo4j:5.18.1-ubi8`](#neo4j5181-ubi8)
-	[`neo4j:5.18.1-ubi9`](#neo4j5181-ubi9)
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
$ docker pull neo4j@sha256:3cb27cc502efd1324ad145a686e4768e912a255a31e59a12114f0b527edd1fcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4` - linux; amd64

```console
$ docker pull neo4j@sha256:d1c9719864c034778491cb35c075d753899c3598f49ff9429f37f2c2090621f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297289279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047496e7595843a241c775bdda57a7f52789246f8cd2dc3ca3f4ff76df298cc9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 28 Feb 2024 10:51:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3db5dd28d669c9f670b2b86ab8ffd8e959e44c256bbb82fc988289462178ea5`  
		Last Modified: Tue, 12 Mar 2024 01:55:50 GMT  
		Size: 145.3 MB (145271512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7e0512782d1b5e01e3f107fbd639184ee1428acd43f6f4836e3c96ee225c89`  
		Last Modified: Tue, 12 Mar 2024 01:55:47 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de256553643941078cf58f628a6570978b59e7c95c4b9ef1f9c448873580708`  
		Last Modified: Tue, 12 Mar 2024 01:55:47 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fd990c3cc6b1b8ad7eaa88aad92f0f691e8c0dd03de702362a4f1de1cf29eb`  
		Last Modified: Tue, 12 Mar 2024 01:55:51 GMT  
		Size: 120.6 MB (120581980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:e523223361ad9f0f2b0474fd05d08bfbeb3d26cea18ef73abc169a09773b65d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511ae3d1dcfb1c3540b902802659ff4e0748f39f28fc0b0416af16cf64b949d7`

```dockerfile
```

-	Layers:
	-	`sha256:74a597744fcd7fb0655145d693f600e6fb4d02e949818a4bfe1c0617edd97f7e`  
		Last Modified: Tue, 12 Mar 2024 01:55:48 GMT  
		Size: 2.9 MB (2937569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61413f0277fd623ceb6f44e82310a459ee2529178946124ee3ae7efb368477b3`  
		Last Modified: Tue, 12 Mar 2024 01:55:47 GMT  
		Size: 20.3 KB (20319 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e86965e0061eab2e37dfd73439ba422019c05a904a79129c4763118d45688f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292638043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2df2eeb53f8318e4734f6438d4690b95d171dca396a6489614c91e34d702af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 28 Feb 2024 10:51:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf6f91a0d0df121729e6da9bb241924491f408ab746eed8f0b43c7b5dc80aaa`  
		Last Modified: Tue, 12 Mar 2024 22:19:54 GMT  
		Size: 142.0 MB (142008483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2273d01ed7414121c6e24d0df5c8b3bd6bb32ffd8c3dfeea46bdef4469308e`  
		Last Modified: Tue, 12 Mar 2024 22:19:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8f1a36ad27de5fa66e9e81c5608d6f171c5352baea827c16da4f0cf4b083b0`  
		Last Modified: Tue, 12 Mar 2024 22:19:50 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fd8b255e5e00937ea3b69e7b9d44aceebc3e9ef1d6270dff797a1ba37a65ad`  
		Last Modified: Tue, 12 Mar 2024 22:19:55 GMT  
		Size: 120.5 MB (120545126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4` - unknown; unknown

```console
$ docker pull neo4j@sha256:dad77039d8c7f42d893ce2ab5ec0b75d24eae6542f196f75ac438b402a843531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7795fb840ccd494e6ce2c15ac0ec19c6249ec0a593f7c41e5b6bb317f1093ab`

```dockerfile
```

-	Layers:
	-	`sha256:fd198f9b1cc0bb47d0f5f4137b87d10a8b13cefeebb80424aa6d1e49002cd3e7`  
		Last Modified: Tue, 12 Mar 2024 22:19:51 GMT  
		Size: 2.9 MB (2937789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8f8234b1ac24e226b9dcc7af22592bfc6db940fb4a1943def17b3de6b40a88a`  
		Last Modified: Tue, 12 Mar 2024 22:19:50 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-community`

```console
$ docker pull neo4j@sha256:3cb27cc502efd1324ad145a686e4768e912a255a31e59a12114f0b527edd1fcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-community` - linux; amd64

```console
$ docker pull neo4j@sha256:d1c9719864c034778491cb35c075d753899c3598f49ff9429f37f2c2090621f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297289279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047496e7595843a241c775bdda57a7f52789246f8cd2dc3ca3f4ff76df298cc9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 28 Feb 2024 10:51:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3db5dd28d669c9f670b2b86ab8ffd8e959e44c256bbb82fc988289462178ea5`  
		Last Modified: Tue, 12 Mar 2024 01:55:50 GMT  
		Size: 145.3 MB (145271512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7e0512782d1b5e01e3f107fbd639184ee1428acd43f6f4836e3c96ee225c89`  
		Last Modified: Tue, 12 Mar 2024 01:55:47 GMT  
		Size: 3.8 KB (3845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de256553643941078cf58f628a6570978b59e7c95c4b9ef1f9c448873580708`  
		Last Modified: Tue, 12 Mar 2024 01:55:47 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fd990c3cc6b1b8ad7eaa88aad92f0f691e8c0dd03de702362a4f1de1cf29eb`  
		Last Modified: Tue, 12 Mar 2024 01:55:51 GMT  
		Size: 120.6 MB (120581980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:e523223361ad9f0f2b0474fd05d08bfbeb3d26cea18ef73abc169a09773b65d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511ae3d1dcfb1c3540b902802659ff4e0748f39f28fc0b0416af16cf64b949d7`

```dockerfile
```

-	Layers:
	-	`sha256:74a597744fcd7fb0655145d693f600e6fb4d02e949818a4bfe1c0617edd97f7e`  
		Last Modified: Tue, 12 Mar 2024 01:55:48 GMT  
		Size: 2.9 MB (2937569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61413f0277fd623ceb6f44e82310a459ee2529178946124ee3ae7efb368477b3`  
		Last Modified: Tue, 12 Mar 2024 01:55:47 GMT  
		Size: 20.3 KB (20319 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e86965e0061eab2e37dfd73439ba422019c05a904a79129c4763118d45688f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292638043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2df2eeb53f8318e4734f6438d4690b95d171dca396a6489614c91e34d702af`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 28 Feb 2024 10:51:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=6a6849c69cf156e54cdab7dd6c938405fc4b3253227f816a01a833878679e193 NEO4J_TARBALL=neo4j-community-4.4.31-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf6f91a0d0df121729e6da9bb241924491f408ab746eed8f0b43c7b5dc80aaa`  
		Last Modified: Tue, 12 Mar 2024 22:19:54 GMT  
		Size: 142.0 MB (142008483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2273d01ed7414121c6e24d0df5c8b3bd6bb32ffd8c3dfeea46bdef4469308e`  
		Last Modified: Tue, 12 Mar 2024 22:19:50 GMT  
		Size: 3.9 KB (3866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8f1a36ad27de5fa66e9e81c5608d6f171c5352baea827c16da4f0cf4b083b0`  
		Last Modified: Tue, 12 Mar 2024 22:19:50 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fd8b255e5e00937ea3b69e7b9d44aceebc3e9ef1d6270dff797a1ba37a65ad`  
		Last Modified: Tue, 12 Mar 2024 22:19:55 GMT  
		Size: 120.5 MB (120545126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:dad77039d8c7f42d893ce2ab5ec0b75d24eae6542f196f75ac438b402a843531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7795fb840ccd494e6ce2c15ac0ec19c6249ec0a593f7c41e5b6bb317f1093ab`

```dockerfile
```

-	Layers:
	-	`sha256:fd198f9b1cc0bb47d0f5f4137b87d10a8b13cefeebb80424aa6d1e49002cd3e7`  
		Last Modified: Tue, 12 Mar 2024 22:19:51 GMT  
		Size: 2.9 MB (2937789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8f8234b1ac24e226b9dcc7af22592bfc6db940fb4a1943def17b3de6b40a88a`  
		Last Modified: Tue, 12 Mar 2024 22:19:50 GMT  
		Size: 19.3 KB (19345 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4-enterprise`

```console
$ docker pull neo4j@sha256:16080c29db39b13922a2e260f56a923cdca18445126f1209f33ba4e2ac50ddab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:ce8129818d134f97d58a4d31dd502ed23951359b8fd89052de8a04827e5af925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401118601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6b140322964bfa5352c3c09e3a0a81e37e14cebb0e9b5e5baccdcd558db540`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 28 Feb 2024 10:51:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=51b1e2141412fcfe348c3bb07cb2ad46fb86b3bfe5fc226ce21066443a4ba639 NEO4J_TARBALL=neo4j-enterprise-4.4.31-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92af0f082468a45d30f220b39e5248b65b189ca027cf382788a6f58ce058514`  
		Last Modified: Tue, 12 Mar 2024 01:56:03 GMT  
		Size: 145.3 MB (145271529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44acbc37742a651c847cb5707fc39c78b0cd289e96307b01b956ffda76b62eb7`  
		Last Modified: Tue, 12 Mar 2024 01:55:59 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9865282528c82cad4d5c3791d4ea39ded9e0bff824e963374668a52d2a3ed6`  
		Last Modified: Tue, 12 Mar 2024 01:56:00 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5460c74ee44cf5cd4e2b7ed96e9cae7e5a9d982d8d08eaff9d77b275d56582`  
		Last Modified: Tue, 12 Mar 2024 01:56:05 GMT  
		Size: 224.4 MB (224411292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c335053582a2832475984422016c8d93a1c3448202fdbc929d48cf6a89aa29f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b812b9901c327f85e36e9d4dbb7d43c104afe282ab501b5d158c71c4b55f49`

```dockerfile
```

-	Layers:
	-	`sha256:c2674a229c30b84361c6832c7be2cee50487bc287f0490a057ca26ffbf9e832b`  
		Last Modified: Tue, 12 Mar 2024 01:56:00 GMT  
		Size: 3.1 MB (3066246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5880860a848388a1039472fbe80275a91e0f1f034b69c3a787a7821ce30235a4`  
		Last Modified: Tue, 12 Mar 2024 01:55:59 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:4.4-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:90bd6cb3b7420026af74bec9654d9f241c82aa3ef2fba17d9fa6705e1289736c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 MB (396469595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0db857d94641af7db9e6ac3472c5a0261d360152a7a10e4dbbd84f729126016`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 28 Feb 2024 10:51:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 10:51:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Feb 2024 10:51:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=51b1e2141412fcfe348c3bb07cb2ad46fb86b3bfe5fc226ce21066443a4ba639 NEO4J_TARBALL=neo4j-enterprise-4.4.31-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-4.4.31-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && ln -s /startup/docker-entrypoint.sh /docker-entrypoint.sh     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 28 Feb 2024 10:51:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Feb 2024 10:51:08 GMT
WORKDIR /var/lib/neo4j
# Wed, 28 Feb 2024 10:51:08 GMT
VOLUME [/data /logs]
# Wed, 28 Feb 2024 10:51:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 28 Feb 2024 10:51:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 28 Feb 2024 10:51:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf6f91a0d0df121729e6da9bb241924491f408ab746eed8f0b43c7b5dc80aaa`  
		Last Modified: Tue, 12 Mar 2024 22:19:54 GMT  
		Size: 142.0 MB (142008483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ba82d3399d840b402b0b0c2c67c9d1ab5d1bb293cb1d7797faf2bb481c389e`  
		Last Modified: Tue, 12 Mar 2024 22:20:57 GMT  
		Size: 3.9 KB (3870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e21dae1258ac7f2589edbbe656ac003760d0b5993be16268ba00c9f908561f`  
		Last Modified: Tue, 12 Mar 2024 22:20:57 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3695b95d6e03a2012923fba0ca79b03367fd1da910f0e2ebad1033cb8a346a9`  
		Last Modified: Tue, 12 Mar 2024 22:21:02 GMT  
		Size: 224.4 MB (224376679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:4.4-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:ceb65cad4520cd905c8790cfa6ee5065dcd141cc86710804b88092ab43b2c599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3085233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b3cc00932231fe5ac33bd7618ea6b3b6a464394f5c0f73387e0648321c6359`

```dockerfile
```

-	Layers:
	-	`sha256:9b1f6f4fbb5af7963342375641c2e09b92f5b2f70c4928ea0a602ce909eb8de4`  
		Last Modified: Tue, 12 Mar 2024 22:20:57 GMT  
		Size: 3.1 MB (3066462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dace74f708639649cf2e7a7c811564d09a625c0e2264bccfb60febe8237bf3f`  
		Last Modified: Tue, 12 Mar 2024 22:20:57 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:4.4.32`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:4.4.32-community`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:4.4.32-enterprise`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:5dc36625e16511564f89eed9700a823630b201d6ef8858b86bc51b2b1e27620a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:58493c48026e0a2f692b1ccb9e492e6d65f008da5b25b1d4dd918235f7e953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557172447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f330eb7278051975e4417a4cd75fe83ee2283b214f85fb4da6e92390924231`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d02b22b4bc2ee99138f6f8c073c75ed4c005ddd1ab50d1d1c417d1c47c493`  
		Last Modified: Mon, 18 Mar 2024 18:37:16 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30416cac1a73765fc4fa530339682deca30f6e64fcc0c7b1821d3099285c7c1`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1527d59162ce7411b72ef36fab2a67fc12f3a94ddb40c697fdbb62895074cf`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc11d282d34d871d300f927eecd6a1b57bb0661a773b370cf9c721b8a36ae51`  
		Last Modified: Mon, 18 Mar 2024 18:37:19 GMT  
		Size: 380.8 MB (380843542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a2ee8765dba8ce8bb9b63e172f7f95343d3f3fdfebf34cc8abc21e6d8ad1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d8b56d5b550944a60c3bad68a8fcf7e2045d4ebb8d796028a127196800da1`

```dockerfile
```

-	Layers:
	-	`sha256:945595dfdfb5eceea1676cf83030e69f8d4baef597a4ea9a3cf166842c89ab87`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6316ff8ca6c6b92a0b7e029e2ac5fe0ac5d1ea45f41c6cd56104726599ede16b`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f7658841ee8ed7c86eec6de4ff84ca8d15af0561619b65184933a842d7abd215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554613136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca214350f164b1a084b9895df0f2a2c560f812fb31904e85a901b6d6c6e639`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf975aca6776e1475525afc9f7dadfa83d3ca0e51aa5c262d3bb07c698317f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f519102707e9f50776057036d9234fa6a4e541215b0bf4890a019807a2dd589e`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b885565db7482ee6045f6c8edb2417ca504f4a15f6a4617751375b5f83e660`  
		Last Modified: Mon, 18 Mar 2024 19:19:50 GMT  
		Size: 380.8 MB (380808174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:27037562d11b85b52043d83355c597a2b708d1362d1a131acdcf1782ffc3f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ae97f2c1c4834bb5f947891c80e4d99539be9144998e427bdf0b98c761b299`

```dockerfile
```

-	Layers:
	-	`sha256:f7b54d231e48b52f4300184e6814a3078f529c61db3a1e79a2cf08ab2be4c47f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d907b4fe83c5874e09625ab20f061731883898b0eb5afeb7f9a875211edef17`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5dc36625e16511564f89eed9700a823630b201d6ef8858b86bc51b2b1e27620a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58493c48026e0a2f692b1ccb9e492e6d65f008da5b25b1d4dd918235f7e953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557172447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f330eb7278051975e4417a4cd75fe83ee2283b214f85fb4da6e92390924231`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d02b22b4bc2ee99138f6f8c073c75ed4c005ddd1ab50d1d1c417d1c47c493`  
		Last Modified: Mon, 18 Mar 2024 18:37:16 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30416cac1a73765fc4fa530339682deca30f6e64fcc0c7b1821d3099285c7c1`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1527d59162ce7411b72ef36fab2a67fc12f3a94ddb40c697fdbb62895074cf`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc11d282d34d871d300f927eecd6a1b57bb0661a773b370cf9c721b8a36ae51`  
		Last Modified: Mon, 18 Mar 2024 18:37:19 GMT  
		Size: 380.8 MB (380843542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a2ee8765dba8ce8bb9b63e172f7f95343d3f3fdfebf34cc8abc21e6d8ad1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d8b56d5b550944a60c3bad68a8fcf7e2045d4ebb8d796028a127196800da1`

```dockerfile
```

-	Layers:
	-	`sha256:945595dfdfb5eceea1676cf83030e69f8d4baef597a4ea9a3cf166842c89ab87`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6316ff8ca6c6b92a0b7e029e2ac5fe0ac5d1ea45f41c6cd56104726599ede16b`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f7658841ee8ed7c86eec6de4ff84ca8d15af0561619b65184933a842d7abd215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554613136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca214350f164b1a084b9895df0f2a2c560f812fb31904e85a901b6d6c6e639`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf975aca6776e1475525afc9f7dadfa83d3ca0e51aa5c262d3bb07c698317f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f519102707e9f50776057036d9234fa6a4e541215b0bf4890a019807a2dd589e`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b885565db7482ee6045f6c8edb2417ca504f4a15f6a4617751375b5f83e660`  
		Last Modified: Mon, 18 Mar 2024 19:19:50 GMT  
		Size: 380.8 MB (380808174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:27037562d11b85b52043d83355c597a2b708d1362d1a131acdcf1782ffc3f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ae97f2c1c4834bb5f947891c80e4d99539be9144998e427bdf0b98c761b299`

```dockerfile
```

-	Layers:
	-	`sha256:f7b54d231e48b52f4300184e6814a3078f529c61db3a1e79a2cf08ab2be4c47f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d907b4fe83c5874e09625ab20f061731883898b0eb5afeb7f9a875211edef17`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:028d39afde25cffc412bd4d2215250643b8f78994d999d8ca44b2b6bca1e0116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:bdc85e7d4dda1d59301314fb7411398a4d8d9c76c09bfc2f31790024f20d1b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20263cfa9aaae7114b8a5e314d98325104d8c1b9f969dfcb22ec79b6fac1fde4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeaf0187031d5e65bed357c6a79752d9e5def9ee9c53c3be6c6c3a042bc5db`  
		Last Modified: Mon, 18 Mar 2024 18:37:37 GMT  
		Size: 163.6 MB (163561416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b5d48fa2aecee03dafb6be8f4133326c101ef017d6b353f7c61000ffd00fcf`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426c1d7f95efe077824e87e2534eae9acaf2a719a279c696e8feccf83a1a3fac`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 377.9 MB (377910398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:704bd376a838562ab1f9ed5ec7288f06e2bab7f4425d34e2508f0e2d5cb31487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be44e245386a0a32d7fa3e3a5026e0b3a94e589aa051c76dd77ed75c9f9390d`

```dockerfile
```

-	Layers:
	-	`sha256:aad12e01053fbf9b990734de91969d5905dd48ea47c992855ad91b536d266eeb`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e6f109446db0aba96c1b07f80229504fce79d3e7fb0c35bd61fc27424f6d4a`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:328f1909789e22d0fed607229291370642425be5d1e83b8911a10b5d8adfc6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7dce4ba3e76d332624612779eed331747d02149a43e087c72f82aca41dd3bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9296980305731d7ce62d092c2576cd341a35385e56a58fd11d67b12b96b3caa`  
		Last Modified: Mon, 18 Mar 2024 20:13:13 GMT  
		Size: 377.9 MB (377910224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:77985fbc6e6f95bdc5a6dab6a9125d77e138ba17262492f854ae69d6824dbe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97767c981b1268424128c71497280ecb5108d633eb059da5206e4d9471ff6a2`

```dockerfile
```

-	Layers:
	-	`sha256:bd439036cf03f79f376ff66cccc71f5ab7ac8038ddf54945fba09eb2e8e4979f`  
		Last Modified: Mon, 18 Mar 2024 20:12:55 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec919468a70abc4da3f758702c2efad7ebdacb31bc73b1e41407dd93b86bf9c`  
		Last Modified: Mon, 18 Mar 2024 20:12:54 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:84c02c864777ed97a8431e3b9b4406a7f49966ccd8fc86fd6db76115c01e05b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:dc763c74655873adb0691329c58edfc7552a02bbff786b085ce9d5d66e9918b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27239bba9891c68d24b03b42cd9d2b85801384d7a2dc293543227fa7de783be`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a24476c4520b1e9c9c66d29c1916e9e62c5a75316e29ce3fc9fff11b59a152`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 257.0 MB (257005824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba5a03dc0af0cc8ce429c45c6639db251f0567674616f890010b13763bc4ed6`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267d38eaffbe637912c68444a66b1b720b609ff2c3877135c3db5abd3d0797d`  
		Last Modified: Mon, 18 Mar 2024 18:37:48 GMT  
		Size: 377.9 MB (377910325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:36c457c46727f8ebd718971ffcb9de0304cb9a2e9cf0b51ef835dab7d6ab5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca751d616a406313aad5d5bd4fe7b36bdea60a843af03a2ff29f8e8758f369`

```dockerfile
```

-	Layers:
	-	`sha256:b51c8a0bdf7d22f2b4d2de07406b6a825c1e5a91801de492f35ef31d6a49c0e0`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb72743887e25635a510673c39ec83b5ae9120532fbdaa247017ce2d4e86544c`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:486cdbb0fd895d792b1567b6f2a7d8d2f0df705a0d5c42e523c4b7454fa144ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663463358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71973171c1f949830ac2f9e3c0c32edb51256f100017d5cabb477aff0877c081`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c609b766a135e00a9ded0424884aa346927f42d3db21d2f80d5dda20599bca5`  
		Last Modified: Mon, 18 Mar 2024 19:58:41 GMT  
		Size: 377.9 MB (377910423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e531c0248bccb0822ada97cfd969348dee3a50f9e4b74ec0733fca4e95642009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ab395c80e808d14fb3aae0e1d2a6183466a98b44958df3061f13375cfbba85`

```dockerfile
```

-	Layers:
	-	`sha256:7954b29e2052c6a0e0dfc227614f61aa18e39ca8069ba1657527e4a934de63cc`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d49e13727dc2f6e004439b75b5a58c304c8e36de7be9a0d3e47d6e7729dff82`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 19.8 KB (19785 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-bullseye`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-community`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-community` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-community-bullseye`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-community-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-community-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-enterprise`

```console
$ docker pull neo4j@sha256:5dc36625e16511564f89eed9700a823630b201d6ef8858b86bc51b2b1e27620a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:58493c48026e0a2f692b1ccb9e492e6d65f008da5b25b1d4dd918235f7e953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557172447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f330eb7278051975e4417a4cd75fe83ee2283b214f85fb4da6e92390924231`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d02b22b4bc2ee99138f6f8c073c75ed4c005ddd1ab50d1d1c417d1c47c493`  
		Last Modified: Mon, 18 Mar 2024 18:37:16 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30416cac1a73765fc4fa530339682deca30f6e64fcc0c7b1821d3099285c7c1`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1527d59162ce7411b72ef36fab2a67fc12f3a94ddb40c697fdbb62895074cf`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc11d282d34d871d300f927eecd6a1b57bb0661a773b370cf9c721b8a36ae51`  
		Last Modified: Mon, 18 Mar 2024 18:37:19 GMT  
		Size: 380.8 MB (380843542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a2ee8765dba8ce8bb9b63e172f7f95343d3f3fdfebf34cc8abc21e6d8ad1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d8b56d5b550944a60c3bad68a8fcf7e2045d4ebb8d796028a127196800da1`

```dockerfile
```

-	Layers:
	-	`sha256:945595dfdfb5eceea1676cf83030e69f8d4baef597a4ea9a3cf166842c89ab87`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6316ff8ca6c6b92a0b7e029e2ac5fe0ac5d1ea45f41c6cd56104726599ede16b`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f7658841ee8ed7c86eec6de4ff84ca8d15af0561619b65184933a842d7abd215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554613136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca214350f164b1a084b9895df0f2a2c560f812fb31904e85a901b6d6c6e639`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf975aca6776e1475525afc9f7dadfa83d3ca0e51aa5c262d3bb07c698317f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f519102707e9f50776057036d9234fa6a4e541215b0bf4890a019807a2dd589e`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b885565db7482ee6045f6c8edb2417ca504f4a15f6a4617751375b5f83e660`  
		Last Modified: Mon, 18 Mar 2024 19:19:50 GMT  
		Size: 380.8 MB (380808174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:27037562d11b85b52043d83355c597a2b708d1362d1a131acdcf1782ffc3f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ae97f2c1c4834bb5f947891c80e4d99539be9144998e427bdf0b98c761b299`

```dockerfile
```

-	Layers:
	-	`sha256:f7b54d231e48b52f4300184e6814a3078f529c61db3a1e79a2cf08ab2be4c47f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d907b4fe83c5874e09625ab20f061731883898b0eb5afeb7f9a875211edef17`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5dc36625e16511564f89eed9700a823630b201d6ef8858b86bc51b2b1e27620a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58493c48026e0a2f692b1ccb9e492e6d65f008da5b25b1d4dd918235f7e953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557172447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f330eb7278051975e4417a4cd75fe83ee2283b214f85fb4da6e92390924231`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d02b22b4bc2ee99138f6f8c073c75ed4c005ddd1ab50d1d1c417d1c47c493`  
		Last Modified: Mon, 18 Mar 2024 18:37:16 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30416cac1a73765fc4fa530339682deca30f6e64fcc0c7b1821d3099285c7c1`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1527d59162ce7411b72ef36fab2a67fc12f3a94ddb40c697fdbb62895074cf`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc11d282d34d871d300f927eecd6a1b57bb0661a773b370cf9c721b8a36ae51`  
		Last Modified: Mon, 18 Mar 2024 18:37:19 GMT  
		Size: 380.8 MB (380843542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a2ee8765dba8ce8bb9b63e172f7f95343d3f3fdfebf34cc8abc21e6d8ad1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d8b56d5b550944a60c3bad68a8fcf7e2045d4ebb8d796028a127196800da1`

```dockerfile
```

-	Layers:
	-	`sha256:945595dfdfb5eceea1676cf83030e69f8d4baef597a4ea9a3cf166842c89ab87`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6316ff8ca6c6b92a0b7e029e2ac5fe0ac5d1ea45f41c6cd56104726599ede16b`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f7658841ee8ed7c86eec6de4ff84ca8d15af0561619b65184933a842d7abd215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554613136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca214350f164b1a084b9895df0f2a2c560f812fb31904e85a901b6d6c6e639`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf975aca6776e1475525afc9f7dadfa83d3ca0e51aa5c262d3bb07c698317f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f519102707e9f50776057036d9234fa6a4e541215b0bf4890a019807a2dd589e`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b885565db7482ee6045f6c8edb2417ca504f4a15f6a4617751375b5f83e660`  
		Last Modified: Mon, 18 Mar 2024 19:19:50 GMT  
		Size: 380.8 MB (380808174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:27037562d11b85b52043d83355c597a2b708d1362d1a131acdcf1782ffc3f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ae97f2c1c4834bb5f947891c80e4d99539be9144998e427bdf0b98c761b299`

```dockerfile
```

-	Layers:
	-	`sha256:f7b54d231e48b52f4300184e6814a3078f529c61db3a1e79a2cf08ab2be4c47f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d907b4fe83c5874e09625ab20f061731883898b0eb5afeb7f9a875211edef17`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:028d39afde25cffc412bd4d2215250643b8f78994d999d8ca44b2b6bca1e0116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:bdc85e7d4dda1d59301314fb7411398a4d8d9c76c09bfc2f31790024f20d1b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20263cfa9aaae7114b8a5e314d98325104d8c1b9f969dfcb22ec79b6fac1fde4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeaf0187031d5e65bed357c6a79752d9e5def9ee9c53c3be6c6c3a042bc5db`  
		Last Modified: Mon, 18 Mar 2024 18:37:37 GMT  
		Size: 163.6 MB (163561416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b5d48fa2aecee03dafb6be8f4133326c101ef017d6b353f7c61000ffd00fcf`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426c1d7f95efe077824e87e2534eae9acaf2a719a279c696e8feccf83a1a3fac`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 377.9 MB (377910398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:704bd376a838562ab1f9ed5ec7288f06e2bab7f4425d34e2508f0e2d5cb31487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be44e245386a0a32d7fa3e3a5026e0b3a94e589aa051c76dd77ed75c9f9390d`

```dockerfile
```

-	Layers:
	-	`sha256:aad12e01053fbf9b990734de91969d5905dd48ea47c992855ad91b536d266eeb`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e6f109446db0aba96c1b07f80229504fce79d3e7fb0c35bd61fc27424f6d4a`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:328f1909789e22d0fed607229291370642425be5d1e83b8911a10b5d8adfc6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7dce4ba3e76d332624612779eed331747d02149a43e087c72f82aca41dd3bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9296980305731d7ce62d092c2576cd341a35385e56a58fd11d67b12b96b3caa`  
		Last Modified: Mon, 18 Mar 2024 20:13:13 GMT  
		Size: 377.9 MB (377910224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:77985fbc6e6f95bdc5a6dab6a9125d77e138ba17262492f854ae69d6824dbe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97767c981b1268424128c71497280ecb5108d633eb059da5206e4d9471ff6a2`

```dockerfile
```

-	Layers:
	-	`sha256:bd439036cf03f79f376ff66cccc71f5ab7ac8038ddf54945fba09eb2e8e4979f`  
		Last Modified: Mon, 18 Mar 2024 20:12:55 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec919468a70abc4da3f758702c2efad7ebdacb31bc73b1e41407dd93b86bf9c`  
		Last Modified: Mon, 18 Mar 2024 20:12:54 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:84c02c864777ed97a8431e3b9b4406a7f49966ccd8fc86fd6db76115c01e05b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:dc763c74655873adb0691329c58edfc7552a02bbff786b085ce9d5d66e9918b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27239bba9891c68d24b03b42cd9d2b85801384d7a2dc293543227fa7de783be`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a24476c4520b1e9c9c66d29c1916e9e62c5a75316e29ce3fc9fff11b59a152`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 257.0 MB (257005824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba5a03dc0af0cc8ce429c45c6639db251f0567674616f890010b13763bc4ed6`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267d38eaffbe637912c68444a66b1b720b609ff2c3877135c3db5abd3d0797d`  
		Last Modified: Mon, 18 Mar 2024 18:37:48 GMT  
		Size: 377.9 MB (377910325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:36c457c46727f8ebd718971ffcb9de0304cb9a2e9cf0b51ef835dab7d6ab5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca751d616a406313aad5d5bd4fe7b36bdea60a843af03a2ff29f8e8758f369`

```dockerfile
```

-	Layers:
	-	`sha256:b51c8a0bdf7d22f2b4d2de07406b6a825c1e5a91801de492f35ef31d6a49c0e0`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb72743887e25635a510673c39ec83b5ae9120532fbdaa247017ce2d4e86544c`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:486cdbb0fd895d792b1567b6f2a7d8d2f0df705a0d5c42e523c4b7454fa144ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663463358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71973171c1f949830ac2f9e3c0c32edb51256f100017d5cabb477aff0877c081`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c609b766a135e00a9ded0424884aa346927f42d3db21d2f80d5dda20599bca5`  
		Last Modified: Mon, 18 Mar 2024 19:58:41 GMT  
		Size: 377.9 MB (377910423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e531c0248bccb0822ada97cfd969348dee3a50f9e4b74ec0733fca4e95642009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ab395c80e808d14fb3aae0e1d2a6183466a98b44958df3061f13375cfbba85`

```dockerfile
```

-	Layers:
	-	`sha256:7954b29e2052c6a0e0dfc227614f61aa18e39ca8069ba1657527e4a934de63cc`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d49e13727dc2f6e004439b75b5a58c304c8e36de7be9a0d3e47d6e7729dff82`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 19.8 KB (19785 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-bullseye`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-community`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-community` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-community-bullseye`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-community-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-community-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-enterprise`

```console
$ docker pull neo4j@sha256:5dc36625e16511564f89eed9700a823630b201d6ef8858b86bc51b2b1e27620a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:58493c48026e0a2f692b1ccb9e492e6d65f008da5b25b1d4dd918235f7e953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557172447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f330eb7278051975e4417a4cd75fe83ee2283b214f85fb4da6e92390924231`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d02b22b4bc2ee99138f6f8c073c75ed4c005ddd1ab50d1d1c417d1c47c493`  
		Last Modified: Mon, 18 Mar 2024 18:37:16 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30416cac1a73765fc4fa530339682deca30f6e64fcc0c7b1821d3099285c7c1`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1527d59162ce7411b72ef36fab2a67fc12f3a94ddb40c697fdbb62895074cf`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc11d282d34d871d300f927eecd6a1b57bb0661a773b370cf9c721b8a36ae51`  
		Last Modified: Mon, 18 Mar 2024 18:37:19 GMT  
		Size: 380.8 MB (380843542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a2ee8765dba8ce8bb9b63e172f7f95343d3f3fdfebf34cc8abc21e6d8ad1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d8b56d5b550944a60c3bad68a8fcf7e2045d4ebb8d796028a127196800da1`

```dockerfile
```

-	Layers:
	-	`sha256:945595dfdfb5eceea1676cf83030e69f8d4baef597a4ea9a3cf166842c89ab87`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6316ff8ca6c6b92a0b7e029e2ac5fe0ac5d1ea45f41c6cd56104726599ede16b`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f7658841ee8ed7c86eec6de4ff84ca8d15af0561619b65184933a842d7abd215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554613136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca214350f164b1a084b9895df0f2a2c560f812fb31904e85a901b6d6c6e639`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf975aca6776e1475525afc9f7dadfa83d3ca0e51aa5c262d3bb07c698317f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f519102707e9f50776057036d9234fa6a4e541215b0bf4890a019807a2dd589e`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b885565db7482ee6045f6c8edb2417ca504f4a15f6a4617751375b5f83e660`  
		Last Modified: Mon, 18 Mar 2024 19:19:50 GMT  
		Size: 380.8 MB (380808174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:27037562d11b85b52043d83355c597a2b708d1362d1a131acdcf1782ffc3f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ae97f2c1c4834bb5f947891c80e4d99539be9144998e427bdf0b98c761b299`

```dockerfile
```

-	Layers:
	-	`sha256:f7b54d231e48b52f4300184e6814a3078f529c61db3a1e79a2cf08ab2be4c47f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d907b4fe83c5874e09625ab20f061731883898b0eb5afeb7f9a875211edef17`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5dc36625e16511564f89eed9700a823630b201d6ef8858b86bc51b2b1e27620a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58493c48026e0a2f692b1ccb9e492e6d65f008da5b25b1d4dd918235f7e953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557172447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f330eb7278051975e4417a4cd75fe83ee2283b214f85fb4da6e92390924231`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d02b22b4bc2ee99138f6f8c073c75ed4c005ddd1ab50d1d1c417d1c47c493`  
		Last Modified: Mon, 18 Mar 2024 18:37:16 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30416cac1a73765fc4fa530339682deca30f6e64fcc0c7b1821d3099285c7c1`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1527d59162ce7411b72ef36fab2a67fc12f3a94ddb40c697fdbb62895074cf`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc11d282d34d871d300f927eecd6a1b57bb0661a773b370cf9c721b8a36ae51`  
		Last Modified: Mon, 18 Mar 2024 18:37:19 GMT  
		Size: 380.8 MB (380843542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a2ee8765dba8ce8bb9b63e172f7f95343d3f3fdfebf34cc8abc21e6d8ad1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d8b56d5b550944a60c3bad68a8fcf7e2045d4ebb8d796028a127196800da1`

```dockerfile
```

-	Layers:
	-	`sha256:945595dfdfb5eceea1676cf83030e69f8d4baef597a4ea9a3cf166842c89ab87`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6316ff8ca6c6b92a0b7e029e2ac5fe0ac5d1ea45f41c6cd56104726599ede16b`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f7658841ee8ed7c86eec6de4ff84ca8d15af0561619b65184933a842d7abd215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554613136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca214350f164b1a084b9895df0f2a2c560f812fb31904e85a901b6d6c6e639`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf975aca6776e1475525afc9f7dadfa83d3ca0e51aa5c262d3bb07c698317f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f519102707e9f50776057036d9234fa6a4e541215b0bf4890a019807a2dd589e`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b885565db7482ee6045f6c8edb2417ca504f4a15f6a4617751375b5f83e660`  
		Last Modified: Mon, 18 Mar 2024 19:19:50 GMT  
		Size: 380.8 MB (380808174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:27037562d11b85b52043d83355c597a2b708d1362d1a131acdcf1782ffc3f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ae97f2c1c4834bb5f947891c80e4d99539be9144998e427bdf0b98c761b299`

```dockerfile
```

-	Layers:
	-	`sha256:f7b54d231e48b52f4300184e6814a3078f529c61db3a1e79a2cf08ab2be4c47f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d907b4fe83c5874e09625ab20f061731883898b0eb5afeb7f9a875211edef17`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:028d39afde25cffc412bd4d2215250643b8f78994d999d8ca44b2b6bca1e0116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:bdc85e7d4dda1d59301314fb7411398a4d8d9c76c09bfc2f31790024f20d1b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20263cfa9aaae7114b8a5e314d98325104d8c1b9f969dfcb22ec79b6fac1fde4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeaf0187031d5e65bed357c6a79752d9e5def9ee9c53c3be6c6c3a042bc5db`  
		Last Modified: Mon, 18 Mar 2024 18:37:37 GMT  
		Size: 163.6 MB (163561416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b5d48fa2aecee03dafb6be8f4133326c101ef017d6b353f7c61000ffd00fcf`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426c1d7f95efe077824e87e2534eae9acaf2a719a279c696e8feccf83a1a3fac`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 377.9 MB (377910398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:704bd376a838562ab1f9ed5ec7288f06e2bab7f4425d34e2508f0e2d5cb31487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be44e245386a0a32d7fa3e3a5026e0b3a94e589aa051c76dd77ed75c9f9390d`

```dockerfile
```

-	Layers:
	-	`sha256:aad12e01053fbf9b990734de91969d5905dd48ea47c992855ad91b536d266eeb`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e6f109446db0aba96c1b07f80229504fce79d3e7fb0c35bd61fc27424f6d4a`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:328f1909789e22d0fed607229291370642425be5d1e83b8911a10b5d8adfc6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7dce4ba3e76d332624612779eed331747d02149a43e087c72f82aca41dd3bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9296980305731d7ce62d092c2576cd341a35385e56a58fd11d67b12b96b3caa`  
		Last Modified: Mon, 18 Mar 2024 20:13:13 GMT  
		Size: 377.9 MB (377910224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:77985fbc6e6f95bdc5a6dab6a9125d77e138ba17262492f854ae69d6824dbe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97767c981b1268424128c71497280ecb5108d633eb059da5206e4d9471ff6a2`

```dockerfile
```

-	Layers:
	-	`sha256:bd439036cf03f79f376ff66cccc71f5ab7ac8038ddf54945fba09eb2e8e4979f`  
		Last Modified: Mon, 18 Mar 2024 20:12:55 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec919468a70abc4da3f758702c2efad7ebdacb31bc73b1e41407dd93b86bf9c`  
		Last Modified: Mon, 18 Mar 2024 20:12:54 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:84c02c864777ed97a8431e3b9b4406a7f49966ccd8fc86fd6db76115c01e05b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:dc763c74655873adb0691329c58edfc7552a02bbff786b085ce9d5d66e9918b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27239bba9891c68d24b03b42cd9d2b85801384d7a2dc293543227fa7de783be`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a24476c4520b1e9c9c66d29c1916e9e62c5a75316e29ce3fc9fff11b59a152`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 257.0 MB (257005824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba5a03dc0af0cc8ce429c45c6639db251f0567674616f890010b13763bc4ed6`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267d38eaffbe637912c68444a66b1b720b609ff2c3877135c3db5abd3d0797d`  
		Last Modified: Mon, 18 Mar 2024 18:37:48 GMT  
		Size: 377.9 MB (377910325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:36c457c46727f8ebd718971ffcb9de0304cb9a2e9cf0b51ef835dab7d6ab5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca751d616a406313aad5d5bd4fe7b36bdea60a843af03a2ff29f8e8758f369`

```dockerfile
```

-	Layers:
	-	`sha256:b51c8a0bdf7d22f2b4d2de07406b6a825c1e5a91801de492f35ef31d6a49c0e0`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb72743887e25635a510673c39ec83b5ae9120532fbdaa247017ce2d4e86544c`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:486cdbb0fd895d792b1567b6f2a7d8d2f0df705a0d5c42e523c4b7454fa144ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663463358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71973171c1f949830ac2f9e3c0c32edb51256f100017d5cabb477aff0877c081`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c609b766a135e00a9ded0424884aa346927f42d3db21d2f80d5dda20599bca5`  
		Last Modified: Mon, 18 Mar 2024 19:58:41 GMT  
		Size: 377.9 MB (377910423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e531c0248bccb0822ada97cfd969348dee3a50f9e4b74ec0733fca4e95642009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ab395c80e808d14fb3aae0e1d2a6183466a98b44958df3061f13375cfbba85`

```dockerfile
```

-	Layers:
	-	`sha256:7954b29e2052c6a0e0dfc227614f61aa18e39ca8069ba1657527e4a934de63cc`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d49e13727dc2f6e004439b75b5a58c304c8e36de7be9a0d3e47d6e7729dff82`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 19.8 KB (19785 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.1-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.1-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.1-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.1-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:5dc36625e16511564f89eed9700a823630b201d6ef8858b86bc51b2b1e27620a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:58493c48026e0a2f692b1ccb9e492e6d65f008da5b25b1d4dd918235f7e953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557172447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f330eb7278051975e4417a4cd75fe83ee2283b214f85fb4da6e92390924231`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d02b22b4bc2ee99138f6f8c073c75ed4c005ddd1ab50d1d1c417d1c47c493`  
		Last Modified: Mon, 18 Mar 2024 18:37:16 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30416cac1a73765fc4fa530339682deca30f6e64fcc0c7b1821d3099285c7c1`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1527d59162ce7411b72ef36fab2a67fc12f3a94ddb40c697fdbb62895074cf`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc11d282d34d871d300f927eecd6a1b57bb0661a773b370cf9c721b8a36ae51`  
		Last Modified: Mon, 18 Mar 2024 18:37:19 GMT  
		Size: 380.8 MB (380843542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a2ee8765dba8ce8bb9b63e172f7f95343d3f3fdfebf34cc8abc21e6d8ad1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d8b56d5b550944a60c3bad68a8fcf7e2045d4ebb8d796028a127196800da1`

```dockerfile
```

-	Layers:
	-	`sha256:945595dfdfb5eceea1676cf83030e69f8d4baef597a4ea9a3cf166842c89ab87`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6316ff8ca6c6b92a0b7e029e2ac5fe0ac5d1ea45f41c6cd56104726599ede16b`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f7658841ee8ed7c86eec6de4ff84ca8d15af0561619b65184933a842d7abd215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554613136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca214350f164b1a084b9895df0f2a2c560f812fb31904e85a901b6d6c6e639`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf975aca6776e1475525afc9f7dadfa83d3ca0e51aa5c262d3bb07c698317f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f519102707e9f50776057036d9234fa6a4e541215b0bf4890a019807a2dd589e`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b885565db7482ee6045f6c8edb2417ca504f4a15f6a4617751375b5f83e660`  
		Last Modified: Mon, 18 Mar 2024 19:19:50 GMT  
		Size: 380.8 MB (380808174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:27037562d11b85b52043d83355c597a2b708d1362d1a131acdcf1782ffc3f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ae97f2c1c4834bb5f947891c80e4d99539be9144998e427bdf0b98c761b299`

```dockerfile
```

-	Layers:
	-	`sha256:f7b54d231e48b52f4300184e6814a3078f529c61db3a1e79a2cf08ab2be4c47f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d907b4fe83c5874e09625ab20f061731883898b0eb5afeb7f9a875211edef17`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:5dc36625e16511564f89eed9700a823630b201d6ef8858b86bc51b2b1e27620a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:58493c48026e0a2f692b1ccb9e492e6d65f008da5b25b1d4dd918235f7e953ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557172447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f330eb7278051975e4417a4cd75fe83ee2283b214f85fb4da6e92390924231`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d02b22b4bc2ee99138f6f8c073c75ed4c005ddd1ab50d1d1c417d1c47c493`  
		Last Modified: Mon, 18 Mar 2024 18:37:16 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30416cac1a73765fc4fa530339682deca30f6e64fcc0c7b1821d3099285c7c1`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.8 KB (3844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1527d59162ce7411b72ef36fab2a67fc12f3a94ddb40c697fdbb62895074cf`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc11d282d34d871d300f927eecd6a1b57bb0661a773b370cf9c721b8a36ae51`  
		Last Modified: Mon, 18 Mar 2024 18:37:19 GMT  
		Size: 380.8 MB (380843542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:2a2ee8765dba8ce8bb9b63e172f7f95343d3f3fdfebf34cc8abc21e6d8ad1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d8b56d5b550944a60c3bad68a8fcf7e2045d4ebb8d796028a127196800da1`

```dockerfile
```

-	Layers:
	-	`sha256:945595dfdfb5eceea1676cf83030e69f8d4baef597a4ea9a3cf166842c89ab87`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6316ff8ca6c6b92a0b7e029e2ac5fe0ac5d1ea45f41c6cd56104726599ede16b`  
		Last Modified: Mon, 18 Mar 2024 18:37:13 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:f7658841ee8ed7c86eec6de4ff84ca8d15af0561619b65184933a842d7abd215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554613136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeca214350f164b1a084b9895df0f2a2c560f812fb31904e85a901b6d6c6e639`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addf975aca6776e1475525afc9f7dadfa83d3ca0e51aa5c262d3bb07c698317f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f519102707e9f50776057036d9234fa6a4e541215b0bf4890a019807a2dd589e`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b885565db7482ee6045f6c8edb2417ca504f4a15f6a4617751375b5f83e660`  
		Last Modified: Mon, 18 Mar 2024 19:19:50 GMT  
		Size: 380.8 MB (380808174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:27037562d11b85b52043d83355c597a2b708d1362d1a131acdcf1782ffc3f21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ae97f2c1c4834bb5f947891c80e4d99539be9144998e427bdf0b98c761b299`

```dockerfile
```

-	Layers:
	-	`sha256:f7b54d231e48b52f4300184e6814a3078f529c61db3a1e79a2cf08ab2be4c47f`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d907b4fe83c5874e09625ab20f061731883898b0eb5afeb7f9a875211edef17`  
		Last Modified: Mon, 18 Mar 2024 19:19:40 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:028d39afde25cffc412bd4d2215250643b8f78994d999d8ca44b2b6bca1e0116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:bdc85e7d4dda1d59301314fb7411398a4d8d9c76c09bfc2f31790024f20d1b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20263cfa9aaae7114b8a5e314d98325104d8c1b9f969dfcb22ec79b6fac1fde4`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeaf0187031d5e65bed357c6a79752d9e5def9ee9c53c3be6c6c3a042bc5db`  
		Last Modified: Mon, 18 Mar 2024 18:37:37 GMT  
		Size: 163.6 MB (163561416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b5d48fa2aecee03dafb6be8f4133326c101ef017d6b353f7c61000ffd00fcf`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426c1d7f95efe077824e87e2534eae9acaf2a719a279c696e8feccf83a1a3fac`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 377.9 MB (377910398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:704bd376a838562ab1f9ed5ec7288f06e2bab7f4425d34e2508f0e2d5cb31487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be44e245386a0a32d7fa3e3a5026e0b3a94e589aa051c76dd77ed75c9f9390d`

```dockerfile
```

-	Layers:
	-	`sha256:aad12e01053fbf9b990734de91969d5905dd48ea47c992855ad91b536d266eeb`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e6f109446db0aba96c1b07f80229504fce79d3e7fb0c35bd61fc27424f6d4a`  
		Last Modified: Mon, 18 Mar 2024 18:37:35 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:328f1909789e22d0fed607229291370642425be5d1e83b8911a10b5d8adfc6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7dce4ba3e76d332624612779eed331747d02149a43e087c72f82aca41dd3bf`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9296980305731d7ce62d092c2576cd341a35385e56a58fd11d67b12b96b3caa`  
		Last Modified: Mon, 18 Mar 2024 20:13:13 GMT  
		Size: 377.9 MB (377910224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:77985fbc6e6f95bdc5a6dab6a9125d77e138ba17262492f854ae69d6824dbe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97767c981b1268424128c71497280ecb5108d633eb059da5206e4d9471ff6a2`

```dockerfile
```

-	Layers:
	-	`sha256:bd439036cf03f79f376ff66cccc71f5ab7ac8038ddf54945fba09eb2e8e4979f`  
		Last Modified: Mon, 18 Mar 2024 20:12:55 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec919468a70abc4da3f758702c2efad7ebdacb31bc73b1e41407dd93b86bf9c`  
		Last Modified: Mon, 18 Mar 2024 20:12:54 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:84c02c864777ed97a8431e3b9b4406a7f49966ccd8fc86fd6db76115c01e05b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:dc763c74655873adb0691329c58edfc7552a02bbff786b085ce9d5d66e9918b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672647491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27239bba9891c68d24b03b42cd9d2b85801384d7a2dc293543227fa7de783be`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a24476c4520b1e9c9c66d29c1916e9e62c5a75316e29ce3fc9fff11b59a152`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 257.0 MB (257005824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba5a03dc0af0cc8ce429c45c6639db251f0567674616f890010b13763bc4ed6`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267d38eaffbe637912c68444a66b1b720b609ff2c3877135c3db5abd3d0797d`  
		Last Modified: Mon, 18 Mar 2024 18:37:48 GMT  
		Size: 377.9 MB (377910325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:36c457c46727f8ebd718971ffcb9de0304cb9a2e9cf0b51ef835dab7d6ab5147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca751d616a406313aad5d5bd4fe7b36bdea60a843af03a2ff29f8e8758f369`

```dockerfile
```

-	Layers:
	-	`sha256:b51c8a0bdf7d22f2b4d2de07406b6a825c1e5a91801de492f35ef31d6a49c0e0`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb72743887e25635a510673c39ec83b5ae9120532fbdaa247017ce2d4e86544c`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:486cdbb0fd895d792b1567b6f2a7d8d2f0df705a0d5c42e523c4b7454fa144ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663463358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71973171c1f949830ac2f9e3c0c32edb51256f100017d5cabb477aff0877c081`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a2ab866be05d2decef558b3e711c4b4403f3a35be6b87f7b94c618bb83b8f7c3 NEO4J_TARBALL=neo4j-enterprise-5.18.1-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c609b766a135e00a9ded0424884aa346927f42d3db21d2f80d5dda20599bca5`  
		Last Modified: Mon, 18 Mar 2024 19:58:41 GMT  
		Size: 377.9 MB (377910423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e531c0248bccb0822ada97cfd969348dee3a50f9e4b74ec0733fca4e95642009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ab395c80e808d14fb3aae0e1d2a6183466a98b44958df3061f13375cfbba85`

```dockerfile
```

-	Layers:
	-	`sha256:7954b29e2052c6a0e0dfc227614f61aa18e39ca8069ba1657527e4a934de63cc`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d49e13727dc2f6e004439b75b5a58c304c8e36de7be9a0d3e47d6e7729dff82`  
		Last Modified: Mon, 18 Mar 2024 19:58:33 GMT  
		Size: 19.8 KB (19785 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:662d0c56786b8a56a12a1b3786a40c95b5263dfc1efb66d659f3c6651ee0a45a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:343f21479a79f319e5157670b434e30f03534f6767efd001dfcfce7884790f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300370427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a7265f934caae51d1fa7ee6b527d1fec977a48b2944b46bf1a9b6b13596cc5`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2c69a7506ac99954616abf48e125d45a64b03a1db134e4da9178511165086`  
		Last Modified: Mon, 18 Mar 2024 18:37:03 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7726f9e4ee8f85b374cd47ef1528936f9a3e61663ab7b94b706b739ea1d494`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f23f1407642628b2efe371d17430d40ed16ff79c5e866a6ef7d14f29a34d162`  
		Last Modified: Mon, 18 Mar 2024 18:36:59 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989bdec5930b02bf773a070774e3abb3c989cf514d1098461386ff12938f33a`  
		Last Modified: Mon, 18 Mar 2024 18:37:02 GMT  
		Size: 124.0 MB (124041524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:acca4cf86a8f3de36629f5e8c2d9a63700e9bf837b4ad426f381b448e644074a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626530cecae907c43d88ed53ed5a59ac1b383d2edfb1afedaf564adaa3975dd`

```dockerfile
```

-	Layers:
	-	`sha256:359e436f2752b37ece536a3610142a384c0af6eec88a5db376cacdb41ddf9e23`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc27298924c99286612dfe17eaff320771a29c21a7a092dfd9d36a357700d11`  
		Last Modified: Mon, 18 Mar 2024 18:37:00 GMT  
		Size: 23.8 KB (23841 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:e9c37aa41996e5e3876a6edb95577cb029a7103ebb144abcac6f2fbc1e8764b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745ba30d84fbe58c5f80bee94f96b9c0310102d60617a3e1fd860bb4f5ecda8b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 18 Mar 2024 11:02:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1de148fde4b75e65c324edc2e56fe29527c61fcf74031052309f1425beb2cc5`  
		Last Modified: Mon, 18 Mar 2024 19:18:30 GMT  
		Size: 143.7 MB (143720408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33654896bfa132f18e870c141a7bbee9e619faed9d5ea13b041a87d746aaf9eb`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502d0ed85ec7f8104e8f8423c2e6723ec9b28b88eeaada309c27af8629c34625`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37717045a9e353b125f2c09c7e03761b5d00266011a7e32b85afecd5c1265afd`  
		Last Modified: Mon, 18 Mar 2024 19:18:29 GMT  
		Size: 124.0 MB (124006961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:3070f907838e94552fa16fe3ab3266fc44a93be3d447de4a749a8d843d812a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2974004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38066585a45e27d828d91c1efc081b954c8edd81c9de9addfcc2c2127142e8a2`

```dockerfile
```

-	Layers:
	-	`sha256:5caf4e1b560f93058d4fa723a626b2bcc1e9c49837e29b5be99b8b694c4ceed9`  
		Last Modified: Mon, 18 Mar 2024 19:18:26 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a41ce92e21fd0f4463873f1eed1caedca08420e709541264a4a913c8395cf16`  
		Last Modified: Mon, 18 Mar 2024 19:18:25 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:fb5447a4e973df1aff3d43c831d740184844ae386b4fc12e45bc92164afa622d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:a2f556e06bf1db5ea0c80e5e58283af0c69f9c39ed5f7afb1cb50a89f741ff27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8889f8037642d87730d54ad86920439d70290d9ff33e0509a4da8888c8e8648b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:b73c26168286b88f0cbea018aa5d2ae2d6ccdccabab07720055cafeee0ec53f2 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:35 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:36 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:b294072ffb946ca555767a8e3a17c9da6090d3220d076f41c17cff409732ce22 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9244dfecc1ccc589806dbe0b81ee5c8360c820b1c07153efd91e8cf84b69cb86 in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:39 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b03b22eb6f720050a3164a0ba12203c1e7d37ec09a62ed11230bd92b1a950b`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 163.6 MB (163561368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258dc6322aec0158482af61573beea4792e4876393f663b2c7e5500b883ae563`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5728d335a55ee61378ec87e92c62ecf6dab730013b899ca44ac41fbb920d668a`  
		Last Modified: Mon, 18 Mar 2024 18:37:45 GMT  
		Size: 121.1 MB (121114232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:d01608e8ff3d1699296b98c34aa586b141beb80ccd897e22b7cc5de08f6f4a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76b274335a2fee0835781bbb6b3b0477a95ba18e15c80bc8233c69b391afb3`

```dockerfile
```

-	Layers:
	-	`sha256:bdd0a226ab04a6017b7f819aff6c8ae36374a7a9ced217faf3b2cc56ad47551a`  
		Last Modified: Mon, 18 Mar 2024 18:37:42 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b64fafa92c68a70724dcd134a28534ab13926a5903d9d7b776911b0a7711d9b`  
		Last Modified: Mon, 18 Mar 2024 18:37:41 GMT  
		Size: 21.4 KB (21393 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:437a2de76437fbf6f8c1fd2884388027d4f9c0c27d0be6dea67770dc0f4e5216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59e12e3383be8d0cc2ce0e70efd8de184740e1da420be0ed72069c560fc248`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Thu, 01 Feb 2024 13:56:34 GMT
ADD file:dac41fc455d0370c9252f9bc5427fc6be222d3fd73d9d32ebf3a82860a1764a0 in / 
# Thu, 01 Feb 2024 13:56:35 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Thu, 01 Feb 2024 13:56:36 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Thu, 01 Feb 2024 13:56:36 GMT
ADD multi:5517a2f729975b00cfd83a35ef413a761bc184b02db52c20f7fd822bcc95df48 in /etc/yum.repos.d/ 
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.component="ubi8-minimal-container"       name="ubi8-minimal"       version="8.9"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 8."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 8 Minimal"
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.expose-services=""
# Thu, 01 Feb 2024 13:56:36 GMT
LABEL io.openshift.tags="minimal rhel8"
# Thu, 01 Feb 2024 13:56:36 GMT
ENV container oci
# Thu, 01 Feb 2024 13:56:36 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 13:56:36 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 13:56:37 GMT
RUN rm -rf /var/log/*
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:9306278203c47f0e103d87ee891fe13b6ea923e232ba7046ea8bbb11382a75c2 in /root/buildinfo/content_manifests/ubi8-minimal-container-8.9-1108.1706795067.json 
# Thu, 01 Feb 2024 13:56:37 GMT
ADD file:0735807c9703202a7ecd9f0d1e4447c5efc9858e58bf55c8ee8476db6b57d13e in /root/buildinfo/Dockerfile-ubi8-minimal-8.9-1108.1706795067 
# Thu, 01 Feb 2024 13:56:37 GMT
LABEL "release"="1108.1706795067" "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-02-01T13:45:18" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="7e7670a8c8c9a3be83beaa2787f3703b404d4a1d" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi8-minimal/images/8.9-1108.1706795067"
# Thu, 01 Feb 2024 13:56:38 GMT
RUN rm -f '/etc/yum.repos.d/odcs-2729145-b7022.repo' '/etc/yum.repos.d/rhel-8.9-compose-157cb.repo'
# Thu, 01 Feb 2024 13:56:40 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Thu, 01 Feb 2024 13:56:41 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750c361ee333299e8b70283d7326435a361982a4d6258a4b0e7c17bc5bebfcd`  
		Last Modified: Mon, 18 Mar 2024 20:11:54 GMT  
		Size: 162.1 MB (162132293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76389e77a00784e05bacc9edc12e3f14f41bdab7f1c647197c4d9edea2816492`  
		Last Modified: Mon, 18 Mar 2024 20:11:45 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a8c13c508b35d8714ff798a7f501d992bab9ef464d6e3c726f5ec29fe56482`  
		Last Modified: Mon, 18 Mar 2024 20:11:49 GMT  
		Size: 121.1 MB (121114301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:2791e30b0f4178a4f523fd42ef48476a2259d39f51b574978ae07367a08aed7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a14b827e6f4e0d778089e15ee3700afda7425b5cefb62d93eafb15578fc07a6`

```dockerfile
```

-	Layers:
	-	`sha256:db81c941af34e20ab23076647a06e61a687e4d8487f9a43b717dbcb565ce5f24`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09d653431446045361adb1f23765113caeb47d269e3ad50ee04c770dec90ef44`  
		Last Modified: Mon, 18 Mar 2024 20:11:46 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:af93c558ecbe5a37cc31d0419b070d4d667c94a06f6231ae18f98a1d46061f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:072f7c628663d84526b275265d83e0d95816231cef187991293592e277795f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415853375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e1571e6866bdeb64076acaeadb1b80693e6037a4e88f916ebe7cd5b7584e8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:f74dfa5d345e76f1f4d9df6077b0cdeaa5b5171f6b548ed1cac475f14515a809 in / 
# Wed, 17 Jan 2024 19:18:26 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:27 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:27 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:27 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:ef91ccf9344b424c8ead898c7856a891de97edf7461478fa846b6deffe2e8379 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:28 GMT
ADD file:75532600b86e8dbdc355d76b86fe28e825754c0d0a529f9282427ca23ab066ef in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:28 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:29 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:31 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df2a3398b842b516c771d5eb1e1e9ab08f5fd1f7dfce76fb94130949dd2869e`  
		Last Modified: Mon, 18 Mar 2024 18:37:28 GMT  
		Size: 257.0 MB (257007970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea527496274d2ad380e50a959a818a7d3b7c70e3d725657529834f288ca53a3`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb871a10466c51577b9dba606858a7fd0177e147f86668b14dcac7f8521f3275`  
		Last Modified: Mon, 18 Mar 2024 18:37:26 GMT  
		Size: 121.1 MB (121114062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:3d9587d5d0a3d3f7006426dd36c0f33782b846708d310643df8c611ec8cd879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227e7f119d150bc19d39a3213ebe85d53142bfd490bdd25a6a1dd9ace296ee5`

```dockerfile
```

-	Layers:
	-	`sha256:d69fbaa6d058aafd048755d28e85a30a1ea08539da00091a142d999189266905`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:959f973ddc43195ae8c3aea6da61701e334ab600be1d66844611dcae9c022151`  
		Last Modified: Mon, 18 Mar 2024 18:37:24 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b200fa8bdd85d054de482774960a7da159fe35483c5668f49b1884d0056be3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406667020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1176cae81f21ebc6c24eabd0e67f6e08030715693b535fd19acf18ae68731d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Wed, 17 Jan 2024 19:18:24 GMT
ADD file:a7c0bdd56d7a77d1a191f8c8ed79585935e74fd20271d6124981f2cbafd9a3e5 in / 
# Wed, 17 Jan 2024 19:18:25 GMT
RUN mv -f /etc/yum.repos.d/ubi.repo /tmp || :
# Wed, 17 Jan 2024 19:18:25 GMT
ADD file:ecc29a1455ca1b7c82018555e16e2e802135974523df6748e431f8707e759ddd in /tmp/tls-ca-bundle.pem 
# Wed, 17 Jan 2024 19:18:25 GMT
ADD multi:655128808f9801300e5f5790b55c073636035214aee6c75e0582afd288da8973 in /etc/yum.repos.d/ 
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.3"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 17 Jan 2024 19:18:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 17 Jan 2024 19:18:25 GMT
ENV container oci
# Wed, 17 Jan 2024 19:18:25 GMT
ENV PATH /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 19:18:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 19:18:27 GMT
RUN rm -rf /var/log/*
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL release=1552
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:bfcc8382df280418e841771f63af4ab23c26bfdabccba49320eca21344392059 in /root/buildinfo/content_manifests/ubi9-minimal-container-9.3-1552.json 
# Wed, 17 Jan 2024 19:18:27 GMT
ADD file:855fc5d4bbaa177d330e050fbde5d82d06b15af68fb9fcc1051cfdaafc7dcc07 in /root/buildinfo/Dockerfile-ubi9-minimal-9.3-1552 
# Wed, 17 Jan 2024 19:18:27 GMT
LABEL "distribution-scope"="public" "vendor"="Red Hat, Inc." "build-date"="2024-01-17T19:05:39" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="e8510c65a9be4b0635372fd09bee126ce7e08bc7" "io.k8s.description"="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly." "url"="https://access.redhat.com/containers/#/registry.access.redhat.com/ubi9-minimal/images/9.3-1552"
# Wed, 17 Jan 2024 19:18:28 GMT
RUN rm -f '/etc/yum.repos.d/repo-cbf3a.repo' '/etc/yum.repos.d/repo-a4968.repo'
# Wed, 17 Jan 2024 19:18:30 GMT
RUN rm -f /tmp/tls-ca-bundle.pem
# Wed, 17 Jan 2024 19:18:32 GMT
RUN mv -fZ /tmp/ubi.repo /etc/yum.repos.d/ubi.repo || :
# Mon, 18 Mar 2024 11:02:14 GMT
ENV JAVA_HOME=/usr
# Mon, 18 Mar 2024 11:02:14 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=8cd8bc48ad59f24e9949cf5a6be2fe3e100ac9eb344efea616ea0ab296411089 NEO4J_TARBALL=neo4j-community-5.18.1-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
# Mon, 18 Mar 2024 11:02:14 GMT
COPY ./local-package/* /startup/ # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.1-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Mon, 18 Mar 2024 11:02:14 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Mar 2024 11:02:14 GMT
WORKDIR /var/lib/neo4j
# Mon, 18 Mar 2024 11:02:14 GMT
VOLUME [/data /logs]
# Mon, 18 Mar 2024 11:02:14 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Mon, 18 Mar 2024 11:02:14 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Mon, 18 Mar 2024 11:02:14 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7195fd9f938653517f3c921661036bd7951932c8dda6cdcfcd9cabfa4cd4b0`  
		Last Modified: Mon, 18 Mar 2024 19:24:25 GMT  
		Size: 249.5 MB (249494310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a556e9605a1b4dfc5eec239caaa627188fa7730462d800b05286d09d356df5`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e216255fa4daa1ddc60d9926b4385d6ceafe4b914e02c1a1959a30d67bdd720`  
		Last Modified: Mon, 18 Mar 2024 19:24:23 GMT  
		Size: 121.1 MB (121114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:4146f61f7b871cfdd940d7f33ddf0ea5d5646035fd3b139ae89785b700552044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c5577b6e3516b4469658092781badfb9cb9c383f967f2bc57d9c15bc1a2064`

```dockerfile
```

-	Layers:
	-	`sha256:0aa234ec535a6afbfc44b4465afa5e352368e161e937210eccf57d7b173b6ab9`  
		Last Modified: Mon, 18 Mar 2024 19:24:20 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952bbfb4d269f6e2243370ae05f585a2c49d1266f38864d79925123b35724972`  
		Last Modified: Mon, 18 Mar 2024 19:24:19 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json
