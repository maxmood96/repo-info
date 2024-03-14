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
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-bullseye`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-bullseye`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi8`

```console
$ docker pull neo4j@sha256:6c9f243fa81510db6aa5505df26a52e7611b76ea84d913c70bda4652051a1a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:23537fc2083d180e5569564ed2797952e2abef56fb3eb91c268ba62859ff0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef15761b982190d9439415b0eb982acba1f6333d839bff7d43d5f3355e53223`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77028486db177a89cb66cf2763d75e58d29427748ca6f508480e69a5ddaedf31`  
		Last Modified: Wed, 13 Mar 2024 19:51:02 GMT  
		Size: 163.6 MB (163561830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77add1502997bbcc5385b65879528dc9a9d9c1b15acefbd01e5d39e39e6abf`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b6ecc0c70706177ae703356b56c46b28e7cfb88e1a0d4702b467269604821`  
		Last Modified: Wed, 13 Mar 2024 19:51:01 GMT  
		Size: 121.1 MB (121113659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e769245f5a01edd4d1b7604e88b8311d22c1a0bae9645dab6a674b4b830aa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2840a45f538e39308878e77b9784ad1627846224b37fe3e1d05be6ac71ac0d0`

```dockerfile
```

-	Layers:
	-	`sha256:747796166085b0847bb698552b72c0126023cca996d7c374b113897a08890ca4`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af28b95315527fd333c1978ba1325a4cd266bda1e53ffd36aabcd1f1cd1c4c9d`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 21.4 KB (21394 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b596e46ad7042157a98747abc9caf3440303be793511459ea168af99e0af7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896561f478c08e96ab4a229d5045817a3aa4c570ca8f9aff2f49c863a794ced`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e8b1702990a5e3913c43625e17a4ac0fd08c829c1db39af4d913cb79eb26f`  
		Last Modified: Wed, 13 Mar 2024 19:58:07 GMT  
		Size: 121.1 MB (121113674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:65df63b45b3aa18ab1854b04a7e9ab8769f0044ba688c2e80bb1a2913c2b6d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6bfe11b32caa5a1c6118b911d9b06dbb1364235ac408c813b2a44526e5823`

```dockerfile
```

-	Layers:
	-	`sha256:7d097f259cb7c097e2a897bdbc6646ad95b51ca0928a482c2996451e361756d6`  
		Last Modified: Wed, 13 Mar 2024 19:58:05 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c24618edb8280ac3cd24095d327710beef60e57344e7ba8225d84b2104ccb2`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-community-ubi9`

```console
$ docker pull neo4j@sha256:13538af1c4025d0b37c48a0faacd4d2ba7f2ae9f424ddcc7c098e3fb1959263d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c717baed9f89995ad01c2ecec25876187e2c1898990cb76cfa9487e02082f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415850039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66573650f78e25ddb34d4ce68f09eaddec4d130e44ea7beca473a71785d1b51`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406ca0abd527c83573c07f9ce0e428083828deda1b5363f037f7b83d632b7994`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 257.0 MB (257005216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670a23b58c2338647617447b2e3870fb9e69900f4e04ece7128ba6805cefe31`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397f457616da9df263526cba72fe0dbda45caac3e0cbe2e69bf838da3addb5`  
		Last Modified: Wed, 13 Mar 2024 19:51:10 GMT  
		Size: 121.1 MB (121113479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b2d9907adca5620fa50fdcdb4a8584e515f41fbc1f1de8ad3bef32e8a3802d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f67baa25690fec61ebde8e331d03c4eeeae0feced180548f1ead0883a619ca`

```dockerfile
```

-	Layers:
	-	`sha256:fc5affdce7f58d29eb96d85a3b8746c7f5f9002c4e2c26769996e655da587a31`  
		Last Modified: Wed, 13 Mar 2024 19:51:07 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c709a3c395b4073e3315c03fcb982b8b52c22ca3eef7c6e651e27cd42c160a56`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:341f3a5aadc0069a742df1a903bcf8008106b86452096fef91866bf66fa6030c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406666010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592987248fc52eea0cddfb922127005aa993278a2bf1ba0950762bdf1ce7a705`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afb49dfe312a015b8f84bff69a471d3f96d98e63a7d284ea7f37ba3895ebcd`  
		Last Modified: Wed, 13 Mar 2024 19:54:56 GMT  
		Size: 121.1 MB (121113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:19727f1614520ef6a49ed526d18cc2179e47e970ec49c62a7c10f3a823812b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae583ff4566cd6515fc2f4a83acbfd12946d7a8a98b355d638204abcc068d69`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c9d172fac036019d2df3fb06bf4035f67c197ebb0bbb1095f4a8fd689b8c7`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5751f4e6c672776ffef60c8d44bf7289a514077fa66fe3cbf22ab0db03b8c1`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise`

```console
$ docker pull neo4j@sha256:36bc7fadb9afec73a2eb4bcfa19844a90bbb6a5957c07db8d1de3caec5b84771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:291c8f54bb68b73893d6b8033284f53a4d7eb6f8735209241a37f275d13b9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb73604ad9fd708f013276b18597e207831d18e14661fb70e54d7905191a5165`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68e5c089844daf9f08460efccfc0561874936190e10b4af31b74c5cdad648`  
		Last Modified: Wed, 13 Mar 2024 19:50:55 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f037a727b88b4f735ce95c33762cb3d044beef4b26093e50d932d18ab8b55`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b19e47a9c78334ceb36d56a8e9df45c497c368a990bb5c64dea11ba27fffff`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8266ce07a566a25dddc5b82565c41f15d92f3b3867fe3583ad7b310c146645`  
		Last Modified: Wed, 13 Mar 2024 19:51:00 GMT  
		Size: 380.8 MB (380843001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:50848cdacb6a5cb9e435d2c80e59afa04b2021b7c1c5195fcc0078494554320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7782abd9c2e9e89f1b2218ebea2d37e7bdd15c19629e9f08c682535a38965a`

```dockerfile
```

-	Layers:
	-	`sha256:7e79e748d787e14fc48dab9645096462fe1949dcdea86193ec5dd1eac7a16144`  
		Last Modified: Wed, 13 Mar 2024 19:50:52 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03b9ab1e275fe75e23c702bea31050b5e48c4865cd9212144dfa5d3d4475bce`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3a54ac46e2711df9a42b4dd1d2d60528b14b2b34844dad2864718610cfa4a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554612849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fb262c0611b2c5928d02e895ec57225bb2834bebb944918448cedc9d5c203c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:2e8069ee70137f9dcf7f4ef1b952b2bec6a4c23760dfcb967593e91b0abf124f`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75506c7aa22e57c2f47b01a544705e63ffa1483382d8a63b150fd69fa857dceb`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fa1249dabf9993c26d71ddf3ab7a48dad02cc7e2da8714ac96e1bfbded688`  
		Last Modified: Wed, 13 Mar 2024 19:53:03 GMT  
		Size: 380.8 MB (380807891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0a1f04ab05dd7afbfa7b9790d8e582fba472a1a7039045b01ead28ef552473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf8f432824b4e848d416af42e855fe3e235d5ff35f24928866ef02199be87`

```dockerfile
```

-	Layers:
	-	`sha256:11879ddd0521286ac33efd2fd80d27f144d507038a48ef5d03888060717b89ce`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eae2cc5909bfc60e5ccee8b43d7ca16e365bd934e1d637e18a263d56e23238c`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:36bc7fadb9afec73a2eb4bcfa19844a90bbb6a5957c07db8d1de3caec5b84771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:291c8f54bb68b73893d6b8033284f53a4d7eb6f8735209241a37f275d13b9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb73604ad9fd708f013276b18597e207831d18e14661fb70e54d7905191a5165`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68e5c089844daf9f08460efccfc0561874936190e10b4af31b74c5cdad648`  
		Last Modified: Wed, 13 Mar 2024 19:50:55 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f037a727b88b4f735ce95c33762cb3d044beef4b26093e50d932d18ab8b55`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b19e47a9c78334ceb36d56a8e9df45c497c368a990bb5c64dea11ba27fffff`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8266ce07a566a25dddc5b82565c41f15d92f3b3867fe3583ad7b310c146645`  
		Last Modified: Wed, 13 Mar 2024 19:51:00 GMT  
		Size: 380.8 MB (380843001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:50848cdacb6a5cb9e435d2c80e59afa04b2021b7c1c5195fcc0078494554320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7782abd9c2e9e89f1b2218ebea2d37e7bdd15c19629e9f08c682535a38965a`

```dockerfile
```

-	Layers:
	-	`sha256:7e79e748d787e14fc48dab9645096462fe1949dcdea86193ec5dd1eac7a16144`  
		Last Modified: Wed, 13 Mar 2024 19:50:52 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03b9ab1e275fe75e23c702bea31050b5e48c4865cd9212144dfa5d3d4475bce`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3a54ac46e2711df9a42b4dd1d2d60528b14b2b34844dad2864718610cfa4a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554612849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fb262c0611b2c5928d02e895ec57225bb2834bebb944918448cedc9d5c203c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:2e8069ee70137f9dcf7f4ef1b952b2bec6a4c23760dfcb967593e91b0abf124f`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75506c7aa22e57c2f47b01a544705e63ffa1483382d8a63b150fd69fa857dceb`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fa1249dabf9993c26d71ddf3ab7a48dad02cc7e2da8714ac96e1bfbded688`  
		Last Modified: Wed, 13 Mar 2024 19:53:03 GMT  
		Size: 380.8 MB (380807891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0a1f04ab05dd7afbfa7b9790d8e582fba472a1a7039045b01ead28ef552473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf8f432824b4e848d416af42e855fe3e235d5ff35f24928866ef02199be87`

```dockerfile
```

-	Layers:
	-	`sha256:11879ddd0521286ac33efd2fd80d27f144d507038a48ef5d03888060717b89ce`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eae2cc5909bfc60e5ccee8b43d7ca16e365bd934e1d637e18a263d56e23238c`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4310ff4980bdf2d3e48af933af75a40bad9d9de04ebfa233ed9ded8e5accea61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:f902808606b9d851e0f845a09d761990ef6c3c77ae36100e62c0a2f57224a0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177880b2cdc2becdf0b4f97816e3a4527dfc99ebe4fa41d3bd353521124fafd6`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b3cdcc0fcc50d4668025f968000c2afed714f46ee20df4ce11ffaa6139f6d9`  
		Last Modified: Wed, 13 Mar 2024 19:51:26 GMT  
		Size: 163.6 MB (163561716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294d2a8bf56f29805f1f8f68a89835294359648b87729df86b37d385593b4209`  
		Last Modified: Wed, 13 Mar 2024 19:51:22 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b967bd37ff3320ff028a96db1aac102e93fd31705ce63b42d3ee7d54d95ea7a6`  
		Last Modified: Wed, 13 Mar 2024 19:51:30 GMT  
		Size: 377.9 MB (377909754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a2ac61620b00ba644d792f0548fc39f220069589e37ebfca766c7a79d0f6b684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c524f7e2d85ebf1564979cc6de053c7c885272163037ab1f51f734a196a3c876`

```dockerfile
```

-	Layers:
	-	`sha256:095dcad2d1443929ceec3b23690b169934827fae9c219f5e0b1d66740a5c86bc`  
		Last Modified: Wed, 13 Mar 2024 19:51:23 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590dc6e12334138d71b0fc50874c79675a5a1610d118daa0c505b4eaaeae052f`  
		Last Modified: Wed, 13 Mar 2024 19:51:23 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b31f58175ee9ea4d607415def49ba100b3049afc5033862b529e98f0cdd02abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03453285a56de6678d11f497b9136de195446a5645d7341ed9d326821fde89a`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3db1a2827e3c72b057d3c6f8fc77649f55b495cf047cf474158db910d1b59e`  
		Last Modified: Wed, 13 Mar 2024 19:59:13 GMT  
		Size: 377.9 MB (377909610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:e88017bb6f9cea037b52be1345a87986027da417145e2e9b520581f387a98392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e75bd3640d8ad74db96e14460fff9ff5d131e366a94474a175a4f28760421b`

```dockerfile
```

-	Layers:
	-	`sha256:8babfb1ed8f1475bbc5ee9655dfca7ca093477b125937b1d7046a37a099ded26`  
		Last Modified: Wed, 13 Mar 2024 19:59:06 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5e04f76a59ff547c12080f11feefc950b726e561dd8d4fd28c5e31365ebd4d`  
		Last Modified: Wed, 13 Mar 2024 19:59:05 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:c625ebec0cc54bddbd9b20825c1fe99cb3910907c09ece604bb53fb2f4a0daed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:d7a84d463b7828f322efc053ac7e05cb5665643e3185b4388750cf5e6bf99229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672646988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5a16a5894c56e2e264ac8331391806daffb40b6d1904f9bee70a75b0fad971`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ff7f30ca3983ba588de9c8bb39d6249f05c72a937ed4a6bb4993a712134cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:15 GMT  
		Size: 257.0 MB (257005929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4897130454eb3efba649314a4bc87cff4299142800979350f9a5913b68f542`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a659939497f65e9c6ba0e5ba1979ee5e9b5a3bba9b20ee9d5d3a00b1a1f388a6`  
		Last Modified: Wed, 13 Mar 2024 19:51:16 GMT  
		Size: 377.9 MB (377909718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8986165b532d2dafb562bdd82e8c7f15a092a9eefb97eb17d9831cd9ce84cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e394f96c0331e083f2088390da6cea69a205dac5c2addfca9af56a85729a318b`

```dockerfile
```

-	Layers:
	-	`sha256:b6371e979dd44facf236abf0540555e0faa423b361db9a49e6f2a911f0f1a81b`  
		Last Modified: Wed, 13 Mar 2024 19:51:13 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4150c2413f9f9a1a0dcd1ddde083669c7bd2f73aeb39b37393c1e0a0b6db053`  
		Last Modified: Wed, 13 Mar 2024 19:51:11 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:469de50fb4138178d2cffb013fc62f72524f26a841c42a814b8d779af84eed9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663462155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2144acdc6adb88f8248251e98f366296ae3bdd71292dcae5695e89486949f8`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16328c2c13fc725904a8cb59fbb37d443dc97acc0c0cd8f0855df2e160e14c85`  
		Last Modified: Wed, 13 Mar 2024 19:56:12 GMT  
		Size: 377.9 MB (377909758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:22740e6aeb760cc0e21b368fc4eff0afcc49b05359d300dc68c9a7b22e6f6055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2faa27c1e6810120846222827a8ebfd8e69ee8215ef02c7e8f1f6bd671a618e`

```dockerfile
```

-	Layers:
	-	`sha256:e12752b901094a5ca78e2b9bb7889c509d0d0c13902a082f9341b1d728b2a571`  
		Last Modified: Wed, 13 Mar 2024 19:56:03 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e6222d2108f569f6e52d47c743941d41f85a412252a62c424cf1c69703e660f`  
		Last Modified: Wed, 13 Mar 2024 19:56:02 GMT  
		Size: 19.8 KB (19784 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi8`

```console
$ docker pull neo4j@sha256:6c9f243fa81510db6aa5505df26a52e7611b76ea84d913c70bda4652051a1a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:23537fc2083d180e5569564ed2797952e2abef56fb3eb91c268ba62859ff0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef15761b982190d9439415b0eb982acba1f6333d839bff7d43d5f3355e53223`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77028486db177a89cb66cf2763d75e58d29427748ca6f508480e69a5ddaedf31`  
		Last Modified: Wed, 13 Mar 2024 19:51:02 GMT  
		Size: 163.6 MB (163561830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77add1502997bbcc5385b65879528dc9a9d9c1b15acefbd01e5d39e39e6abf`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b6ecc0c70706177ae703356b56c46b28e7cfb88e1a0d4702b467269604821`  
		Last Modified: Wed, 13 Mar 2024 19:51:01 GMT  
		Size: 121.1 MB (121113659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e769245f5a01edd4d1b7604e88b8311d22c1a0bae9645dab6a674b4b830aa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2840a45f538e39308878e77b9784ad1627846224b37fe3e1d05be6ac71ac0d0`

```dockerfile
```

-	Layers:
	-	`sha256:747796166085b0847bb698552b72c0126023cca996d7c374b113897a08890ca4`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af28b95315527fd333c1978ba1325a4cd266bda1e53ffd36aabcd1f1cd1c4c9d`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 21.4 KB (21394 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b596e46ad7042157a98747abc9caf3440303be793511459ea168af99e0af7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896561f478c08e96ab4a229d5045817a3aa4c570ca8f9aff2f49c863a794ced`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e8b1702990a5e3913c43625e17a4ac0fd08c829c1db39af4d913cb79eb26f`  
		Last Modified: Wed, 13 Mar 2024 19:58:07 GMT  
		Size: 121.1 MB (121113674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:65df63b45b3aa18ab1854b04a7e9ab8769f0044ba688c2e80bb1a2913c2b6d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6bfe11b32caa5a1c6118b911d9b06dbb1364235ac408c813b2a44526e5823`

```dockerfile
```

-	Layers:
	-	`sha256:7d097f259cb7c097e2a897bdbc6646ad95b51ca0928a482c2996451e361756d6`  
		Last Modified: Wed, 13 Mar 2024 19:58:05 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c24618edb8280ac3cd24095d327710beef60e57344e7ba8225d84b2104ccb2`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5-ubi9`

```console
$ docker pull neo4j@sha256:13538af1c4025d0b37c48a0faacd4d2ba7f2ae9f424ddcc7c098e3fb1959263d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c717baed9f89995ad01c2ecec25876187e2c1898990cb76cfa9487e02082f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415850039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66573650f78e25ddb34d4ce68f09eaddec4d130e44ea7beca473a71785d1b51`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406ca0abd527c83573c07f9ce0e428083828deda1b5363f037f7b83d632b7994`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 257.0 MB (257005216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670a23b58c2338647617447b2e3870fb9e69900f4e04ece7128ba6805cefe31`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397f457616da9df263526cba72fe0dbda45caac3e0cbe2e69bf838da3addb5`  
		Last Modified: Wed, 13 Mar 2024 19:51:10 GMT  
		Size: 121.1 MB (121113479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b2d9907adca5620fa50fdcdb4a8584e515f41fbc1f1de8ad3bef32e8a3802d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f67baa25690fec61ebde8e331d03c4eeeae0feced180548f1ead0883a619ca`

```dockerfile
```

-	Layers:
	-	`sha256:fc5affdce7f58d29eb96d85a3b8746c7f5f9002c4e2c26769996e655da587a31`  
		Last Modified: Wed, 13 Mar 2024 19:51:07 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c709a3c395b4073e3315c03fcb982b8b52c22ca3eef7c6e651e27cd42c160a56`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:341f3a5aadc0069a742df1a903bcf8008106b86452096fef91866bf66fa6030c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406666010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592987248fc52eea0cddfb922127005aa993278a2bf1ba0950762bdf1ce7a705`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afb49dfe312a015b8f84bff69a471d3f96d98e63a7d284ea7f37ba3895ebcd`  
		Last Modified: Wed, 13 Mar 2024 19:54:56 GMT  
		Size: 121.1 MB (121113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:19727f1614520ef6a49ed526d18cc2179e47e970ec49c62a7c10f3a823812b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae583ff4566cd6515fc2f4a83acbfd12946d7a8a98b355d638204abcc068d69`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c9d172fac036019d2df3fb06bf4035f67c197ebb0bbb1095f4a8fd689b8c7`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5751f4e6c672776ffef60c8d44bf7289a514077fa66fe3cbf22ab0db03b8c1`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-bullseye`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-community`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-community-bullseye`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-community-ubi8`

```console
$ docker pull neo4j@sha256:6c9f243fa81510db6aa5505df26a52e7611b76ea84d913c70bda4652051a1a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:23537fc2083d180e5569564ed2797952e2abef56fb3eb91c268ba62859ff0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef15761b982190d9439415b0eb982acba1f6333d839bff7d43d5f3355e53223`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77028486db177a89cb66cf2763d75e58d29427748ca6f508480e69a5ddaedf31`  
		Last Modified: Wed, 13 Mar 2024 19:51:02 GMT  
		Size: 163.6 MB (163561830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77add1502997bbcc5385b65879528dc9a9d9c1b15acefbd01e5d39e39e6abf`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b6ecc0c70706177ae703356b56c46b28e7cfb88e1a0d4702b467269604821`  
		Last Modified: Wed, 13 Mar 2024 19:51:01 GMT  
		Size: 121.1 MB (121113659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e769245f5a01edd4d1b7604e88b8311d22c1a0bae9645dab6a674b4b830aa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2840a45f538e39308878e77b9784ad1627846224b37fe3e1d05be6ac71ac0d0`

```dockerfile
```

-	Layers:
	-	`sha256:747796166085b0847bb698552b72c0126023cca996d7c374b113897a08890ca4`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af28b95315527fd333c1978ba1325a4cd266bda1e53ffd36aabcd1f1cd1c4c9d`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 21.4 KB (21394 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b596e46ad7042157a98747abc9caf3440303be793511459ea168af99e0af7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896561f478c08e96ab4a229d5045817a3aa4c570ca8f9aff2f49c863a794ced`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e8b1702990a5e3913c43625e17a4ac0fd08c829c1db39af4d913cb79eb26f`  
		Last Modified: Wed, 13 Mar 2024 19:58:07 GMT  
		Size: 121.1 MB (121113674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:65df63b45b3aa18ab1854b04a7e9ab8769f0044ba688c2e80bb1a2913c2b6d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6bfe11b32caa5a1c6118b911d9b06dbb1364235ac408c813b2a44526e5823`

```dockerfile
```

-	Layers:
	-	`sha256:7d097f259cb7c097e2a897bdbc6646ad95b51ca0928a482c2996451e361756d6`  
		Last Modified: Wed, 13 Mar 2024 19:58:05 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c24618edb8280ac3cd24095d327710beef60e57344e7ba8225d84b2104ccb2`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-community-ubi9`

```console
$ docker pull neo4j@sha256:13538af1c4025d0b37c48a0faacd4d2ba7f2ae9f424ddcc7c098e3fb1959263d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c717baed9f89995ad01c2ecec25876187e2c1898990cb76cfa9487e02082f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415850039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66573650f78e25ddb34d4ce68f09eaddec4d130e44ea7beca473a71785d1b51`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406ca0abd527c83573c07f9ce0e428083828deda1b5363f037f7b83d632b7994`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 257.0 MB (257005216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670a23b58c2338647617447b2e3870fb9e69900f4e04ece7128ba6805cefe31`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397f457616da9df263526cba72fe0dbda45caac3e0cbe2e69bf838da3addb5`  
		Last Modified: Wed, 13 Mar 2024 19:51:10 GMT  
		Size: 121.1 MB (121113479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b2d9907adca5620fa50fdcdb4a8584e515f41fbc1f1de8ad3bef32e8a3802d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f67baa25690fec61ebde8e331d03c4eeeae0feced180548f1ead0883a619ca`

```dockerfile
```

-	Layers:
	-	`sha256:fc5affdce7f58d29eb96d85a3b8746c7f5f9002c4e2c26769996e655da587a31`  
		Last Modified: Wed, 13 Mar 2024 19:51:07 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c709a3c395b4073e3315c03fcb982b8b52c22ca3eef7c6e651e27cd42c160a56`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:341f3a5aadc0069a742df1a903bcf8008106b86452096fef91866bf66fa6030c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406666010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592987248fc52eea0cddfb922127005aa993278a2bf1ba0950762bdf1ce7a705`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afb49dfe312a015b8f84bff69a471d3f96d98e63a7d284ea7f37ba3895ebcd`  
		Last Modified: Wed, 13 Mar 2024 19:54:56 GMT  
		Size: 121.1 MB (121113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:19727f1614520ef6a49ed526d18cc2179e47e970ec49c62a7c10f3a823812b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae583ff4566cd6515fc2f4a83acbfd12946d7a8a98b355d638204abcc068d69`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c9d172fac036019d2df3fb06bf4035f67c197ebb0bbb1095f4a8fd689b8c7`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5751f4e6c672776ffef60c8d44bf7289a514077fa66fe3cbf22ab0db03b8c1`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-enterprise`

```console
$ docker pull neo4j@sha256:36bc7fadb9afec73a2eb4bcfa19844a90bbb6a5957c07db8d1de3caec5b84771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:291c8f54bb68b73893d6b8033284f53a4d7eb6f8735209241a37f275d13b9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb73604ad9fd708f013276b18597e207831d18e14661fb70e54d7905191a5165`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68e5c089844daf9f08460efccfc0561874936190e10b4af31b74c5cdad648`  
		Last Modified: Wed, 13 Mar 2024 19:50:55 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f037a727b88b4f735ce95c33762cb3d044beef4b26093e50d932d18ab8b55`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b19e47a9c78334ceb36d56a8e9df45c497c368a990bb5c64dea11ba27fffff`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8266ce07a566a25dddc5b82565c41f15d92f3b3867fe3583ad7b310c146645`  
		Last Modified: Wed, 13 Mar 2024 19:51:00 GMT  
		Size: 380.8 MB (380843001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:50848cdacb6a5cb9e435d2c80e59afa04b2021b7c1c5195fcc0078494554320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7782abd9c2e9e89f1b2218ebea2d37e7bdd15c19629e9f08c682535a38965a`

```dockerfile
```

-	Layers:
	-	`sha256:7e79e748d787e14fc48dab9645096462fe1949dcdea86193ec5dd1eac7a16144`  
		Last Modified: Wed, 13 Mar 2024 19:50:52 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03b9ab1e275fe75e23c702bea31050b5e48c4865cd9212144dfa5d3d4475bce`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3a54ac46e2711df9a42b4dd1d2d60528b14b2b34844dad2864718610cfa4a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554612849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fb262c0611b2c5928d02e895ec57225bb2834bebb944918448cedc9d5c203c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:2e8069ee70137f9dcf7f4ef1b952b2bec6a4c23760dfcb967593e91b0abf124f`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75506c7aa22e57c2f47b01a544705e63ffa1483382d8a63b150fd69fa857dceb`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fa1249dabf9993c26d71ddf3ab7a48dad02cc7e2da8714ac96e1bfbded688`  
		Last Modified: Wed, 13 Mar 2024 19:53:03 GMT  
		Size: 380.8 MB (380807891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0a1f04ab05dd7afbfa7b9790d8e582fba472a1a7039045b01ead28ef552473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf8f432824b4e848d416af42e855fe3e235d5ff35f24928866ef02199be87`

```dockerfile
```

-	Layers:
	-	`sha256:11879ddd0521286ac33efd2fd80d27f144d507038a48ef5d03888060717b89ce`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eae2cc5909bfc60e5ccee8b43d7ca16e365bd934e1d637e18a263d56e23238c`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:36bc7fadb9afec73a2eb4bcfa19844a90bbb6a5957c07db8d1de3caec5b84771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:291c8f54bb68b73893d6b8033284f53a4d7eb6f8735209241a37f275d13b9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb73604ad9fd708f013276b18597e207831d18e14661fb70e54d7905191a5165`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68e5c089844daf9f08460efccfc0561874936190e10b4af31b74c5cdad648`  
		Last Modified: Wed, 13 Mar 2024 19:50:55 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f037a727b88b4f735ce95c33762cb3d044beef4b26093e50d932d18ab8b55`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b19e47a9c78334ceb36d56a8e9df45c497c368a990bb5c64dea11ba27fffff`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8266ce07a566a25dddc5b82565c41f15d92f3b3867fe3583ad7b310c146645`  
		Last Modified: Wed, 13 Mar 2024 19:51:00 GMT  
		Size: 380.8 MB (380843001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:50848cdacb6a5cb9e435d2c80e59afa04b2021b7c1c5195fcc0078494554320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7782abd9c2e9e89f1b2218ebea2d37e7bdd15c19629e9f08c682535a38965a`

```dockerfile
```

-	Layers:
	-	`sha256:7e79e748d787e14fc48dab9645096462fe1949dcdea86193ec5dd1eac7a16144`  
		Last Modified: Wed, 13 Mar 2024 19:50:52 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03b9ab1e275fe75e23c702bea31050b5e48c4865cd9212144dfa5d3d4475bce`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3a54ac46e2711df9a42b4dd1d2d60528b14b2b34844dad2864718610cfa4a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554612849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fb262c0611b2c5928d02e895ec57225bb2834bebb944918448cedc9d5c203c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:2e8069ee70137f9dcf7f4ef1b952b2bec6a4c23760dfcb967593e91b0abf124f`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75506c7aa22e57c2f47b01a544705e63ffa1483382d8a63b150fd69fa857dceb`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fa1249dabf9993c26d71ddf3ab7a48dad02cc7e2da8714ac96e1bfbded688`  
		Last Modified: Wed, 13 Mar 2024 19:53:03 GMT  
		Size: 380.8 MB (380807891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0a1f04ab05dd7afbfa7b9790d8e582fba472a1a7039045b01ead28ef552473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf8f432824b4e848d416af42e855fe3e235d5ff35f24928866ef02199be87`

```dockerfile
```

-	Layers:
	-	`sha256:11879ddd0521286ac33efd2fd80d27f144d507038a48ef5d03888060717b89ce`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eae2cc5909bfc60e5ccee8b43d7ca16e365bd934e1d637e18a263d56e23238c`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4310ff4980bdf2d3e48af933af75a40bad9d9de04ebfa233ed9ded8e5accea61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:f902808606b9d851e0f845a09d761990ef6c3c77ae36100e62c0a2f57224a0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177880b2cdc2becdf0b4f97816e3a4527dfc99ebe4fa41d3bd353521124fafd6`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b3cdcc0fcc50d4668025f968000c2afed714f46ee20df4ce11ffaa6139f6d9`  
		Last Modified: Wed, 13 Mar 2024 19:51:26 GMT  
		Size: 163.6 MB (163561716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294d2a8bf56f29805f1f8f68a89835294359648b87729df86b37d385593b4209`  
		Last Modified: Wed, 13 Mar 2024 19:51:22 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b967bd37ff3320ff028a96db1aac102e93fd31705ce63b42d3ee7d54d95ea7a6`  
		Last Modified: Wed, 13 Mar 2024 19:51:30 GMT  
		Size: 377.9 MB (377909754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a2ac61620b00ba644d792f0548fc39f220069589e37ebfca766c7a79d0f6b684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c524f7e2d85ebf1564979cc6de053c7c885272163037ab1f51f734a196a3c876`

```dockerfile
```

-	Layers:
	-	`sha256:095dcad2d1443929ceec3b23690b169934827fae9c219f5e0b1d66740a5c86bc`  
		Last Modified: Wed, 13 Mar 2024 19:51:23 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590dc6e12334138d71b0fc50874c79675a5a1610d118daa0c505b4eaaeae052f`  
		Last Modified: Wed, 13 Mar 2024 19:51:23 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b31f58175ee9ea4d607415def49ba100b3049afc5033862b529e98f0cdd02abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03453285a56de6678d11f497b9136de195446a5645d7341ed9d326821fde89a`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3db1a2827e3c72b057d3c6f8fc77649f55b495cf047cf474158db910d1b59e`  
		Last Modified: Wed, 13 Mar 2024 19:59:13 GMT  
		Size: 377.9 MB (377909610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:e88017bb6f9cea037b52be1345a87986027da417145e2e9b520581f387a98392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e75bd3640d8ad74db96e14460fff9ff5d131e366a94474a175a4f28760421b`

```dockerfile
```

-	Layers:
	-	`sha256:8babfb1ed8f1475bbc5ee9655dfca7ca093477b125937b1d7046a37a099ded26`  
		Last Modified: Wed, 13 Mar 2024 19:59:06 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5e04f76a59ff547c12080f11feefc950b726e561dd8d4fd28c5e31365ebd4d`  
		Last Modified: Wed, 13 Mar 2024 19:59:05 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:c625ebec0cc54bddbd9b20825c1fe99cb3910907c09ece604bb53fb2f4a0daed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:d7a84d463b7828f322efc053ac7e05cb5665643e3185b4388750cf5e6bf99229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672646988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5a16a5894c56e2e264ac8331391806daffb40b6d1904f9bee70a75b0fad971`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ff7f30ca3983ba588de9c8bb39d6249f05c72a937ed4a6bb4993a712134cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:15 GMT  
		Size: 257.0 MB (257005929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4897130454eb3efba649314a4bc87cff4299142800979350f9a5913b68f542`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a659939497f65e9c6ba0e5ba1979ee5e9b5a3bba9b20ee9d5d3a00b1a1f388a6`  
		Last Modified: Wed, 13 Mar 2024 19:51:16 GMT  
		Size: 377.9 MB (377909718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8986165b532d2dafb562bdd82e8c7f15a092a9eefb97eb17d9831cd9ce84cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e394f96c0331e083f2088390da6cea69a205dac5c2addfca9af56a85729a318b`

```dockerfile
```

-	Layers:
	-	`sha256:b6371e979dd44facf236abf0540555e0faa423b361db9a49e6f2a911f0f1a81b`  
		Last Modified: Wed, 13 Mar 2024 19:51:13 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4150c2413f9f9a1a0dcd1ddde083669c7bd2f73aeb39b37393c1e0a0b6db053`  
		Last Modified: Wed, 13 Mar 2024 19:51:11 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:469de50fb4138178d2cffb013fc62f72524f26a841c42a814b8d779af84eed9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663462155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2144acdc6adb88f8248251e98f366296ae3bdd71292dcae5695e89486949f8`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16328c2c13fc725904a8cb59fbb37d443dc97acc0c0cd8f0855df2e160e14c85`  
		Last Modified: Wed, 13 Mar 2024 19:56:12 GMT  
		Size: 377.9 MB (377909758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:22740e6aeb760cc0e21b368fc4eff0afcc49b05359d300dc68c9a7b22e6f6055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2faa27c1e6810120846222827a8ebfd8e69ee8215ef02c7e8f1f6bd671a618e`

```dockerfile
```

-	Layers:
	-	`sha256:e12752b901094a5ca78e2b9bb7889c509d0d0c13902a082f9341b1d728b2a571`  
		Last Modified: Wed, 13 Mar 2024 19:56:03 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e6222d2108f569f6e52d47c743941d41f85a412252a62c424cf1c69703e660f`  
		Last Modified: Wed, 13 Mar 2024 19:56:02 GMT  
		Size: 19.8 KB (19784 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-ubi8`

```console
$ docker pull neo4j@sha256:6c9f243fa81510db6aa5505df26a52e7611b76ea84d913c70bda4652051a1a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:23537fc2083d180e5569564ed2797952e2abef56fb3eb91c268ba62859ff0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef15761b982190d9439415b0eb982acba1f6333d839bff7d43d5f3355e53223`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77028486db177a89cb66cf2763d75e58d29427748ca6f508480e69a5ddaedf31`  
		Last Modified: Wed, 13 Mar 2024 19:51:02 GMT  
		Size: 163.6 MB (163561830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77add1502997bbcc5385b65879528dc9a9d9c1b15acefbd01e5d39e39e6abf`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b6ecc0c70706177ae703356b56c46b28e7cfb88e1a0d4702b467269604821`  
		Last Modified: Wed, 13 Mar 2024 19:51:01 GMT  
		Size: 121.1 MB (121113659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e769245f5a01edd4d1b7604e88b8311d22c1a0bae9645dab6a674b4b830aa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2840a45f538e39308878e77b9784ad1627846224b37fe3e1d05be6ac71ac0d0`

```dockerfile
```

-	Layers:
	-	`sha256:747796166085b0847bb698552b72c0126023cca996d7c374b113897a08890ca4`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af28b95315527fd333c1978ba1325a4cd266bda1e53ffd36aabcd1f1cd1c4c9d`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 21.4 KB (21394 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b596e46ad7042157a98747abc9caf3440303be793511459ea168af99e0af7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896561f478c08e96ab4a229d5045817a3aa4c570ca8f9aff2f49c863a794ced`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e8b1702990a5e3913c43625e17a4ac0fd08c829c1db39af4d913cb79eb26f`  
		Last Modified: Wed, 13 Mar 2024 19:58:07 GMT  
		Size: 121.1 MB (121113674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:65df63b45b3aa18ab1854b04a7e9ab8769f0044ba688c2e80bb1a2913c2b6d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6bfe11b32caa5a1c6118b911d9b06dbb1364235ac408c813b2a44526e5823`

```dockerfile
```

-	Layers:
	-	`sha256:7d097f259cb7c097e2a897bdbc6646ad95b51ca0928a482c2996451e361756d6`  
		Last Modified: Wed, 13 Mar 2024 19:58:05 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c24618edb8280ac3cd24095d327710beef60e57344e7ba8225d84b2104ccb2`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18-ubi9`

```console
$ docker pull neo4j@sha256:13538af1c4025d0b37c48a0faacd4d2ba7f2ae9f424ddcc7c098e3fb1959263d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c717baed9f89995ad01c2ecec25876187e2c1898990cb76cfa9487e02082f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415850039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66573650f78e25ddb34d4ce68f09eaddec4d130e44ea7beca473a71785d1b51`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406ca0abd527c83573c07f9ce0e428083828deda1b5363f037f7b83d632b7994`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 257.0 MB (257005216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670a23b58c2338647617447b2e3870fb9e69900f4e04ece7128ba6805cefe31`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397f457616da9df263526cba72fe0dbda45caac3e0cbe2e69bf838da3addb5`  
		Last Modified: Wed, 13 Mar 2024 19:51:10 GMT  
		Size: 121.1 MB (121113479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b2d9907adca5620fa50fdcdb4a8584e515f41fbc1f1de8ad3bef32e8a3802d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f67baa25690fec61ebde8e331d03c4eeeae0feced180548f1ead0883a619ca`

```dockerfile
```

-	Layers:
	-	`sha256:fc5affdce7f58d29eb96d85a3b8746c7f5f9002c4e2c26769996e655da587a31`  
		Last Modified: Wed, 13 Mar 2024 19:51:07 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c709a3c395b4073e3315c03fcb982b8b52c22ca3eef7c6e651e27cd42c160a56`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:341f3a5aadc0069a742df1a903bcf8008106b86452096fef91866bf66fa6030c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406666010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592987248fc52eea0cddfb922127005aa993278a2bf1ba0950762bdf1ce7a705`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afb49dfe312a015b8f84bff69a471d3f96d98e63a7d284ea7f37ba3895ebcd`  
		Last Modified: Wed, 13 Mar 2024 19:54:56 GMT  
		Size: 121.1 MB (121113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:19727f1614520ef6a49ed526d18cc2179e47e970ec49c62a7c10f3a823812b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae583ff4566cd6515fc2f4a83acbfd12946d7a8a98b355d638204abcc068d69`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c9d172fac036019d2df3fb06bf4035f67c197ebb0bbb1095f4a8fd689b8c7`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5751f4e6c672776ffef60c8d44bf7289a514077fa66fe3cbf22ab0db03b8c1`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-bullseye`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-community`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-community` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-community-bullseye`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-community-ubi8`

```console
$ docker pull neo4j@sha256:6c9f243fa81510db6aa5505df26a52e7611b76ea84d913c70bda4652051a1a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:23537fc2083d180e5569564ed2797952e2abef56fb3eb91c268ba62859ff0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef15761b982190d9439415b0eb982acba1f6333d839bff7d43d5f3355e53223`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77028486db177a89cb66cf2763d75e58d29427748ca6f508480e69a5ddaedf31`  
		Last Modified: Wed, 13 Mar 2024 19:51:02 GMT  
		Size: 163.6 MB (163561830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77add1502997bbcc5385b65879528dc9a9d9c1b15acefbd01e5d39e39e6abf`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b6ecc0c70706177ae703356b56c46b28e7cfb88e1a0d4702b467269604821`  
		Last Modified: Wed, 13 Mar 2024 19:51:01 GMT  
		Size: 121.1 MB (121113659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e769245f5a01edd4d1b7604e88b8311d22c1a0bae9645dab6a674b4b830aa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2840a45f538e39308878e77b9784ad1627846224b37fe3e1d05be6ac71ac0d0`

```dockerfile
```

-	Layers:
	-	`sha256:747796166085b0847bb698552b72c0126023cca996d7c374b113897a08890ca4`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af28b95315527fd333c1978ba1325a4cd266bda1e53ffd36aabcd1f1cd1c4c9d`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 21.4 KB (21394 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b596e46ad7042157a98747abc9caf3440303be793511459ea168af99e0af7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896561f478c08e96ab4a229d5045817a3aa4c570ca8f9aff2f49c863a794ced`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e8b1702990a5e3913c43625e17a4ac0fd08c829c1db39af4d913cb79eb26f`  
		Last Modified: Wed, 13 Mar 2024 19:58:07 GMT  
		Size: 121.1 MB (121113674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:65df63b45b3aa18ab1854b04a7e9ab8769f0044ba688c2e80bb1a2913c2b6d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6bfe11b32caa5a1c6118b911d9b06dbb1364235ac408c813b2a44526e5823`

```dockerfile
```

-	Layers:
	-	`sha256:7d097f259cb7c097e2a897bdbc6646ad95b51ca0928a482c2996451e361756d6`  
		Last Modified: Wed, 13 Mar 2024 19:58:05 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c24618edb8280ac3cd24095d327710beef60e57344e7ba8225d84b2104ccb2`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-community-ubi9`

```console
$ docker pull neo4j@sha256:13538af1c4025d0b37c48a0faacd4d2ba7f2ae9f424ddcc7c098e3fb1959263d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c717baed9f89995ad01c2ecec25876187e2c1898990cb76cfa9487e02082f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415850039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66573650f78e25ddb34d4ce68f09eaddec4d130e44ea7beca473a71785d1b51`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406ca0abd527c83573c07f9ce0e428083828deda1b5363f037f7b83d632b7994`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 257.0 MB (257005216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670a23b58c2338647617447b2e3870fb9e69900f4e04ece7128ba6805cefe31`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397f457616da9df263526cba72fe0dbda45caac3e0cbe2e69bf838da3addb5`  
		Last Modified: Wed, 13 Mar 2024 19:51:10 GMT  
		Size: 121.1 MB (121113479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b2d9907adca5620fa50fdcdb4a8584e515f41fbc1f1de8ad3bef32e8a3802d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f67baa25690fec61ebde8e331d03c4eeeae0feced180548f1ead0883a619ca`

```dockerfile
```

-	Layers:
	-	`sha256:fc5affdce7f58d29eb96d85a3b8746c7f5f9002c4e2c26769996e655da587a31`  
		Last Modified: Wed, 13 Mar 2024 19:51:07 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c709a3c395b4073e3315c03fcb982b8b52c22ca3eef7c6e651e27cd42c160a56`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:341f3a5aadc0069a742df1a903bcf8008106b86452096fef91866bf66fa6030c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406666010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592987248fc52eea0cddfb922127005aa993278a2bf1ba0950762bdf1ce7a705`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afb49dfe312a015b8f84bff69a471d3f96d98e63a7d284ea7f37ba3895ebcd`  
		Last Modified: Wed, 13 Mar 2024 19:54:56 GMT  
		Size: 121.1 MB (121113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:19727f1614520ef6a49ed526d18cc2179e47e970ec49c62a7c10f3a823812b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae583ff4566cd6515fc2f4a83acbfd12946d7a8a98b355d638204abcc068d69`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c9d172fac036019d2df3fb06bf4035f67c197ebb0bbb1095f4a8fd689b8c7`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5751f4e6c672776ffef60c8d44bf7289a514077fa66fe3cbf22ab0db03b8c1`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-enterprise`

```console
$ docker pull neo4j@sha256:36bc7fadb9afec73a2eb4bcfa19844a90bbb6a5957c07db8d1de3caec5b84771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:291c8f54bb68b73893d6b8033284f53a4d7eb6f8735209241a37f275d13b9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb73604ad9fd708f013276b18597e207831d18e14661fb70e54d7905191a5165`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68e5c089844daf9f08460efccfc0561874936190e10b4af31b74c5cdad648`  
		Last Modified: Wed, 13 Mar 2024 19:50:55 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f037a727b88b4f735ce95c33762cb3d044beef4b26093e50d932d18ab8b55`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b19e47a9c78334ceb36d56a8e9df45c497c368a990bb5c64dea11ba27fffff`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8266ce07a566a25dddc5b82565c41f15d92f3b3867fe3583ad7b310c146645`  
		Last Modified: Wed, 13 Mar 2024 19:51:00 GMT  
		Size: 380.8 MB (380843001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:50848cdacb6a5cb9e435d2c80e59afa04b2021b7c1c5195fcc0078494554320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7782abd9c2e9e89f1b2218ebea2d37e7bdd15c19629e9f08c682535a38965a`

```dockerfile
```

-	Layers:
	-	`sha256:7e79e748d787e14fc48dab9645096462fe1949dcdea86193ec5dd1eac7a16144`  
		Last Modified: Wed, 13 Mar 2024 19:50:52 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03b9ab1e275fe75e23c702bea31050b5e48c4865cd9212144dfa5d3d4475bce`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3a54ac46e2711df9a42b4dd1d2d60528b14b2b34844dad2864718610cfa4a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554612849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fb262c0611b2c5928d02e895ec57225bb2834bebb944918448cedc9d5c203c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:2e8069ee70137f9dcf7f4ef1b952b2bec6a4c23760dfcb967593e91b0abf124f`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75506c7aa22e57c2f47b01a544705e63ffa1483382d8a63b150fd69fa857dceb`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fa1249dabf9993c26d71ddf3ab7a48dad02cc7e2da8714ac96e1bfbded688`  
		Last Modified: Wed, 13 Mar 2024 19:53:03 GMT  
		Size: 380.8 MB (380807891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0a1f04ab05dd7afbfa7b9790d8e582fba472a1a7039045b01ead28ef552473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf8f432824b4e848d416af42e855fe3e235d5ff35f24928866ef02199be87`

```dockerfile
```

-	Layers:
	-	`sha256:11879ddd0521286ac33efd2fd80d27f144d507038a48ef5d03888060717b89ce`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eae2cc5909bfc60e5ccee8b43d7ca16e365bd934e1d637e18a263d56e23238c`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-enterprise-bullseye`

```console
$ docker pull neo4j@sha256:36bc7fadb9afec73a2eb4bcfa19844a90bbb6a5957c07db8d1de3caec5b84771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:291c8f54bb68b73893d6b8033284f53a4d7eb6f8735209241a37f275d13b9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb73604ad9fd708f013276b18597e207831d18e14661fb70e54d7905191a5165`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68e5c089844daf9f08460efccfc0561874936190e10b4af31b74c5cdad648`  
		Last Modified: Wed, 13 Mar 2024 19:50:55 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f037a727b88b4f735ce95c33762cb3d044beef4b26093e50d932d18ab8b55`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b19e47a9c78334ceb36d56a8e9df45c497c368a990bb5c64dea11ba27fffff`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8266ce07a566a25dddc5b82565c41f15d92f3b3867fe3583ad7b310c146645`  
		Last Modified: Wed, 13 Mar 2024 19:51:00 GMT  
		Size: 380.8 MB (380843001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:50848cdacb6a5cb9e435d2c80e59afa04b2021b7c1c5195fcc0078494554320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7782abd9c2e9e89f1b2218ebea2d37e7bdd15c19629e9f08c682535a38965a`

```dockerfile
```

-	Layers:
	-	`sha256:7e79e748d787e14fc48dab9645096462fe1949dcdea86193ec5dd1eac7a16144`  
		Last Modified: Wed, 13 Mar 2024 19:50:52 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03b9ab1e275fe75e23c702bea31050b5e48c4865cd9212144dfa5d3d4475bce`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3a54ac46e2711df9a42b4dd1d2d60528b14b2b34844dad2864718610cfa4a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554612849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fb262c0611b2c5928d02e895ec57225bb2834bebb944918448cedc9d5c203c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:2e8069ee70137f9dcf7f4ef1b952b2bec6a4c23760dfcb967593e91b0abf124f`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75506c7aa22e57c2f47b01a544705e63ffa1483382d8a63b150fd69fa857dceb`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fa1249dabf9993c26d71ddf3ab7a48dad02cc7e2da8714ac96e1bfbded688`  
		Last Modified: Wed, 13 Mar 2024 19:53:03 GMT  
		Size: 380.8 MB (380807891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0a1f04ab05dd7afbfa7b9790d8e582fba472a1a7039045b01ead28ef552473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf8f432824b4e848d416af42e855fe3e235d5ff35f24928866ef02199be87`

```dockerfile
```

-	Layers:
	-	`sha256:11879ddd0521286ac33efd2fd80d27f144d507038a48ef5d03888060717b89ce`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eae2cc5909bfc60e5ccee8b43d7ca16e365bd934e1d637e18a263d56e23238c`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4310ff4980bdf2d3e48af933af75a40bad9d9de04ebfa233ed9ded8e5accea61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:f902808606b9d851e0f845a09d761990ef6c3c77ae36100e62c0a2f57224a0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177880b2cdc2becdf0b4f97816e3a4527dfc99ebe4fa41d3bd353521124fafd6`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b3cdcc0fcc50d4668025f968000c2afed714f46ee20df4ce11ffaa6139f6d9`  
		Last Modified: Wed, 13 Mar 2024 19:51:26 GMT  
		Size: 163.6 MB (163561716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294d2a8bf56f29805f1f8f68a89835294359648b87729df86b37d385593b4209`  
		Last Modified: Wed, 13 Mar 2024 19:51:22 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b967bd37ff3320ff028a96db1aac102e93fd31705ce63b42d3ee7d54d95ea7a6`  
		Last Modified: Wed, 13 Mar 2024 19:51:30 GMT  
		Size: 377.9 MB (377909754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a2ac61620b00ba644d792f0548fc39f220069589e37ebfca766c7a79d0f6b684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c524f7e2d85ebf1564979cc6de053c7c885272163037ab1f51f734a196a3c876`

```dockerfile
```

-	Layers:
	-	`sha256:095dcad2d1443929ceec3b23690b169934827fae9c219f5e0b1d66740a5c86bc`  
		Last Modified: Wed, 13 Mar 2024 19:51:23 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590dc6e12334138d71b0fc50874c79675a5a1610d118daa0c505b4eaaeae052f`  
		Last Modified: Wed, 13 Mar 2024 19:51:23 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b31f58175ee9ea4d607415def49ba100b3049afc5033862b529e98f0cdd02abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03453285a56de6678d11f497b9136de195446a5645d7341ed9d326821fde89a`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3db1a2827e3c72b057d3c6f8fc77649f55b495cf047cf474158db910d1b59e`  
		Last Modified: Wed, 13 Mar 2024 19:59:13 GMT  
		Size: 377.9 MB (377909610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:e88017bb6f9cea037b52be1345a87986027da417145e2e9b520581f387a98392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e75bd3640d8ad74db96e14460fff9ff5d131e366a94474a175a4f28760421b`

```dockerfile
```

-	Layers:
	-	`sha256:8babfb1ed8f1475bbc5ee9655dfca7ca093477b125937b1d7046a37a099ded26`  
		Last Modified: Wed, 13 Mar 2024 19:59:06 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5e04f76a59ff547c12080f11feefc950b726e561dd8d4fd28c5e31365ebd4d`  
		Last Modified: Wed, 13 Mar 2024 19:59:05 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-enterprise-ubi9`

```console
$ docker pull neo4j@sha256:c625ebec0cc54bddbd9b20825c1fe99cb3910907c09ece604bb53fb2f4a0daed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:d7a84d463b7828f322efc053ac7e05cb5665643e3185b4388750cf5e6bf99229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672646988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5a16a5894c56e2e264ac8331391806daffb40b6d1904f9bee70a75b0fad971`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ff7f30ca3983ba588de9c8bb39d6249f05c72a937ed4a6bb4993a712134cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:15 GMT  
		Size: 257.0 MB (257005929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4897130454eb3efba649314a4bc87cff4299142800979350f9a5913b68f542`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a659939497f65e9c6ba0e5ba1979ee5e9b5a3bba9b20ee9d5d3a00b1a1f388a6`  
		Last Modified: Wed, 13 Mar 2024 19:51:16 GMT  
		Size: 377.9 MB (377909718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8986165b532d2dafb562bdd82e8c7f15a092a9eefb97eb17d9831cd9ce84cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e394f96c0331e083f2088390da6cea69a205dac5c2addfca9af56a85729a318b`

```dockerfile
```

-	Layers:
	-	`sha256:b6371e979dd44facf236abf0540555e0faa423b361db9a49e6f2a911f0f1a81b`  
		Last Modified: Wed, 13 Mar 2024 19:51:13 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4150c2413f9f9a1a0dcd1ddde083669c7bd2f73aeb39b37393c1e0a0b6db053`  
		Last Modified: Wed, 13 Mar 2024 19:51:11 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:469de50fb4138178d2cffb013fc62f72524f26a841c42a814b8d779af84eed9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663462155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2144acdc6adb88f8248251e98f366296ae3bdd71292dcae5695e89486949f8`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16328c2c13fc725904a8cb59fbb37d443dc97acc0c0cd8f0855df2e160e14c85`  
		Last Modified: Wed, 13 Mar 2024 19:56:12 GMT  
		Size: 377.9 MB (377909758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:22740e6aeb760cc0e21b368fc4eff0afcc49b05359d300dc68c9a7b22e6f6055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2faa27c1e6810120846222827a8ebfd8e69ee8215ef02c7e8f1f6bd671a618e`

```dockerfile
```

-	Layers:
	-	`sha256:e12752b901094a5ca78e2b9bb7889c509d0d0c13902a082f9341b1d728b2a571`  
		Last Modified: Wed, 13 Mar 2024 19:56:03 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e6222d2108f569f6e52d47c743941d41f85a412252a62c424cf1c69703e660f`  
		Last Modified: Wed, 13 Mar 2024 19:56:02 GMT  
		Size: 19.8 KB (19784 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-ubi8`

```console
$ docker pull neo4j@sha256:6c9f243fa81510db6aa5505df26a52e7611b76ea84d913c70bda4652051a1a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:23537fc2083d180e5569564ed2797952e2abef56fb3eb91c268ba62859ff0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef15761b982190d9439415b0eb982acba1f6333d839bff7d43d5f3355e53223`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77028486db177a89cb66cf2763d75e58d29427748ca6f508480e69a5ddaedf31`  
		Last Modified: Wed, 13 Mar 2024 19:51:02 GMT  
		Size: 163.6 MB (163561830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77add1502997bbcc5385b65879528dc9a9d9c1b15acefbd01e5d39e39e6abf`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b6ecc0c70706177ae703356b56c46b28e7cfb88e1a0d4702b467269604821`  
		Last Modified: Wed, 13 Mar 2024 19:51:01 GMT  
		Size: 121.1 MB (121113659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e769245f5a01edd4d1b7604e88b8311d22c1a0bae9645dab6a674b4b830aa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2840a45f538e39308878e77b9784ad1627846224b37fe3e1d05be6ac71ac0d0`

```dockerfile
```

-	Layers:
	-	`sha256:747796166085b0847bb698552b72c0126023cca996d7c374b113897a08890ca4`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af28b95315527fd333c1978ba1325a4cd266bda1e53ffd36aabcd1f1cd1c4c9d`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 21.4 KB (21394 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b596e46ad7042157a98747abc9caf3440303be793511459ea168af99e0af7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896561f478c08e96ab4a229d5045817a3aa4c570ca8f9aff2f49c863a794ced`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e8b1702990a5e3913c43625e17a4ac0fd08c829c1db39af4d913cb79eb26f`  
		Last Modified: Wed, 13 Mar 2024 19:58:07 GMT  
		Size: 121.1 MB (121113674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:65df63b45b3aa18ab1854b04a7e9ab8769f0044ba688c2e80bb1a2913c2b6d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6bfe11b32caa5a1c6118b911d9b06dbb1364235ac408c813b2a44526e5823`

```dockerfile
```

-	Layers:
	-	`sha256:7d097f259cb7c097e2a897bdbc6646ad95b51ca0928a482c2996451e361756d6`  
		Last Modified: Wed, 13 Mar 2024 19:58:05 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c24618edb8280ac3cd24095d327710beef60e57344e7ba8225d84b2104ccb2`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:5.18.0-ubi9`

```console
$ docker pull neo4j@sha256:13538af1c4025d0b37c48a0faacd4d2ba7f2ae9f424ddcc7c098e3fb1959263d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:5.18.0-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c717baed9f89995ad01c2ecec25876187e2c1898990cb76cfa9487e02082f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415850039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66573650f78e25ddb34d4ce68f09eaddec4d130e44ea7beca473a71785d1b51`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406ca0abd527c83573c07f9ce0e428083828deda1b5363f037f7b83d632b7994`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 257.0 MB (257005216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670a23b58c2338647617447b2e3870fb9e69900f4e04ece7128ba6805cefe31`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397f457616da9df263526cba72fe0dbda45caac3e0cbe2e69bf838da3addb5`  
		Last Modified: Wed, 13 Mar 2024 19:51:10 GMT  
		Size: 121.1 MB (121113479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b2d9907adca5620fa50fdcdb4a8584e515f41fbc1f1de8ad3bef32e8a3802d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f67baa25690fec61ebde8e331d03c4eeeae0feced180548f1ead0883a619ca`

```dockerfile
```

-	Layers:
	-	`sha256:fc5affdce7f58d29eb96d85a3b8746c7f5f9002c4e2c26769996e655da587a31`  
		Last Modified: Wed, 13 Mar 2024 19:51:07 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c709a3c395b4073e3315c03fcb982b8b52c22ca3eef7c6e651e27cd42c160a56`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:5.18.0-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:341f3a5aadc0069a742df1a903bcf8008106b86452096fef91866bf66fa6030c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406666010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592987248fc52eea0cddfb922127005aa993278a2bf1ba0950762bdf1ce7a705`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afb49dfe312a015b8f84bff69a471d3f96d98e63a7d284ea7f37ba3895ebcd`  
		Last Modified: Wed, 13 Mar 2024 19:54:56 GMT  
		Size: 121.1 MB (121113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:5.18.0-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:19727f1614520ef6a49ed526d18cc2179e47e970ec49c62a7c10f3a823812b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae583ff4566cd6515fc2f4a83acbfd12946d7a8a98b355d638204abcc068d69`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c9d172fac036019d2df3fb06bf4035f67c197ebb0bbb1095f4a8fd689b8c7`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5751f4e6c672776ffef60c8d44bf7289a514077fa66fe3cbf22ab0db03b8c1`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:bullseye`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-bullseye`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi8`

```console
$ docker pull neo4j@sha256:6c9f243fa81510db6aa5505df26a52e7611b76ea84d913c70bda4652051a1a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:23537fc2083d180e5569564ed2797952e2abef56fb3eb91c268ba62859ff0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef15761b982190d9439415b0eb982acba1f6333d839bff7d43d5f3355e53223`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77028486db177a89cb66cf2763d75e58d29427748ca6f508480e69a5ddaedf31`  
		Last Modified: Wed, 13 Mar 2024 19:51:02 GMT  
		Size: 163.6 MB (163561830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77add1502997bbcc5385b65879528dc9a9d9c1b15acefbd01e5d39e39e6abf`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b6ecc0c70706177ae703356b56c46b28e7cfb88e1a0d4702b467269604821`  
		Last Modified: Wed, 13 Mar 2024 19:51:01 GMT  
		Size: 121.1 MB (121113659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e769245f5a01edd4d1b7604e88b8311d22c1a0bae9645dab6a674b4b830aa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2840a45f538e39308878e77b9784ad1627846224b37fe3e1d05be6ac71ac0d0`

```dockerfile
```

-	Layers:
	-	`sha256:747796166085b0847bb698552b72c0126023cca996d7c374b113897a08890ca4`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af28b95315527fd333c1978ba1325a4cd266bda1e53ffd36aabcd1f1cd1c4c9d`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 21.4 KB (21394 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b596e46ad7042157a98747abc9caf3440303be793511459ea168af99e0af7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896561f478c08e96ab4a229d5045817a3aa4c570ca8f9aff2f49c863a794ced`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e8b1702990a5e3913c43625e17a4ac0fd08c829c1db39af4d913cb79eb26f`  
		Last Modified: Wed, 13 Mar 2024 19:58:07 GMT  
		Size: 121.1 MB (121113674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:65df63b45b3aa18ab1854b04a7e9ab8769f0044ba688c2e80bb1a2913c2b6d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6bfe11b32caa5a1c6118b911d9b06dbb1364235ac408c813b2a44526e5823`

```dockerfile
```

-	Layers:
	-	`sha256:7d097f259cb7c097e2a897bdbc6646ad95b51ca0928a482c2996451e361756d6`  
		Last Modified: Wed, 13 Mar 2024 19:58:05 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c24618edb8280ac3cd24095d327710beef60e57344e7ba8225d84b2104ccb2`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:community-ubi9`

```console
$ docker pull neo4j@sha256:13538af1c4025d0b37c48a0faacd4d2ba7f2ae9f424ddcc7c098e3fb1959263d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:community-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c717baed9f89995ad01c2ecec25876187e2c1898990cb76cfa9487e02082f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415850039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66573650f78e25ddb34d4ce68f09eaddec4d130e44ea7beca473a71785d1b51`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406ca0abd527c83573c07f9ce0e428083828deda1b5363f037f7b83d632b7994`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 257.0 MB (257005216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670a23b58c2338647617447b2e3870fb9e69900f4e04ece7128ba6805cefe31`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397f457616da9df263526cba72fe0dbda45caac3e0cbe2e69bf838da3addb5`  
		Last Modified: Wed, 13 Mar 2024 19:51:10 GMT  
		Size: 121.1 MB (121113479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b2d9907adca5620fa50fdcdb4a8584e515f41fbc1f1de8ad3bef32e8a3802d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f67baa25690fec61ebde8e331d03c4eeeae0feced180548f1ead0883a619ca`

```dockerfile
```

-	Layers:
	-	`sha256:fc5affdce7f58d29eb96d85a3b8746c7f5f9002c4e2c26769996e655da587a31`  
		Last Modified: Wed, 13 Mar 2024 19:51:07 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c709a3c395b4073e3315c03fcb982b8b52c22ca3eef7c6e651e27cd42c160a56`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:community-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:341f3a5aadc0069a742df1a903bcf8008106b86452096fef91866bf66fa6030c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406666010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592987248fc52eea0cddfb922127005aa993278a2bf1ba0950762bdf1ce7a705`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afb49dfe312a015b8f84bff69a471d3f96d98e63a7d284ea7f37ba3895ebcd`  
		Last Modified: Wed, 13 Mar 2024 19:54:56 GMT  
		Size: 121.1 MB (121113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:community-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:19727f1614520ef6a49ed526d18cc2179e47e970ec49c62a7c10f3a823812b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae583ff4566cd6515fc2f4a83acbfd12946d7a8a98b355d638204abcc068d69`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c9d172fac036019d2df3fb06bf4035f67c197ebb0bbb1095f4a8fd689b8c7`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5751f4e6c672776ffef60c8d44bf7289a514077fa66fe3cbf22ab0db03b8c1`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:36bc7fadb9afec73a2eb4bcfa19844a90bbb6a5957c07db8d1de3caec5b84771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:291c8f54bb68b73893d6b8033284f53a4d7eb6f8735209241a37f275d13b9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb73604ad9fd708f013276b18597e207831d18e14661fb70e54d7905191a5165`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68e5c089844daf9f08460efccfc0561874936190e10b4af31b74c5cdad648`  
		Last Modified: Wed, 13 Mar 2024 19:50:55 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f037a727b88b4f735ce95c33762cb3d044beef4b26093e50d932d18ab8b55`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b19e47a9c78334ceb36d56a8e9df45c497c368a990bb5c64dea11ba27fffff`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8266ce07a566a25dddc5b82565c41f15d92f3b3867fe3583ad7b310c146645`  
		Last Modified: Wed, 13 Mar 2024 19:51:00 GMT  
		Size: 380.8 MB (380843001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:50848cdacb6a5cb9e435d2c80e59afa04b2021b7c1c5195fcc0078494554320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7782abd9c2e9e89f1b2218ebea2d37e7bdd15c19629e9f08c682535a38965a`

```dockerfile
```

-	Layers:
	-	`sha256:7e79e748d787e14fc48dab9645096462fe1949dcdea86193ec5dd1eac7a16144`  
		Last Modified: Wed, 13 Mar 2024 19:50:52 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03b9ab1e275fe75e23c702bea31050b5e48c4865cd9212144dfa5d3d4475bce`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3a54ac46e2711df9a42b4dd1d2d60528b14b2b34844dad2864718610cfa4a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554612849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fb262c0611b2c5928d02e895ec57225bb2834bebb944918448cedc9d5c203c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:2e8069ee70137f9dcf7f4ef1b952b2bec6a4c23760dfcb967593e91b0abf124f`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75506c7aa22e57c2f47b01a544705e63ffa1483382d8a63b150fd69fa857dceb`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fa1249dabf9993c26d71ddf3ab7a48dad02cc7e2da8714ac96e1bfbded688`  
		Last Modified: Wed, 13 Mar 2024 19:53:03 GMT  
		Size: 380.8 MB (380807891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0a1f04ab05dd7afbfa7b9790d8e582fba472a1a7039045b01ead28ef552473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf8f432824b4e848d416af42e855fe3e235d5ff35f24928866ef02199be87`

```dockerfile
```

-	Layers:
	-	`sha256:11879ddd0521286ac33efd2fd80d27f144d507038a48ef5d03888060717b89ce`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eae2cc5909bfc60e5ccee8b43d7ca16e365bd934e1d637e18a263d56e23238c`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-bullseye`

```console
$ docker pull neo4j@sha256:36bc7fadb9afec73a2eb4bcfa19844a90bbb6a5957c07db8d1de3caec5b84771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-bullseye` - linux; amd64

```console
$ docker pull neo4j@sha256:291c8f54bb68b73893d6b8033284f53a4d7eb6f8735209241a37f275d13b9ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **557.2 MB (557171902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb73604ad9fd708f013276b18597e207831d18e14661fb70e54d7905191a5165`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e68e5c089844daf9f08460efccfc0561874936190e10b4af31b74c5cdad648`  
		Last Modified: Wed, 13 Mar 2024 19:50:55 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9f037a727b88b4f735ce95c33762cb3d044beef4b26093e50d932d18ab8b55`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b19e47a9c78334ceb36d56a8e9df45c497c368a990bb5c64dea11ba27fffff`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8266ce07a566a25dddc5b82565c41f15d92f3b3867fe3583ad7b310c146645`  
		Last Modified: Wed, 13 Mar 2024 19:51:00 GMT  
		Size: 380.8 MB (380843001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:50848cdacb6a5cb9e435d2c80e59afa04b2021b7c1c5195fcc0078494554320b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7782abd9c2e9e89f1b2218ebea2d37e7bdd15c19629e9f08c682535a38965a`

```dockerfile
```

-	Layers:
	-	`sha256:7e79e748d787e14fc48dab9645096462fe1949dcdea86193ec5dd1eac7a16144`  
		Last Modified: Wed, 13 Mar 2024 19:50:52 GMT  
		Size: 3.1 MB (3117385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03b9ab1e275fe75e23c702bea31050b5e48c4865cd9212144dfa5d3d4475bce`  
		Last Modified: Wed, 13 Mar 2024 19:50:51 GMT  
		Size: 21.5 KB (21474 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-bullseye` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:3a54ac46e2711df9a42b4dd1d2d60528b14b2b34844dad2864718610cfa4a756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **554.6 MB (554612849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fb262c0611b2c5928d02e895ec57225bb2834bebb944918448cedc9d5c203c`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:2e8069ee70137f9dcf7f4ef1b952b2bec6a4c23760dfcb967593e91b0abf124f`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 3.9 KB (3869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75506c7aa22e57c2f47b01a544705e63ffa1483382d8a63b150fd69fa857dceb`  
		Last Modified: Wed, 13 Mar 2024 19:52:55 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0fa1249dabf9993c26d71ddf3ab7a48dad02cc7e2da8714ac96e1bfbded688`  
		Last Modified: Wed, 13 Mar 2024 19:53:03 GMT  
		Size: 380.8 MB (380807891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-bullseye` - unknown; unknown

```console
$ docker pull neo4j@sha256:c0a1f04ab05dd7afbfa7b9790d8e582fba472a1a7039045b01ead28ef552473f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3138120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf8f432824b4e848d416af42e855fe3e235d5ff35f24928866ef02199be87`

```dockerfile
```

-	Layers:
	-	`sha256:11879ddd0521286ac33efd2fd80d27f144d507038a48ef5d03888060717b89ce`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 3.1 MB (3117613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eae2cc5909bfc60e5ccee8b43d7ca16e365bd934e1d637e18a263d56e23238c`  
		Last Modified: Wed, 13 Mar 2024 19:52:56 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi8`

```console
$ docker pull neo4j@sha256:4310ff4980bdf2d3e48af933af75a40bad9d9de04ebfa233ed9ded8e5accea61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:f902808606b9d851e0f845a09d761990ef6c3c77ae36100e62c0a2f57224a0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **580.8 MB (580773302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177880b2cdc2becdf0b4f97816e3a4527dfc99ebe4fa41d3bd353521124fafd6`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b3cdcc0fcc50d4668025f968000c2afed714f46ee20df4ce11ffaa6139f6d9`  
		Last Modified: Wed, 13 Mar 2024 19:51:26 GMT  
		Size: 163.6 MB (163561716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294d2a8bf56f29805f1f8f68a89835294359648b87729df86b37d385593b4209`  
		Last Modified: Wed, 13 Mar 2024 19:51:22 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b967bd37ff3320ff028a96db1aac102e93fd31705ce63b42d3ee7d54d95ea7a6`  
		Last Modified: Wed, 13 Mar 2024 19:51:30 GMT  
		Size: 377.9 MB (377909754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:a2ac61620b00ba644d792f0548fc39f220069589e37ebfca766c7a79d0f6b684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11016314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c524f7e2d85ebf1564979cc6de053c7c885272163037ab1f51f734a196a3c876`

```dockerfile
```

-	Layers:
	-	`sha256:095dcad2d1443929ceec3b23690b169934827fae9c219f5e0b1d66740a5c86bc`  
		Last Modified: Wed, 13 Mar 2024 19:51:23 GMT  
		Size: 11.0 MB (10996098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590dc6e12334138d71b0fc50874c79675a5a1610d118daa0c505b4eaaeae052f`  
		Last Modified: Wed, 13 Mar 2024 19:51:23 GMT  
		Size: 20.2 KB (20216 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b31f58175ee9ea4d607415def49ba100b3049afc5033862b529e98f0cdd02abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **577.7 MB (577692908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03453285a56de6678d11f497b9136de195446a5645d7341ed9d326821fde89a`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3db1a2827e3c72b057d3c6f8fc77649f55b495cf047cf474158db910d1b59e`  
		Last Modified: Wed, 13 Mar 2024 19:59:13 GMT  
		Size: 377.9 MB (377909610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:e88017bb6f9cea037b52be1345a87986027da417145e2e9b520581f387a98392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11013695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e75bd3640d8ad74db96e14460fff9ff5d131e366a94474a175a4f28760421b`

```dockerfile
```

-	Layers:
	-	`sha256:8babfb1ed8f1475bbc5ee9655dfca7ca093477b125937b1d7046a37a099ded26`  
		Last Modified: Wed, 13 Mar 2024 19:59:06 GMT  
		Size: 11.0 MB (10993636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5e04f76a59ff547c12080f11feefc950b726e561dd8d4fd28c5e31365ebd4d`  
		Last Modified: Wed, 13 Mar 2024 19:59:05 GMT  
		Size: 20.1 KB (20059 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:enterprise-ubi9`

```console
$ docker pull neo4j@sha256:c625ebec0cc54bddbd9b20825c1fe99cb3910907c09ece604bb53fb2f4a0daed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:enterprise-ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:d7a84d463b7828f322efc053ac7e05cb5665643e3185b4388750cf5e6bf99229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.6 MB (672646988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5a16a5894c56e2e264ac8331391806daffb40b6d1904f9bee70a75b0fad971`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519ff7f30ca3983ba588de9c8bb39d6249f05c72a937ed4a6bb4993a712134cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:15 GMT  
		Size: 257.0 MB (257005929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4897130454eb3efba649314a4bc87cff4299142800979350f9a5913b68f542`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a659939497f65e9c6ba0e5ba1979ee5e9b5a3bba9b20ee9d5d3a00b1a1f388a6`  
		Last Modified: Wed, 13 Mar 2024 19:51:16 GMT  
		Size: 377.9 MB (377909718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8986165b532d2dafb562bdd82e8c7f15a092a9eefb97eb17d9831cd9ce84cde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (14034458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e394f96c0331e083f2088390da6cea69a205dac5c2addfca9af56a85729a318b`

```dockerfile
```

-	Layers:
	-	`sha256:b6371e979dd44facf236abf0540555e0faa423b361db9a49e6f2a911f0f1a81b`  
		Last Modified: Wed, 13 Mar 2024 19:51:13 GMT  
		Size: 14.0 MB (14014516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4150c2413f9f9a1a0dcd1ddde083669c7bd2f73aeb39b37393c1e0a0b6db053`  
		Last Modified: Wed, 13 Mar 2024 19:51:11 GMT  
		Size: 19.9 KB (19942 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:enterprise-ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:469de50fb4138178d2cffb013fc62f72524f26a841c42a814b8d779af84eed9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.5 MB (663462155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2144acdc6adb88f8248251e98f366296ae3bdd71292dcae5695e89486949f8`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=2a4c8cea8ff65f02b3d386d9454db4b8054741551c731144c4759557d1a4f455 NEO4J_TARBALL=neo4j-enterprise-5.18.0-unix.tar.gz NEO4J_EDITION=enterprise NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-enterprise-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16328c2c13fc725904a8cb59fbb37d443dc97acc0c0cd8f0855df2e160e14c85`  
		Last Modified: Wed, 13 Mar 2024 19:56:12 GMT  
		Size: 377.9 MB (377909758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:enterprise-ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:22740e6aeb760cc0e21b368fc4eff0afcc49b05359d300dc68c9a7b22e6f6055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13927354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2faa27c1e6810120846222827a8ebfd8e69ee8215ef02c7e8f1f6bd671a618e`

```dockerfile
```

-	Layers:
	-	`sha256:e12752b901094a5ca78e2b9bb7889c509d0d0c13902a082f9341b1d728b2a571`  
		Last Modified: Wed, 13 Mar 2024 19:56:03 GMT  
		Size: 13.9 MB (13907570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e6222d2108f569f6e52d47c743941d41f85a412252a62c424cf1c69703e660f`  
		Last Modified: Wed, 13 Mar 2024 19:56:02 GMT  
		Size: 19.8 KB (19784 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:latest`

```console
$ docker pull neo4j@sha256:b018c04b0d01e7b6b3ff001d297fe2b80d0612a49516a7d20b0beb7f784994bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:latest` - linux; amd64

```console
$ docker pull neo4j@sha256:b084caeb649cb441efd13a8b756507a85752da14491ba0f32a81c22a90b7b089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300369655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec750d10cc32f7e6fa5691863d53380508e0f7645973ee1188773d55b7b465d`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc546a74d35e3481aa72e2b2dd73f424321211681a4e4b2cbdedb7aeccbe778`  
		Last Modified: Wed, 13 Mar 2024 19:50:35 GMT  
		Size: 144.9 MB (144893002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf06b88649235de5b9bf498d325d3915d780d1ed4fd0190c18db0a282021fb2`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b491c29ea63d437a5b25c4530bdddff17d2a8f5d741e37157da539b3872a572c`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d3e2e91469890a42573586aac4cb0d93a0697029eacb8eede062fbce8ae32`  
		Last Modified: Wed, 13 Mar 2024 19:50:33 GMT  
		Size: 124.0 MB (124040757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:b1c6f313a4a0fbc7a43e6c51850398a41e58d0eb0b5d9afba0dcad02357d81be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960274c276220aec8859ea63ea600466c5e962135496daaeb6104d2b911d2d1`

```dockerfile
```

-	Layers:
	-	`sha256:ed9b5f6dc78f72e36f99217b78ff3c24a71c22f4202c39fb2ab35743be00c6ea`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 3.0 MB (2950050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4e49fbfe4fad08551aa3b1f4741f3815037b2d84e1a225042c48d95e89b264`  
		Last Modified: Wed, 13 Mar 2024 19:50:31 GMT  
		Size: 23.8 KB (23843 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:latest` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:c5957770ff87483dd1c1964760c6b95386a72da71486d85728056f9f019d1116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297811784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfa90ebdd792adad3caac4b34ce41016fe81f4426252c5c9a318659cd4c4df9`
-	Entrypoint: `["tini","-g","--","\/startup\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 13 Mar 2024 08:34:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN addgroup --gid 7474 --system neo4j && adduser --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --ingroup neo4j neo4j # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN apt update     && apt-get install -y curl gcc git jq make procps tini wget     && curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* "${NEO4J_HOME}"     && rm ${NEO4J_TARBALL}     && mv "${NEO4J_HOME}"/data /data     && mv "${NEO4J_HOME}"/logs /logs     && chown -R neo4j:neo4j /data     && chmod -R 777 /data     && chown -R neo4j:neo4j /logs     && chmod -R 777 /logs     && chown -R neo4j:neo4j "${NEO4J_HOME}"     && chmod -R 777 "${NEO4J_HOME}"     && ln -s /data "${NEO4J_HOME}"/data     && ln -s /logs "${NEO4J_HOME}"/logs     && mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report     && git clone https://github.com/ncopa/su-exec.git     && cd su-exec     && git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af     && echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c     && echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c     && make     && mv /su-exec/su-exec /usr/bin/su-exec     && apt-get -y purge --auto-remove curl gcc git make     && rm -rf /var/lib/apt/lists/* /su-exec # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
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
	-	`sha256:62a531fb3ca6d74f8b41307bd0b7f6feb33bd7f451ee78c576042fd55759e053`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 3.9 KB (3877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9141f4f6d86b6ee11226df22a167c6c4e3f5c39c48d44733ff23894673cbb33`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ddfab853fa7058d1ba2167c38c773d5149fcbc28df21bb3f4ba98028a324c6`  
		Last Modified: Wed, 13 Mar 2024 19:51:46 GMT  
		Size: 124.0 MB (124006813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:latest` - unknown; unknown

```console
$ docker pull neo4j@sha256:d9f51436670990bba63c43abc28f78ac8396d330e028633cea3bb3e24ec7fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4826b1f5c45109a2dc5cbbb7de39b2b254f4f7f63ae16b5af865b8e6f0f4958d`

```dockerfile
```

-	Layers:
	-	`sha256:f4200f4134c1ca4973570205110b9fabfa806e88bf639e529fbbba6b7216aa44`  
		Last Modified: Wed, 13 Mar 2024 19:51:43 GMT  
		Size: 3.0 MB (2950294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fd5424314768dd3dbf28ced4d3f48f27e73708a6580ac5c5919a24c06a33cd`  
		Last Modified: Wed, 13 Mar 2024 19:51:42 GMT  
		Size: 22.9 KB (22891 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi8`

```console
$ docker pull neo4j@sha256:6c9f243fa81510db6aa5505df26a52e7611b76ea84d913c70bda4652051a1a63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi8` - linux; amd64

```console
$ docker pull neo4j@sha256:23537fc2083d180e5569564ed2797952e2abef56fb3eb91c268ba62859ff0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.0 MB (323977320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef15761b982190d9439415b0eb982acba1f6333d839bff7d43d5f3355e53223`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:74e0c06e5eac269967e6970582b9b25168177df26dffed37ccde09369302a87a`  
		Last Modified: Mon, 05 Feb 2024 10:53:50 GMT  
		Size: 39.3 MB (39292103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77028486db177a89cb66cf2763d75e58d29427748ca6f508480e69a5ddaedf31`  
		Last Modified: Wed, 13 Mar 2024 19:51:02 GMT  
		Size: 163.6 MB (163561830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77add1502997bbcc5385b65879528dc9a9d9c1b15acefbd01e5d39e39e6abf`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 9.7 KB (9696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b6ecc0c70706177ae703356b56c46b28e7cfb88e1a0d4702b467269604821`  
		Last Modified: Wed, 13 Mar 2024 19:51:01 GMT  
		Size: 121.1 MB (121113659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:1e769245f5a01edd4d1b7604e88b8311d22c1a0bae9645dab6a674b4b830aa87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10848963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2840a45f538e39308878e77b9784ad1627846224b37fe3e1d05be6ac71ac0d0`

```dockerfile
```

-	Layers:
	-	`sha256:747796166085b0847bb698552b72c0126023cca996d7c374b113897a08890ca4`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 10.8 MB (10827569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af28b95315527fd333c1978ba1325a4cd266bda1e53ffd36aabcd1f1cd1c4c9d`  
		Last Modified: Wed, 13 Mar 2024 19:50:59 GMT  
		Size: 21.4 KB (21394 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi8` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:b596e46ad7042157a98747abc9caf3440303be793511459ea168af99e0af7a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5896561f478c08e96ab4a229d5045817a3aa4c570ca8f9aff2f49c863a794ced`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y dnf;     dnf install -y         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     dnf remove -y gcc git make;     dnf autoremove;     dnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:2c4c07dbc80419961a4afec481bfcb4221efca54fdbf2cf08e8408c96c0b75bc`  
		Last Modified: Mon, 05 Feb 2024 11:48:16 GMT  
		Size: 37.6 MB (37639930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c38bfd11a7b45588d0c6f9cd5a99830ee4164293f15385f978d7a5fb467c3e7`  
		Last Modified: Wed, 13 Mar 2024 19:58:08 GMT  
		Size: 162.1 MB (162133639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669003a74a531c7a51e0163deee5bdbdcb44ef7b56fce48700481db091638ea`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 9.7 KB (9697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5e8b1702990a5e3913c43625e17a4ac0fd08c829c1db39af4d913cb79eb26f`  
		Last Modified: Wed, 13 Mar 2024 19:58:07 GMT  
		Size: 121.1 MB (121113674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi8` - unknown; unknown

```console
$ docker pull neo4j@sha256:65df63b45b3aa18ab1854b04a7e9ab8769f0044ba688c2e80bb1a2913c2b6d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6bfe11b32caa5a1c6118b911d9b06dbb1364235ac408c813b2a44526e5823`

```dockerfile
```

-	Layers:
	-	`sha256:7d097f259cb7c097e2a897bdbc6646ad95b51ca0928a482c2996451e361756d6`  
		Last Modified: Wed, 13 Mar 2024 19:58:05 GMT  
		Size: 10.8 MB (10825115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c24618edb8280ac3cd24095d327710beef60e57344e7ba8225d84b2104ccb2`  
		Last Modified: Wed, 13 Mar 2024 19:58:04 GMT  
		Size: 21.4 KB (21412 bytes)  
		MIME: application/vnd.in-toto+json

## `neo4j:ubi9`

```console
$ docker pull neo4j@sha256:13538af1c4025d0b37c48a0faacd4d2ba7f2ae9f424ddcc7c098e3fb1959263d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neo4j:ubi9` - linux; amd64

```console
$ docker pull neo4j@sha256:c717baed9f89995ad01c2ecec25876187e2c1898990cb76cfa9487e02082f0c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.9 MB (415850039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66573650f78e25ddb34d4ce68f09eaddec4d130e44ea7beca473a71785d1b51`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:0765fffac8ba6e6750a4f53defaa3c6361fb9dd8a72d4aa3eecea0b6a9d035dd`  
		Last Modified: Thu, 25 Jan 2024 16:53:03 GMT  
		Size: 37.7 MB (37721772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406ca0abd527c83573c07f9ce0e428083828deda1b5363f037f7b83d632b7994`  
		Last Modified: Wed, 13 Mar 2024 19:51:12 GMT  
		Size: 257.0 MB (257005216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2670a23b58c2338647617447b2e3870fb9e69900f4e04ece7128ba6805cefe31`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e397f457616da9df263526cba72fe0dbda45caac3e0cbe2e69bf838da3addb5`  
		Last Modified: Wed, 13 Mar 2024 19:51:10 GMT  
		Size: 121.1 MB (121113479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:8b2d9907adca5620fa50fdcdb4a8584e515f41fbc1f1de8ad3bef32e8a3802d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13867107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f67baa25690fec61ebde8e331d03c4eeeae0feced180548f1ead0883a619ca`

```dockerfile
```

-	Layers:
	-	`sha256:fc5affdce7f58d29eb96d85a3b8746c7f5f9002c4e2c26769996e655da587a31`  
		Last Modified: Wed, 13 Mar 2024 19:51:07 GMT  
		Size: 13.8 MB (13845987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c709a3c395b4073e3315c03fcb982b8b52c22ca3eef7c6e651e27cd42c160a56`  
		Last Modified: Wed, 13 Mar 2024 19:51:06 GMT  
		Size: 21.1 KB (21120 bytes)  
		MIME: application/vnd.in-toto+json

### `neo4j:ubi9` - linux; arm64 variant v8

```console
$ docker pull neo4j@sha256:341f3a5aadc0069a742df1a903bcf8008106b86452096fef91866bf66fa6030c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406666010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592987248fc52eea0cddfb922127005aa993278a2bf1ba0950762bdf1ce7a705`
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
# Wed, 13 Mar 2024 08:34:21 GMT
ENV JAVA_HOME=/usr
# Wed, 13 Mar 2024 08:34:21 GMT
RUN set -eux;     arch="$(uname -m)";     case "${arch}" in         'x86_64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini";             tinisha="93dcc18adc78c65a028a84799ecf8ad40c936fdfc5f2a57b1acda5a8117fa82c";             ;;         'aarch64')             tiniurl="https://github.com/krallin/tini/releases/download/v0.19.0/tini-arm64";             tinisha="07952557df20bfd2a95f9bef198b445e006171969499a1d361bd9e6f8e5e0e81";             ;;         *) echo >&2 "Neo4j does not currently have a docker image for architecture $arch"; exit 1 ;;     esac;     microdnf install -y --nodocs         findutils         gcc         git         gzip         hostname         java-17         jq         make         procps         shadow-utils         tar         wget         which;     wget -q ${tiniurl} -O /usr/bin/tini;     wget -q ${tiniurl}.asc -O tini.asc;     echo "${tinisha}"  /usr/bin/tini | sha256sum -c --strict --quiet;     chmod a+x /usr/bin/tini;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys         595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7         B42F6819007F00F88E364FD4036A9C25BF357DD4;     gpg --batch --verify tini.asc /usr/bin/tini;     git clone https://github.com/ncopa/su-exec.git;     cd su-exec;     git checkout 4c3bb42b093f14da70d8ab924b487ccfbb1397af;     echo d6c40440609a23483f12eb6295b5191e94baf08298a856bab6e15b10c3b82891 su-exec.c | sha256sum -c;     echo 2a87af245eb125aca9305a0b1025525ac80825590800f047419dc57bba36b334 Makefile | sha256sum -c;     make;     mv /su-exec/su-exec /usr/bin/su-exec;     gpgconf --kill all;     rm -rf "$GNUPGHOME" tini.asc /su-exec;     microdnf clean all # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin NEO4J_SHA256=5cfa57e9a94b6fcd68e48057d7a7871e424c8bc57f47fd985d6382c441ca754d NEO4J_TARBALL=neo4j-community-5.18.0-unix.tar.gz NEO4J_EDITION=community NEO4J_HOME=/var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
ARG NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
# Wed, 13 Mar 2024 08:34:21 GMT
COPY ./local-package/* /startup/ # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
# ARGS: NEO4J_URI=https://dist.neo4j.org/neo4j-community-5.18.0-unix.tar.gz
RUN set -eux;     groupadd --gid 7474 --system neo4j && useradd --uid 7474 --system --no-create-home --home "${NEO4J_HOME}" --gid neo4j neo4j;     curl --fail --silent --show-error --location --remote-name ${NEO4J_URI};     echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -c --strict --quiet;     tar --extract --file ${NEO4J_TARBALL} --directory /var/lib;     mv /var/lib/neo4j-* "${NEO4J_HOME}";     rm ${NEO4J_TARBALL};     mv "${NEO4J_HOME}"/data /data;     mv "${NEO4J_HOME}"/logs /logs;     chown -R neo4j:neo4j /data;     chmod -R 777 /data;     chown -R neo4j:neo4j /logs;     chmod -R 777 /logs;     chown -R neo4j:neo4j "${NEO4J_HOME}";     chmod -R 777 "${NEO4J_HOME}";     ln -s /data "${NEO4J_HOME}"/data;     ln -s /logs "${NEO4J_HOME}"/logs;     mv /startup/neo4j-admin-report.sh "${NEO4J_HOME}"/bin/neo4j-admin-report # buildkit
# Wed, 13 Mar 2024 08:34:21 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Mar 2024 08:34:21 GMT
WORKDIR /var/lib/neo4j
# Wed, 13 Mar 2024 08:34:21 GMT
VOLUME [/data /logs]
# Wed, 13 Mar 2024 08:34:21 GMT
EXPOSE map[7473/tcp:{} 7474/tcp:{} 7687/tcp:{}]
# Wed, 13 Mar 2024 08:34:21 GMT
ENTRYPOINT ["tini" "-g" "--" "/startup/docker-entrypoint.sh"]
# Wed, 13 Mar 2024 08:34:21 GMT
CMD ["neo4j"]
```

-	Layers:
	-	`sha256:5995d2c3a044ca24b3d19b7e7e55d359fc18627baa8aef944edb65b14383cefc`  
		Last Modified: Thu, 25 Jan 2024 16:53:01 GMT  
		Size: 36.0 MB (36049053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687120e2f6932ba28fb7fbe41a98d3ef8173702c0e00ba583e0a25449d9c082`  
		Last Modified: Wed, 13 Mar 2024 19:54:58 GMT  
		Size: 249.5 MB (249493772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fbf80a8b2826677e26083c2baa4077a01e0db1f95438202f7cdc718535ee2c`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 9.5 KB (9540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6afb49dfe312a015b8f84bff69a471d3f96d98e63a7d284ea7f37ba3895ebcd`  
		Last Modified: Wed, 13 Mar 2024 19:54:56 GMT  
		Size: 121.1 MB (121113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neo4j:ubi9` - unknown; unknown

```console
$ docker pull neo4j@sha256:19727f1614520ef6a49ed526d18cc2179e47e970ec49c62a7c10f3a823812b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13760187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae583ff4566cd6515fc2f4a83acbfd12946d7a8a98b355d638204abcc068d69`

```dockerfile
```

-	Layers:
	-	`sha256:9d3c9d172fac036019d2df3fb06bf4035f67c197ebb0bbb1095f4a8fd689b8c7`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 13.7 MB (13739049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f5751f4e6c672776ffef60c8d44bf7289a514077fa66fe3cbf22ab0db03b8c1`  
		Last Modified: Wed, 13 Mar 2024 19:54:52 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json
