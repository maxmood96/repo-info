<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neo4j`

-	[`neo4j:4.4`](#neo4j44)
-	[`neo4j:4.4-community`](#neo4j44-community)
-	[`neo4j:4.4-enterprise`](#neo4j44-enterprise)
-	[`neo4j:4.4.31`](#neo4j4431)
-	[`neo4j:4.4.31-community`](#neo4j4431-community)
-	[`neo4j:4.4.31-enterprise`](#neo4j4431-enterprise)
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
-	[`neo4j:5.18.0`](#neo4j5180)
-	[`neo4j:5.18.0-bullseye`](#neo4j5180-bullseye)
-	[`neo4j:5.18.0-community`](#neo4j5180-community)
-	[`neo4j:5.18.0-community-bullseye`](#neo4j5180-community-bullseye)
-	[`neo4j:5.18.0-community-ubi8`](#neo4j5180-community-ubi8)
-	[`neo4j:5.18.0-community-ubi9`](#neo4j5180-community-ubi9)
-	[`neo4j:5.18.0-enterprise`](#neo4j5180-enterprise)
-	[`neo4j:5.18.0-enterprise-bullseye`](#neo4j5180-enterprise-bullseye)
-	[`neo4j:5.18.0-enterprise-ubi8`](#neo4j5180-enterprise-ubi8)
-	[`neo4j:5.18.0-enterprise-ubi9`](#neo4j5180-enterprise-ubi9)
-	[`neo4j:5.18.0-ubi8`](#neo4j5180-ubi8)
-	[`neo4j:5.18.0-ubi9`](#neo4j5180-ubi9)
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

## `neo4j:4.4.31`

```console
$ docker pull neo4j@sha256:3cb27cc502efd1324ad145a686e4768e912a255a31e59a12114f0b527edd1fcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.31` - linux; amd64

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

### `neo4j:4.4.31` - unknown; unknown

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

### `neo4j:4.4.31` - linux; arm64 variant v8

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

### `neo4j:4.4.31` - unknown; unknown

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

## `neo4j:4.4.31-community`

```console
$ docker pull neo4j@sha256:3cb27cc502efd1324ad145a686e4768e912a255a31e59a12114f0b527edd1fcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.31-community` - linux; amd64

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

### `neo4j:4.4.31-community` - unknown; unknown

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

### `neo4j:4.4.31-community` - linux; arm64 variant v8

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

### `neo4j:4.4.31-community` - unknown; unknown

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

## `neo4j:4.4.31-enterprise`

```console
$ docker pull neo4j@sha256:16080c29db39b13922a2e260f56a923cdca18445126f1209f33ba4e2ac50ddab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:4.4.31-enterprise` - linux; amd64

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

### `neo4j:4.4.31-enterprise` - unknown; unknown

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

### `neo4j:4.4.31-enterprise` - linux; arm64 variant v8

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

### `neo4j:4.4.31-enterprise` - unknown; unknown

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

## `neo4j:5`

```console
$ docker pull neo4j@sha256:71cb98dc5542f1522526ed3c4cdcc431566c18e2fe481ccc7d0aaea7224ffcf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:8af52c7115587f6a3692a289d0c0417fee817a172e31c742c29a20dedaf2da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4bc591862134bde83b1e36fedb947cfe746212fbe980873036bc869905f3b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb35ebf43af4d5a2976763eb721f37930beb2073403f2e2a465fd56f204fcbf`  
		Last Modified: Tue, 12 Mar 2024 01:55:58 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f49e08fe440f270178b3d4fb2d4c15702727cf81e9990f622891664f48ecc1`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefef581dc74acc3e911565b057adf59b1411e2140cffa5368121cb6464accc`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267c25bcd12c7364b91278e66c044f1b83a4f11a88ebc37a049ee903cf9e24d`  
		Last Modified: Tue, 12 Mar 2024 01:55:57 GMT  
		Size: 116.1 MB (116122145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf1ddc3b9fae908039b95e2c2eed9dff15292d68b5fa6dfec9d47d1814beffba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871f8bb00f0dbd52f3bb8fbc342714f6012636da74f0d7182259d6aff3cd200d`

```dockerfile
```

-	Layers:
	-	`sha256:42c7943c814f76ca253826785f171083d3ed2b6a8586312283a2d3258529dfce`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a04b6a423ba4c7a8f89c80bf02ad9343e25a8efe3016eefbe8414f5482610d`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 23.8 KB (23842 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9d382f017f83e87fa1e957949000b1468f1f52d98f037e9c938d5f1cb8f44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f542150c0938299083e23feab8045e05f137ba8fbe19030b95b96510cac122`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd26f867f102b41367f8fe6e3cf37812e243694ffd5b8ae3a8eda398d9862eb9`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5407fc875c66651b59c3b4804def13c56999c9d0f573a42a78d7df6350e8b`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae917b13b5d0d0d6df31bc930a8b4b993f2bc76c8b21e520893c079679a17fe`  
		Last Modified: Tue, 12 Mar 2024 22:17:27 GMT  
		Size: 116.1 MB (116091424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:1701f7426d6098db0a59cdac50fcce65e93f15bdec09943885bf1ffd13e3fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f566e612a32859db77b293700c9542aa700aee93d5b8d57c6448ccf8266a0928`

```dockerfile
```

-	Layers:
	-	`sha256:3c43a64bfe9bf1ace6135c99b9e7b16793d70c648ce0f409c27247fa666597a7`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b629096654cdbd1e1c821c5fa1ce0132cf91dd7ec42cf4388eb2790bfb3c5149`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:71cb98dc5542f1522526ed3c4cdcc431566c18e2fe481ccc7d0aaea7224ffcf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8af52c7115587f6a3692a289d0c0417fee817a172e31c742c29a20dedaf2da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4bc591862134bde83b1e36fedb947cfe746212fbe980873036bc869905f3b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb35ebf43af4d5a2976763eb721f37930beb2073403f2e2a465fd56f204fcbf`  
		Last Modified: Tue, 12 Mar 2024 01:55:58 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f49e08fe440f270178b3d4fb2d4c15702727cf81e9990f622891664f48ecc1`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefef581dc74acc3e911565b057adf59b1411e2140cffa5368121cb6464accc`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267c25bcd12c7364b91278e66c044f1b83a4f11a88ebc37a049ee903cf9e24d`  
		Last Modified: Tue, 12 Mar 2024 01:55:57 GMT  
		Size: 116.1 MB (116122145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf1ddc3b9fae908039b95e2c2eed9dff15292d68b5fa6dfec9d47d1814beffba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871f8bb00f0dbd52f3bb8fbc342714f6012636da74f0d7182259d6aff3cd200d`

```dockerfile
```

-	Layers:
	-	`sha256:42c7943c814f76ca253826785f171083d3ed2b6a8586312283a2d3258529dfce`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a04b6a423ba4c7a8f89c80bf02ad9343e25a8efe3016eefbe8414f5482610d`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 23.8 KB (23842 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9d382f017f83e87fa1e957949000b1468f1f52d98f037e9c938d5f1cb8f44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f542150c0938299083e23feab8045e05f137ba8fbe19030b95b96510cac122`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd26f867f102b41367f8fe6e3cf37812e243694ffd5b8ae3a8eda398d9862eb9`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5407fc875c66651b59c3b4804def13c56999c9d0f573a42a78d7df6350e8b`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae917b13b5d0d0d6df31bc930a8b4b993f2bc76c8b21e520893c079679a17fe`  
		Last Modified: Tue, 12 Mar 2024 22:17:27 GMT  
		Size: 116.1 MB (116091424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1701f7426d6098db0a59cdac50fcce65e93f15bdec09943885bf1ffd13e3fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f566e612a32859db77b293700c9542aa700aee93d5b8d57c6448ccf8266a0928`

```dockerfile
```

-	Layers:
	-	`sha256:3c43a64bfe9bf1ace6135c99b9e7b16793d70c648ce0f409c27247fa666597a7`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b629096654cdbd1e1c821c5fa1ce0132cf91dd7ec42cf4388eb2790bfb3c5149`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:71cb98dc5542f1522526ed3c4cdcc431566c18e2fe481ccc7d0aaea7224ffcf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:8af52c7115587f6a3692a289d0c0417fee817a172e31c742c29a20dedaf2da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4bc591862134bde83b1e36fedb947cfe746212fbe980873036bc869905f3b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb35ebf43af4d5a2976763eb721f37930beb2073403f2e2a465fd56f204fcbf`  
		Last Modified: Tue, 12 Mar 2024 01:55:58 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f49e08fe440f270178b3d4fb2d4c15702727cf81e9990f622891664f48ecc1`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefef581dc74acc3e911565b057adf59b1411e2140cffa5368121cb6464accc`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267c25bcd12c7364b91278e66c044f1b83a4f11a88ebc37a049ee903cf9e24d`  
		Last Modified: Tue, 12 Mar 2024 01:55:57 GMT  
		Size: 116.1 MB (116122145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf1ddc3b9fae908039b95e2c2eed9dff15292d68b5fa6dfec9d47d1814beffba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871f8bb00f0dbd52f3bb8fbc342714f6012636da74f0d7182259d6aff3cd200d`

```dockerfile
```

-	Layers:
	-	`sha256:42c7943c814f76ca253826785f171083d3ed2b6a8586312283a2d3258529dfce`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a04b6a423ba4c7a8f89c80bf02ad9343e25a8efe3016eefbe8414f5482610d`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 23.8 KB (23842 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9d382f017f83e87fa1e957949000b1468f1f52d98f037e9c938d5f1cb8f44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f542150c0938299083e23feab8045e05f137ba8fbe19030b95b96510cac122`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd26f867f102b41367f8fe6e3cf37812e243694ffd5b8ae3a8eda398d9862eb9`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5407fc875c66651b59c3b4804def13c56999c9d0f573a42a78d7df6350e8b`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae917b13b5d0d0d6df31bc930a8b4b993f2bc76c8b21e520893c079679a17fe`  
		Last Modified: Tue, 12 Mar 2024 22:17:27 GMT  
		Size: 116.1 MB (116091424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:1701f7426d6098db0a59cdac50fcce65e93f15bdec09943885bf1ffd13e3fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f566e612a32859db77b293700c9542aa700aee93d5b8d57c6448ccf8266a0928`

```dockerfile
```

-	Layers:
	-	`sha256:3c43a64bfe9bf1ace6135c99b9e7b16793d70c648ce0f409c27247fa666597a7`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b629096654cdbd1e1c821c5fa1ce0132cf91dd7ec42cf4388eb2790bfb3c5149`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:71cb98dc5542f1522526ed3c4cdcc431566c18e2fe481ccc7d0aaea7224ffcf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8af52c7115587f6a3692a289d0c0417fee817a172e31c742c29a20dedaf2da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4bc591862134bde83b1e36fedb947cfe746212fbe980873036bc869905f3b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb35ebf43af4d5a2976763eb721f37930beb2073403f2e2a465fd56f204fcbf`  
		Last Modified: Tue, 12 Mar 2024 01:55:58 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f49e08fe440f270178b3d4fb2d4c15702727cf81e9990f622891664f48ecc1`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefef581dc74acc3e911565b057adf59b1411e2140cffa5368121cb6464accc`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267c25bcd12c7364b91278e66c044f1b83a4f11a88ebc37a049ee903cf9e24d`  
		Last Modified: Tue, 12 Mar 2024 01:55:57 GMT  
		Size: 116.1 MB (116122145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf1ddc3b9fae908039b95e2c2eed9dff15292d68b5fa6dfec9d47d1814beffba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871f8bb00f0dbd52f3bb8fbc342714f6012636da74f0d7182259d6aff3cd200d`

```dockerfile
```

-	Layers:
	-	`sha256:42c7943c814f76ca253826785f171083d3ed2b6a8586312283a2d3258529dfce`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a04b6a423ba4c7a8f89c80bf02ad9343e25a8efe3016eefbe8414f5482610d`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 23.8 KB (23842 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9d382f017f83e87fa1e957949000b1468f1f52d98f037e9c938d5f1cb8f44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f542150c0938299083e23feab8045e05f137ba8fbe19030b95b96510cac122`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd26f867f102b41367f8fe6e3cf37812e243694ffd5b8ae3a8eda398d9862eb9`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5407fc875c66651b59c3b4804def13c56999c9d0f573a42a78d7df6350e8b`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae917b13b5d0d0d6df31bc930a8b4b993f2bc76c8b21e520893c079679a17fe`  
		Last Modified: Tue, 12 Mar 2024 22:17:27 GMT  
		Size: 116.1 MB (116091424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1701f7426d6098db0a59cdac50fcce65e93f15bdec09943885bf1ffd13e3fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f566e612a32859db77b293700c9542aa700aee93d5b8d57c6448ccf8266a0928`

```dockerfile
```

-	Layers:
	-	`sha256:3c43a64bfe9bf1ace6135c99b9e7b16793d70c648ce0f409c27247fa666597a7`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b629096654cdbd1e1c821c5fa1ce0132cf91dd7ec42cf4388eb2790bfb3c5149`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:463816965a2ab466ce0337dc9f2064f8fde85b521756fe2542ea64d80c4a169a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:daa7763f0a70630f0c94ea3a51a7ecc4df560f13ccc568b5213b42beada855fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34536abe1267a0a185a701cfa7086793b432582503a02f54d81a8f599e348dc8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472fb8dc312a8f21a0830c5ed203b664a70d6f08466de7ccd1fa9e567c92445c`  
		Last Modified: Tue, 12 Mar 2024 01:56:05 GMT  
		Size: 144.9 MB (144893014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd0cd7ed6f5089702d860c810323d50754ae6f2e13ec4ed7db65878cbafbbc9`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7607c1a1728d9d10d585f4b28b59c63c4bbb31ed54c30aecce24466c2d4bc2`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cd70ba11508d3e84fa0184c03b118d0437bd2f69a8bae9924057d8a3de936`  
		Last Modified: Tue, 12 Mar 2024 01:56:10 GMT  
		Size: 389.3 MB (389324403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:232c341eb3a43c159d0157f8630454dcb9a186b5a975767d51708c5d9cc1294b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94b2ea6a7d231886c12d80eb83973ca1ede0bd1bab7fab53a5f8e3700a6814`

```dockerfile
```

-	Layers:
	-	`sha256:1257625b665585c1a3df549a65587b082e0ae433e2ceab22a95056cac64105c9`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600b02378812f5f9bd71c85123a9038948df7aac0c3bcc3aab4ec6f2d7b8c59f`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cf0d5b4184227385064becb8488e2c121e8efb327a269b6f051650bd48aa47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b7115f0207ab987fe3cee4f75d165a904bb8ede6880fef7298a030c5b8220b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed76ea2d82556dcb1f4125e14d41202c6f30e8c9d76fdf457ee3581b69d17a60`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6df90962977766b5f1e4920e0bf5f93859c8c5c905c0bdcef9678b668e19700`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045b27a1263080f5c8c1aae5c96dc284dc6a0ec748c8c9d449c0532ecf86f521`  
		Last Modified: Tue, 12 Mar 2024 22:18:46 GMT  
		Size: 389.3 MB (389287038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:d95e62cd9a196cd91aaf41d1b88ca5b7e0696b50b23696004dccc7d7689f0b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba24388356a4151796897814936f0035a924516568c10ae9e46d19c6d3ec1fa`

```dockerfile
```

-	Layers:
	-	`sha256:239427dc5acd8f2bd927ded9c08100e168df2496c6778e181aa94c24d38b590f`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c0066e29df8a2976e332f57ed5b819cdc08d6b8bcb477cadd7802f28c7f091b`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:463816965a2ab466ce0337dc9f2064f8fde85b521756fe2542ea64d80c4a169a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:daa7763f0a70630f0c94ea3a51a7ecc4df560f13ccc568b5213b42beada855fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34536abe1267a0a185a701cfa7086793b432582503a02f54d81a8f599e348dc8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472fb8dc312a8f21a0830c5ed203b664a70d6f08466de7ccd1fa9e567c92445c`  
		Last Modified: Tue, 12 Mar 2024 01:56:05 GMT  
		Size: 144.9 MB (144893014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd0cd7ed6f5089702d860c810323d50754ae6f2e13ec4ed7db65878cbafbbc9`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7607c1a1728d9d10d585f4b28b59c63c4bbb31ed54c30aecce24466c2d4bc2`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cd70ba11508d3e84fa0184c03b118d0437bd2f69a8bae9924057d8a3de936`  
		Last Modified: Tue, 12 Mar 2024 01:56:10 GMT  
		Size: 389.3 MB (389324403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:232c341eb3a43c159d0157f8630454dcb9a186b5a975767d51708c5d9cc1294b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94b2ea6a7d231886c12d80eb83973ca1ede0bd1bab7fab53a5f8e3700a6814`

```dockerfile
```

-	Layers:
	-	`sha256:1257625b665585c1a3df549a65587b082e0ae433e2ceab22a95056cac64105c9`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600b02378812f5f9bd71c85123a9038948df7aac0c3bcc3aab4ec6f2d7b8c59f`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cf0d5b4184227385064becb8488e2c121e8efb327a269b6f051650bd48aa47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b7115f0207ab987fe3cee4f75d165a904bb8ede6880fef7298a030c5b8220b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed76ea2d82556dcb1f4125e14d41202c6f30e8c9d76fdf457ee3581b69d17a60`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6df90962977766b5f1e4920e0bf5f93859c8c5c905c0bdcef9678b668e19700`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045b27a1263080f5c8c1aae5c96dc284dc6a0ec748c8c9d449c0532ecf86f521`  
		Last Modified: Tue, 12 Mar 2024 22:18:46 GMT  
		Size: 389.3 MB (389287038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d95e62cd9a196cd91aaf41d1b88ca5b7e0696b50b23696004dccc7d7689f0b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba24388356a4151796897814936f0035a924516568c10ae9e46d19c6d3ec1fa`

```dockerfile
```

-	Layers:
	-	`sha256:239427dc5acd8f2bd927ded9c08100e168df2496c6778e181aa94c24d38b590f`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c0066e29df8a2976e332f57ed5b819cdc08d6b8bcb477cadd7802f28c7f091b`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:c2f24c55f0ea8bcc80934aa179f49918f444c156023c21ff0c0c48a923b95dc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:904beb2ed79cdaa9e666223d372274cf51b44cafc5b4e07bd5799bdd100a85dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589269445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d00d9433bc176aff9e3e6b9ff21e1c7e1986cf7d9283cf319fd2824204d7edf`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a49eb38151ca388fa80eb98e18c6f5ef85dcd8fb7315fa609c498120ad28d0`  
		Last Modified: Fri, 23 Feb 2024 18:51:57 GMT  
		Size: 163.6 MB (163577740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d4ccf8ca9d5b7d2322147d5b1be42e4716c4465516776ebfadbfb8e62e8dc7`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 9.7 KB (9656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec9c83e68e904b7dc8f2fd3669ad25ad5b12cb95d576bcb94cb3cffc90d787e`  
		Last Modified: Fri, 23 Feb 2024 18:52:01 GMT  
		Size: 386.4 MB (386389914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:dca7566746c27041625a3be754241b214886d9e62c89b5b8a4b00529c9171c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11022639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a80c58be80ef10f3bc943a8e7bebdd2718fb9ade551cd06b13fe2511dec4c`

```dockerfile
```

-	Layers:
	-	`sha256:cad35efde588348e0debf23ac10130815b74fcbd073ae91b24227d4c206c02fc`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 11.0 MB (11002402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c6b5ac29d1d755218db21e6714ad1382fabf2ce3bee9152a09213fc3a80ebd`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d3ac955137b3de314a2c557dfbbfa41713e7594969586c81c1c1aa55ae987b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.8 MB (574768646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d47e8b70ec8b3c14c2794f5359d1f1fac35d4437a157a1f271ca2e1e24a858`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce38530574a0791c26c54af2213fd4d24c3d62b102f7ea8db8c9d039f289e7e`  
		Last Modified: Fri, 23 Feb 2024 19:00:52 GMT  
		Size: 386.4 MB (386389916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:9c21d7938ae4c954920e5012715ed28ae2f729ddfbca964c026a4b1be3f41ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10490618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e232450558a959f89225082823cb60af7f5fb04a7bc203b692e3a6797caef8`

```dockerfile
```

-	Layers:
	-	`sha256:0a5feb2e27d68574aa57f6c6db81f34a8173a0f41d7705b90b10cfc1453934c1`  
		Last Modified: Fri, 23 Feb 2024 19:00:44 GMT  
		Size: 10.5 MB (10470539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cc20a366bec1600c5bff7894f4252c39ee2388b19a00b856429003f45c5360`  
		Last Modified: Fri, 23 Feb 2024 19:00:43 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f4a5d6e454607ede046e96eb21122a5d66e81b024063f22abb2978a47b9f64a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ccb1ee370100eb18985fc22273d4713d7da3c03f38bc18b89dcb61c6d316a0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.1 MB (676132904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8e05085587403b0c69c7397dee2d2670105099abbf925cb6470563e67eb9f6`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aea9f35d719b8986fb084c21f8df565d1f3b38cb00bab53a4cf7fc04011ed52`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 252.0 MB (252011964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf99163b8f3a7c45f905f73d8e91c73db237e07898e572361301efe73e43f5d`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9829bdf3c809f0f1d3e727e687fe527723b2f1ece231b641810ee8adfa446bcc`  
		Last Modified: Fri, 23 Feb 2024 18:51:56 GMT  
		Size: 386.4 MB (386389639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e3916714511cc13603ae1e383b04d60a8fffcb570f43397aea38cecd8b6b4cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13722704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe4ef69dfd63cf7db912d01bd0e38570b4e3952a74889c17814f910f187755`

```dockerfile
```

-	Layers:
	-	`sha256:646669a250069b3b2bbb5ab81ee7271519680c0089ece996e83a6410f41d85cb`  
		Last Modified: Fri, 23 Feb 2024 18:51:52 GMT  
		Size: 13.7 MB (13702741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4316664f66d12d3edf32cb303d6fbd6e2da017b34972c76e99f5a6073c20f494`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9d326da1011c9d36019b40ebe80a08cdae4ae1a66807a4dec7eeccb07e7d0b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.5 MB (667475135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82db0c22b7b49b9111609e9db96568b69802a24644f25765545221294122b17`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4079f7a3f13239ba4e7d4a97e2e3b193be6700523aa4e469dc31a81127fcb01`  
		Last Modified: Fri, 23 Feb 2024 18:58:52 GMT  
		Size: 386.4 MB (386389645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:62591f21bb56eac783a50278f0cf8a7b081d322fa670ae4b4b72932c2834fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13615603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b690629f9e2e5d5132f7e8a0832e8f96434e2908160bc9b1e10464c04abca43`

```dockerfile
```

-	Layers:
	-	`sha256:6403bb678609276aada73532e28a48934d2f75c3301bc5888531dc0dce02e013`  
		Last Modified: Fri, 23 Feb 2024 18:58:44 GMT  
		Size: 13.6 MB (13595797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8307bca2c474b1b9a72ed3caae6900cf7c93d6f83d9b75b9945290ec6595d865`  
		Last Modified: Fri, 23 Feb 2024 18:58:43 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-bullseye`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-community`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-community-bullseye`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-community-ubi8`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-community-ubi9`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-enterprise`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-ubi8`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18-ubi9`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-bullseye`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-community`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-community-bullseye`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-community-ubi8`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-community-ubi9`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-enterprise`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-ubi8`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:5.18.0-ubi9`

```console
$ docker pull neo4j@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:71cb98dc5542f1522526ed3c4cdcc431566c18e2fe481ccc7d0aaea7224ffcf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8af52c7115587f6a3692a289d0c0417fee817a172e31c742c29a20dedaf2da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4bc591862134bde83b1e36fedb947cfe746212fbe980873036bc869905f3b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb35ebf43af4d5a2976763eb721f37930beb2073403f2e2a465fd56f204fcbf`  
		Last Modified: Tue, 12 Mar 2024 01:55:58 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f49e08fe440f270178b3d4fb2d4c15702727cf81e9990f622891664f48ecc1`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefef581dc74acc3e911565b057adf59b1411e2140cffa5368121cb6464accc`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267c25bcd12c7364b91278e66c044f1b83a4f11a88ebc37a049ee903cf9e24d`  
		Last Modified: Tue, 12 Mar 2024 01:55:57 GMT  
		Size: 116.1 MB (116122145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf1ddc3b9fae908039b95e2c2eed9dff15292d68b5fa6dfec9d47d1814beffba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871f8bb00f0dbd52f3bb8fbc342714f6012636da74f0d7182259d6aff3cd200d`

```dockerfile
```

-	Layers:
	-	`sha256:42c7943c814f76ca253826785f171083d3ed2b6a8586312283a2d3258529dfce`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a04b6a423ba4c7a8f89c80bf02ad9343e25a8efe3016eefbe8414f5482610d`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 23.8 KB (23842 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9d382f017f83e87fa1e957949000b1468f1f52d98f037e9c938d5f1cb8f44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f542150c0938299083e23feab8045e05f137ba8fbe19030b95b96510cac122`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd26f867f102b41367f8fe6e3cf37812e243694ffd5b8ae3a8eda398d9862eb9`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5407fc875c66651b59c3b4804def13c56999c9d0f573a42a78d7df6350e8b`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae917b13b5d0d0d6df31bc930a8b4b993f2bc76c8b21e520893c079679a17fe`  
		Last Modified: Tue, 12 Mar 2024 22:17:27 GMT  
		Size: 116.1 MB (116091424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1701f7426d6098db0a59cdac50fcce65e93f15bdec09943885bf1ffd13e3fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f566e612a32859db77b293700c9542aa700aee93d5b8d57c6448ccf8266a0928`

```dockerfile
```

-	Layers:
	-	`sha256:3c43a64bfe9bf1ace6135c99b9e7b16793d70c648ce0f409c27247fa666597a7`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b629096654cdbd1e1c821c5fa1ce0132cf91dd7ec42cf4388eb2790bfb3c5149`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:71cb98dc5542f1522526ed3c4cdcc431566c18e2fe481ccc7d0aaea7224ffcf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:8af52c7115587f6a3692a289d0c0417fee817a172e31c742c29a20dedaf2da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4bc591862134bde83b1e36fedb947cfe746212fbe980873036bc869905f3b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb35ebf43af4d5a2976763eb721f37930beb2073403f2e2a465fd56f204fcbf`  
		Last Modified: Tue, 12 Mar 2024 01:55:58 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f49e08fe440f270178b3d4fb2d4c15702727cf81e9990f622891664f48ecc1`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefef581dc74acc3e911565b057adf59b1411e2140cffa5368121cb6464accc`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267c25bcd12c7364b91278e66c044f1b83a4f11a88ebc37a049ee903cf9e24d`  
		Last Modified: Tue, 12 Mar 2024 01:55:57 GMT  
		Size: 116.1 MB (116122145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf1ddc3b9fae908039b95e2c2eed9dff15292d68b5fa6dfec9d47d1814beffba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871f8bb00f0dbd52f3bb8fbc342714f6012636da74f0d7182259d6aff3cd200d`

```dockerfile
```

-	Layers:
	-	`sha256:42c7943c814f76ca253826785f171083d3ed2b6a8586312283a2d3258529dfce`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a04b6a423ba4c7a8f89c80bf02ad9343e25a8efe3016eefbe8414f5482610d`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 23.8 KB (23842 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9d382f017f83e87fa1e957949000b1468f1f52d98f037e9c938d5f1cb8f44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f542150c0938299083e23feab8045e05f137ba8fbe19030b95b96510cac122`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd26f867f102b41367f8fe6e3cf37812e243694ffd5b8ae3a8eda398d9862eb9`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5407fc875c66651b59c3b4804def13c56999c9d0f573a42a78d7df6350e8b`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae917b13b5d0d0d6df31bc930a8b4b993f2bc76c8b21e520893c079679a17fe`  
		Last Modified: Tue, 12 Mar 2024 22:17:27 GMT  
		Size: 116.1 MB (116091424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:1701f7426d6098db0a59cdac50fcce65e93f15bdec09943885bf1ffd13e3fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f566e612a32859db77b293700c9542aa700aee93d5b8d57c6448ccf8266a0928`

```dockerfile
```

-	Layers:
	-	`sha256:3c43a64bfe9bf1ace6135c99b9e7b16793d70c648ce0f409c27247fa666597a7`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b629096654cdbd1e1c821c5fa1ce0132cf91dd7ec42cf4388eb2790bfb3c5149`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:71cb98dc5542f1522526ed3c4cdcc431566c18e2fe481ccc7d0aaea7224ffcf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:8af52c7115587f6a3692a289d0c0417fee817a172e31c742c29a20dedaf2da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4bc591862134bde83b1e36fedb947cfe746212fbe980873036bc869905f3b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb35ebf43af4d5a2976763eb721f37930beb2073403f2e2a465fd56f204fcbf`  
		Last Modified: Tue, 12 Mar 2024 01:55:58 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f49e08fe440f270178b3d4fb2d4c15702727cf81e9990f622891664f48ecc1`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefef581dc74acc3e911565b057adf59b1411e2140cffa5368121cb6464accc`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267c25bcd12c7364b91278e66c044f1b83a4f11a88ebc37a049ee903cf9e24d`  
		Last Modified: Tue, 12 Mar 2024 01:55:57 GMT  
		Size: 116.1 MB (116122145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf1ddc3b9fae908039b95e2c2eed9dff15292d68b5fa6dfec9d47d1814beffba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871f8bb00f0dbd52f3bb8fbc342714f6012636da74f0d7182259d6aff3cd200d`

```dockerfile
```

-	Layers:
	-	`sha256:42c7943c814f76ca253826785f171083d3ed2b6a8586312283a2d3258529dfce`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a04b6a423ba4c7a8f89c80bf02ad9343e25a8efe3016eefbe8414f5482610d`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 23.8 KB (23842 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9d382f017f83e87fa1e957949000b1468f1f52d98f037e9c938d5f1cb8f44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f542150c0938299083e23feab8045e05f137ba8fbe19030b95b96510cac122`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd26f867f102b41367f8fe6e3cf37812e243694ffd5b8ae3a8eda398d9862eb9`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5407fc875c66651b59c3b4804def13c56999c9d0f573a42a78d7df6350e8b`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae917b13b5d0d0d6df31bc930a8b4b993f2bc76c8b21e520893c079679a17fe`  
		Last Modified: Tue, 12 Mar 2024 22:17:27 GMT  
		Size: 116.1 MB (116091424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:1701f7426d6098db0a59cdac50fcce65e93f15bdec09943885bf1ffd13e3fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f566e612a32859db77b293700c9542aa700aee93d5b8d57c6448ccf8266a0928`

```dockerfile
```

-	Layers:
	-	`sha256:3c43a64bfe9bf1ace6135c99b9e7b16793d70c648ce0f409c27247fa666597a7`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b629096654cdbd1e1c821c5fa1ce0132cf91dd7ec42cf4388eb2790bfb3c5149`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:463816965a2ab466ce0337dc9f2064f8fde85b521756fe2542ea64d80c4a169a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:daa7763f0a70630f0c94ea3a51a7ecc4df560f13ccc568b5213b42beada855fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34536abe1267a0a185a701cfa7086793b432582503a02f54d81a8f599e348dc8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472fb8dc312a8f21a0830c5ed203b664a70d6f08466de7ccd1fa9e567c92445c`  
		Last Modified: Tue, 12 Mar 2024 01:56:05 GMT  
		Size: 144.9 MB (144893014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd0cd7ed6f5089702d860c810323d50754ae6f2e13ec4ed7db65878cbafbbc9`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7607c1a1728d9d10d585f4b28b59c63c4bbb31ed54c30aecce24466c2d4bc2`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cd70ba11508d3e84fa0184c03b118d0437bd2f69a8bae9924057d8a3de936`  
		Last Modified: Tue, 12 Mar 2024 01:56:10 GMT  
		Size: 389.3 MB (389324403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:232c341eb3a43c159d0157f8630454dcb9a186b5a975767d51708c5d9cc1294b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94b2ea6a7d231886c12d80eb83973ca1ede0bd1bab7fab53a5f8e3700a6814`

```dockerfile
```

-	Layers:
	-	`sha256:1257625b665585c1a3df549a65587b082e0ae433e2ceab22a95056cac64105c9`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600b02378812f5f9bd71c85123a9038948df7aac0c3bcc3aab4ec6f2d7b8c59f`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cf0d5b4184227385064becb8488e2c121e8efb327a269b6f051650bd48aa47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b7115f0207ab987fe3cee4f75d165a904bb8ede6880fef7298a030c5b8220b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed76ea2d82556dcb1f4125e14d41202c6f30e8c9d76fdf457ee3581b69d17a60`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6df90962977766b5f1e4920e0bf5f93859c8c5c905c0bdcef9678b668e19700`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045b27a1263080f5c8c1aae5c96dc284dc6a0ec748c8c9d449c0532ecf86f521`  
		Last Modified: Tue, 12 Mar 2024 22:18:46 GMT  
		Size: 389.3 MB (389287038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:d95e62cd9a196cd91aaf41d1b88ca5b7e0696b50b23696004dccc7d7689f0b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba24388356a4151796897814936f0035a924516568c10ae9e46d19c6d3ec1fa`

```dockerfile
```

-	Layers:
	-	`sha256:239427dc5acd8f2bd927ded9c08100e168df2496c6778e181aa94c24d38b590f`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c0066e29df8a2976e332f57ed5b819cdc08d6b8bcb477cadd7802f28c7f091b`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:463816965a2ab466ce0337dc9f2064f8fde85b521756fe2542ea64d80c4a169a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:daa7763f0a70630f0c94ea3a51a7ecc4df560f13ccc568b5213b42beada855fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **565.7 MB (565653277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34536abe1267a0a185a701cfa7086793b432582503a02f54d81a8f599e348dc8`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472fb8dc312a8f21a0830c5ed203b664a70d6f08466de7ccd1fa9e567c92445c`  
		Last Modified: Tue, 12 Mar 2024 01:56:05 GMT  
		Size: 144.9 MB (144893014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd0cd7ed6f5089702d860c810323d50754ae6f2e13ec4ed7db65878cbafbbc9`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7607c1a1728d9d10d585f4b28b59c63c4bbb31ed54c30aecce24466c2d4bc2`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61cd70ba11508d3e84fa0184c03b118d0437bd2f69a8bae9924057d8a3de936`  
		Last Modified: Tue, 12 Mar 2024 01:56:10 GMT  
		Size: 389.3 MB (389324403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:232c341eb3a43c159d0157f8630454dcb9a186b5a975767d51708c5d9cc1294b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3145187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec94b2ea6a7d231886c12d80eb83973ca1ede0bd1bab7fab53a5f8e3700a6814`

```dockerfile
```

-	Layers:
	-	`sha256:1257625b665585c1a3df549a65587b082e0ae433e2ceab22a95056cac64105c9`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 3.1 MB (3123713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600b02378812f5f9bd71c85123a9038948df7aac0c3bcc3aab4ec6f2d7b8c59f`  
		Last Modified: Tue, 12 Mar 2024 01:56:01 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:0cf0d5b4184227385064becb8488e2c121e8efb327a269b6f051650bd48aa47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **563.1 MB (563091959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b7115f0207ab987fe3cee4f75d165a904bb8ede6880fef7298a030c5b8220b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed76ea2d82556dcb1f4125e14d41202c6f30e8c9d76fdf457ee3581b69d17a60`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 3.9 KB (3867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6df90962977766b5f1e4920e0bf5f93859c8c5c905c0bdcef9678b668e19700`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045b27a1263080f5c8c1aae5c96dc284dc6a0ec748c8c9d449c0532ecf86f521`  
		Last Modified: Tue, 12 Mar 2024 22:18:46 GMT  
		Size: 389.3 MB (389287038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d95e62cd9a196cd91aaf41d1b88ca5b7e0696b50b23696004dccc7d7689f0b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3144448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba24388356a4151796897814936f0035a924516568c10ae9e46d19c6d3ec1fa`

```dockerfile
```

-	Layers:
	-	`sha256:239427dc5acd8f2bd927ded9c08100e168df2496c6778e181aa94c24d38b590f`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 3.1 MB (3123941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c0066e29df8a2976e332f57ed5b819cdc08d6b8bcb477cadd7802f28c7f091b`  
		Last Modified: Tue, 12 Mar 2024 22:18:38 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:c2f24c55f0ea8bcc80934aa179f49918f444c156023c21ff0c0c48a923b95dc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:904beb2ed79cdaa9e666223d372274cf51b44cafc5b4e07bd5799bdd100a85dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.3 MB (589269445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d00d9433bc176aff9e3e6b9ff21e1c7e1986cf7d9283cf319fd2824204d7edf`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a49eb38151ca388fa80eb98e18c6f5ef85dcd8fb7315fa609c498120ad28d0`  
		Last Modified: Fri, 23 Feb 2024 18:51:57 GMT  
		Size: 163.6 MB (163577740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d4ccf8ca9d5b7d2322147d5b1be42e4716c4465516776ebfadbfb8e62e8dc7`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 9.7 KB (9656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec9c83e68e904b7dc8f2fd3669ad25ad5b12cb95d576bcb94cb3cffc90d787e`  
		Last Modified: Fri, 23 Feb 2024 18:52:01 GMT  
		Size: 386.4 MB (386389914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:dca7566746c27041625a3be754241b214886d9e62c89b5b8a4b00529c9171c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11022639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a80c58be80ef10f3bc943a8e7bebdd2718fb9ade551cd06b13fe2511dec4c`

```dockerfile
```

-	Layers:
	-	`sha256:cad35efde588348e0debf23ac10130815b74fcbd073ae91b24227d4c206c02fc`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 11.0 MB (11002402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05c6b5ac29d1d755218db21e6714ad1382fabf2ce3bee9152a09213fc3a80ebd`  
		Last Modified: Fri, 23 Feb 2024 18:51:54 GMT  
		Size: 20.2 KB (20237 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:d3ac955137b3de314a2c557dfbbfa41713e7594969586c81c1c1aa55ae987b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **574.8 MB (574768646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d47e8b70ec8b3c14c2794f5359d1f1fac35d4437a157a1f271ca2e1e24a858`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce38530574a0791c26c54af2213fd4d24c3d62b102f7ea8db8c9d039f289e7e`  
		Last Modified: Fri, 23 Feb 2024 19:00:52 GMT  
		Size: 386.4 MB (386389916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:9c21d7938ae4c954920e5012715ed28ae2f729ddfbca964c026a4b1be3f41ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10490618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e232450558a959f89225082823cb60af7f5fb04a7bc203b692e3a6797caef8`

```dockerfile
```

-	Layers:
	-	`sha256:0a5feb2e27d68574aa57f6c6db81f34a8173a0f41d7705b90b10cfc1453934c1`  
		Last Modified: Fri, 23 Feb 2024 19:00:44 GMT  
		Size: 10.5 MB (10470539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cc20a366bec1600c5bff7894f4252c39ee2388b19a00b856429003f45c5360`  
		Last Modified: Fri, 23 Feb 2024 19:00:43 GMT  
		Size: 20.1 KB (20079 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:f4a5d6e454607ede046e96eb21122a5d66e81b024063f22abb2978a47b9f64a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:ccb1ee370100eb18985fc22273d4713d7da3c03f38bc18b89dcb61c6d316a0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.1 MB (676132904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8e05085587403b0c69c7397dee2d2670105099abbf925cb6470563e67eb9f6`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aea9f35d719b8986fb084c21f8df565d1f3b38cb00bab53a4cf7fc04011ed52`  
		Last Modified: Fri, 23 Feb 2024 18:51:55 GMT  
		Size: 252.0 MB (252011964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf99163b8f3a7c45f905f73d8e91c73db237e07898e572361301efe73e43f5d`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9829bdf3c809f0f1d3e727e687fe527723b2f1ece231b641810ee8adfa446bcc`  
		Last Modified: Fri, 23 Feb 2024 18:51:56 GMT  
		Size: 386.4 MB (386389639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:e3916714511cc13603ae1e383b04d60a8fffcb570f43397aea38cecd8b6b4cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13722704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe4ef69dfd63cf7db912d01bd0e38570b4e3952a74889c17814f910f187755`

```dockerfile
```

-	Layers:
	-	`sha256:646669a250069b3b2bbb5ab81ee7271519680c0089ece996e83a6410f41d85cb`  
		Last Modified: Fri, 23 Feb 2024 18:51:52 GMT  
		Size: 13.7 MB (13702741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4316664f66d12d3edf32cb303d6fbd6e2da017b34972c76e99f5a6073c20f494`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 20.0 KB (19963 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:9d326da1011c9d36019b40ebe80a08cdae4ae1a66807a4dec7eeccb07e7d0b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.5 MB (667475135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82db0c22b7b49b9111609e9db96568b69802a24644f25765545221294122b17`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=a0acf804ff2f4bbb18f9ab8e2ee9e60f614056a361987be293f09acc2d3f0ff4 NEO4J_TARBALL=neo4j-enterprise-5.17.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4079f7a3f13239ba4e7d4a97e2e3b193be6700523aa4e469dc31a81127fcb01`  
		Last Modified: Fri, 23 Feb 2024 18:58:52 GMT  
		Size: 386.4 MB (386389645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:62591f21bb56eac783a50278f0cf8a7b081d322fa670ae4b4b72932c2834fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13615603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b690629f9e2e5d5132f7e8a0832e8f96434e2908160bc9b1e10464c04abca43`

```dockerfile
```

-	Layers:
	-	`sha256:6403bb678609276aada73532e28a48934d2f75c3301bc5888531dc0dce02e013`  
		Last Modified: Fri, 23 Feb 2024 18:58:44 GMT  
		Size: 13.6 MB (13595797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8307bca2c474b1b9a72ed3caae6900cf7c93d6f83d9b75b9945290ec6595d865`  
		Last Modified: Fri, 23 Feb 2024 18:58:43 GMT  
		Size: 19.8 KB (19806 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:71cb98dc5542f1522526ed3c4cdcc431566c18e2fe481ccc7d0aaea7224ffcf5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:8af52c7115587f6a3692a289d0c0417fee817a172e31c742c29a20dedaf2da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292451004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4bc591862134bde83b1e36fedb947cfe746212fbe980873036bc869905f3b`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb35ebf43af4d5a2976763eb721f37930beb2073403f2e2a465fd56f204fcbf`  
		Last Modified: Tue, 12 Mar 2024 01:55:58 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f49e08fe440f270178b3d4fb2d4c15702727cf81e9990f622891664f48ecc1`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefef581dc74acc3e911565b057adf59b1411e2140cffa5368121cb6464accc`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 9.5 KB (9500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c267c25bcd12c7364b91278e66c044f1b83a4f11a88ebc37a049ee903cf9e24d`  
		Last Modified: Tue, 12 Mar 2024 01:55:57 GMT  
		Size: 116.1 MB (116122145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:bf1ddc3b9fae908039b95e2c2eed9dff15292d68b5fa6dfec9d47d1814beffba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871f8bb00f0dbd52f3bb8fbc342714f6012636da74f0d7182259d6aff3cd200d`

```dockerfile
```

-	Layers:
	-	`sha256:42c7943c814f76ca253826785f171083d3ed2b6a8586312283a2d3258529dfce`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 2.9 MB (2934302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a04b6a423ba4c7a8f89c80bf02ad9343e25a8efe3016eefbe8414f5482610d`  
		Last Modified: Tue, 12 Mar 2024 01:55:54 GMT  
		Size: 23.8 KB (23842 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c9d382f017f83e87fa1e957949000b1468f1f52d98f037e9c938d5f1cb8f44d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289896344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f542150c0938299083e23feab8045e05f137ba8fbe19030b95b96510cac122`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Fri, 23 Feb 2024 15:05:08 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 23 Feb 2024 15:05:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e38e4dfe0d7e2b4c883bb9dbdfb9b92f0fcdb107d3f003c2a17ac9b9ab90267`  
		Last Modified: Tue, 12 Mar 2024 22:17:28 GMT  
		Size: 143.7 MB (143720407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd26f867f102b41367f8fe6e3cf37812e243694ffd5b8ae3a8eda398d9862eb9`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 3.9 KB (3868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5407fc875c66651b59c3b4804def13c56999c9d0f573a42a78d7df6350e8b`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae917b13b5d0d0d6df31bc930a8b4b993f2bc76c8b21e520893c079679a17fe`  
		Last Modified: Tue, 12 Mar 2024 22:17:27 GMT  
		Size: 116.1 MB (116091424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:1701f7426d6098db0a59cdac50fcce65e93f15bdec09943885bf1ffd13e3fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2958256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f566e612a32859db77b293700c9542aa700aee93d5b8d57c6448ccf8266a0928`

```dockerfile
```

-	Layers:
	-	`sha256:3c43a64bfe9bf1ace6135c99b9e7b16793d70c648ce0f409c27247fa666597a7`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 2.9 MB (2934546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b629096654cdbd1e1c821c5fa1ce0132cf91dd7ec42cf4388eb2790bfb3c5149`  
		Last Modified: Tue, 12 Mar 2024 22:17:24 GMT  
		Size: 23.7 KB (23710 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:7976dfbb7e11c0ba2dff811cd3b56728bcc7f2b86222b019b290007211c316f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:c8f213f9b772c89ba430bccdf706b3268630e2a11221e032882c6c633a05b31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316074525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007a1daaaefc32c82b42e604f7d6e780ca253ce15bbd6fcd64d00b82ca4bb5fe`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ec5973593eada6ab2789103967dd694b6e5c1a265c90d0c12cb4e29d8597e`  
		Last Modified: Fri, 23 Feb 2024 18:51:41 GMT  
		Size: 163.6 MB (163578461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcdf104cb5a2499d6e8e5c0783a53ee53975a985fe35dd65f7e07ab44b61a0b`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 9.7 KB (9657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc6a1c197e449e15f8c0cdb910dd2ff832397a5b205fbb09701feca75cf82b6`  
		Last Modified: Fri, 23 Feb 2024 18:51:39 GMT  
		Size: 113.2 MB (113194272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:ef5fd3f0224f021775f26d79dbf1e5c48105de065cb055eb2701bec280d04ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c7b8c780bfab2f064e1e76ca4801515ec9ea374ec6a577b16ff98b72542fa`

```dockerfile
```

-	Layers:
	-	`sha256:5ac698fdd22d8234e44fda134a18db48146831ddd6c81fbd161aa27028d05ead`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 10.8 MB (10811797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34104f6cb1d9e05bf005b545081a0494a487ac8ab4439dd12f313a964ca7d9b1`  
		Last Modified: Fri, 23 Feb 2024 18:51:38 GMT  
		Size: 21.4 KB (21415 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:88b796cf8af2eb94e18ba3877587ae63e66d1dca47e093a020433c83de7fba75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301573045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391974af9b9a3d7e78ce7c5be82f663cfeb3cd3b2f4c1e1d3e275eccd718b197`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bbc3c91d353b5c5584684a520bfe6e3f7f8ea7d6ec345e1353e02958e4b37`  
		Last Modified: Mon, 05 Feb 2024 22:36:58 GMT  
		Size: 150.7 MB (150729110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924ad1acd80aa5b1134005ae00c85318cca8a2cb7d4420aa803edeb7e7f558a2`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 9.7 KB (9658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba7e4586366143734b3e29f5f8f4f476345d2cf346a7681cf8eae7180bbd72c`  
		Last Modified: Fri, 23 Feb 2024 18:59:43 GMT  
		Size: 113.2 MB (113194315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:381e7b9b0e70ad72b2559835dd673b8dd33b453327381b6d1a26ce05dfecef68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10301208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b680e500dc0c321c979caaebd49fc92227cd701ac391744af41131d103e55ba`

```dockerfile
```

-	Layers:
	-	`sha256:d70aa085f0f713585a03b44a83028543600cecd7f1750a3a0b08ad0da4e3f8f8`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 10.3 MB (10279942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4252dee01dda03a9e21671663ef123ef9e7d7d3ec7cfd6b376880cfc77521792`  
		Last Modified: Fri, 23 Feb 2024 18:59:40 GMT  
		Size: 21.3 KB (21266 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:518658cb61bde33e7ab11aeee0cb1e1dd7b66f83b962f75ab4a9df8b4885549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:3ad06565d7068eac9ba357682b47addb2b9e8d0d5341c4dfafa4b2c07c3c717d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402939342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7affaff5df09f269e2c763129fead5401667345bddf55af76af53bca21f3785`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629f11a811d39fc28e5239134c97ea55c85a48c2d7cf1fca897f7901f58598cf`  
		Last Modified: Fri, 23 Feb 2024 18:51:51 GMT  
		Size: 252.0 MB (252013740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ed6523c43ccb627c0d083fae31a1d0ee265eac961421160cddad6ca66e80df`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b027f028db2f1e449ca65da35e0b491f3849a2095cd0f413c11dd5b6ddf004`  
		Last Modified: Fri, 23 Feb 2024 18:51:48 GMT  
		Size: 113.2 MB (113194297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:542483488f9e36f25790d585680b9f01c6e5f5a558ca2bd9554f2556ffa9d01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13533276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6fd85ec6701bf436dbbb4acc09908a20f46416cf3b87b12293738d7fef5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:3c3f9da16b2e732eb4973ac6212ffe7a982720cf67dd5f9c5b471254aa82f784`  
		Last Modified: Fri, 23 Feb 2024 18:51:46 GMT  
		Size: 13.5 MB (13512136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da78b8367adc40306aa097f65cef7af1c9c5a50c6e81460a5ceab4baebdffc2`  
		Last Modified: Fri, 23 Feb 2024 18:51:45 GMT  
		Size: 21.1 KB (21140 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:838f09c2b8b1b2e75ad1ed1d37838883a70ed18aaa976b566f3c6f4bb50fff98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394279815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb07ae034f2d3741162226d3a034e847051f363f2747e9534a0b8fa242dac88`
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
# Fri, 23 Feb 2024 15:05:08 GMT
ENV JAVA_HOME=/usr
# Fri, 23 Feb 2024 15:05:08 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=975b79448e4a7e0cd3f729c343149b52d20474fb3505509d638dfde861c9c440 NEO4J_TARBALL=neo4j-community-5.17.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
# Fri, 23 Feb 2024 15:05:08 GMT
COPY ./local-package/* /startup/ # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.17.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Fri, 23 Feb 2024 15:05:08 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 15:05:08 GMT
WORKDIR /var/lib/neo4j
# Fri, 23 Feb 2024 15:05:08 GMT
VOLUME [/data /logs]
# Fri, 23 Feb 2024 15:05:08 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Fri, 23 Feb 2024 15:05:08 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Fri, 23 Feb 2024 15:05:08 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f22b5bba2adcfbf3d1fe3b58c0e98708f3165c717b134ad3b1abdc5413928`  
		Last Modified: Fri, 23 Feb 2024 18:57:41 GMT  
		Size: 245.0 MB (245026908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8082ed98605720bfc5d74724213d88cfc71e1f7e030337215168b9ab2e50c6`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 9.5 KB (9497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1403da0607f1a15dd7c393890e897975497d427e074f08d4cf9a2dccd82ad4e3`  
		Last Modified: Fri, 23 Feb 2024 18:57:38 GMT  
		Size: 113.2 MB (113194325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:17977f5db7668e6191ebaa0caf94076b4502eeba996b3b97b4510a032e7e832f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13426359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a97395fc101c356d96eb8a6c7de6d95048ed127c7b0e0b10eaec1657e18857d`

```dockerfile
```

-	Layers:
	-	`sha256:5e2dcd8bea1b9ad893721c6c33f7cb7943d77678d161cfbe9f822014612921cf`  
		Last Modified: Fri, 23 Feb 2024 18:57:36 GMT  
		Size: 13.4 MB (13405200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da92e4a66e1d194cfdd6ea7195783b4ff0a0ce7df36c033a3b96bc8e57321e1a`  
		Last Modified: Fri, 23 Feb 2024 18:57:35 GMT  
		Size: 21.2 KB (21159 bytes)  
		MIME: application/vnd.in-toto+json
